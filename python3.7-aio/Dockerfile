FROM python:3.7.4-alpine3.9


ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN apk update && apk add bash

RUN apk add --no-cache --virtual .build-deps \
    build-base \
    gcc \
    python3-dev \
    musl-dev \
    postgresql-dev \
    && pip install --no-cache-dir psycopg2


RUN apk add --no-cache py-cryptography libffi-dev openssl-dev
#RUN pip install cython

RUN pip install -U setuptools pip
RUN pip install -vvv uvloop
COPY requirements.txt ./requirements.txt

RUN pip install --no-cache-dir -r requirements.txt

RUN apk del .build-deps





