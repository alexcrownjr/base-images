FROM python:3.7.2-alpine3.9


ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1


RUN apk add --no-cache --virtual build-deps build-base

RUN apk add musl-dev python3-dev
RUN apk add --no-cache py-cryptography libffi-dev openssl-dev
RUN pip install cython

RUN pip install -U setuptools pip

RUN apk add --no-cache bash


RUN pip install uvloop
RUN pip install websockets
RUN pip install aioredis
