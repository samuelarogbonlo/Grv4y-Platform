FROM python:3.8-slim-buster

# RUN mkdir -p /home/core-api && chown -R node:node /home/auth-api
WORKDIR /home/core-api

COPY requirements.txt requirements.txt

RUN pip3 install -r requirements.txt

COPY . .

CMD [ "python3", "main.py"]