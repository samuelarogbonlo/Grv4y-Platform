# Platform-Challenge

# Architecture Overview

```
+----------------------------------+
|            Merchant              |
+-+--------^------------+--------^-+
  |        |            |        |
 (1)      (2)          (3)      (5)
  |        |            |        |
+-v--------+-+        +-v--------+-+        +-----------------+
|  Auth API  |        |  Core API  |        |  PSP Connector  | 
+------------+        +------+-----+        +---------^-------+
                             |                        |
                            (4)                      (6)
                             |                        |
                      +------v------------------------+-------+
                      |          Redis Message Queue          |
                      +---------------------------------------+
```

There are 3 distinct services:

- [Auth API] - Creates authentication tokens to valid users.
- [Core API] - Processes transaction requests.
- [PSP Connector] - Processes the transactions with a Payment Service Provider (PSP).

## Requirments
- Ensure the ports are different for each of the services.
- Ensure Docker Daemon is running.
- Ensure Redis is installed and running.
- Ensure to always be in the right directory.


## Start-Up Processes

- Build all the docker images by getting to the directories of each of the services and running `docker build .`.
- Start the local enviroment with `Docker-compose up`.
- Install all the requirments for each service. 
- Run the application depending on the python version running on your local machine.
- Test the endpoints as well

## Authors
- Samuel Arogbonlo - [GitHub](https://github.com/samuelarogbonlo) · [Twitter](https://twitter.com/samuelarogbonlo)

## Collaborators
- [YOUR NAME HERE] - Feel free to contribute to the codebase by resolving any open issues, refactoring, adding new features, writing test cases or any other way to make the project better and helpful to the community. Feel free to fork and send pull requests.


## License

The MIT License (http://www.opensource.org/licenses/mit-license.php)
