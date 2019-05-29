FROM python:3.7.3-stretch

#RUN apt-get install build-essential libffi-dev openssl-dev musl-dev python3-dev

RUN pip install cython

RUN pip install -U setuptools pip



RUN pip install uvloop
RUN pip install websockets
RUN pip install aioredis
RUN pip install pandas numpy
RUN pip install https://github.com/sammchardy/python-binance/archive/feature/asyncio.zip
