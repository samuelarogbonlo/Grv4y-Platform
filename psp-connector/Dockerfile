FROM python:3.8-slim-buster

# RUN mkdir -p /home/psp-connector && chown -R node:node /home/psp-connector
WORKDIR /home/psp-connector

COPY requirements.txt requirements.txt

RUN pip3 install -r requirements.txt

RUN export REDIS_URL=redis://redis:6379/0

COPY . .

CMD [ "python3", "./main.py"]