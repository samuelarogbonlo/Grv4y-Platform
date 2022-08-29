FROM python:3.8-slim-buster

# RUN mkdir -p /home/auth-api && chown -R node:node /home/auth-api
WORKDIR /home/auth-api

COPY requirements.txt requirements.txt
COPY users.json .

RUN pip3 install -r requirements.txt

COPY . .

CMD [ "python3", "main.py"]