FROM python:3.7.2
MAINTAINER tanupoo "docker-shoichi@tanu.org"

ENV LANG C.UTF-8
ENV TZ=Asia/Tokyo

RUN apt-get update -y && apt-get install -y git
RUN pip install --upgrade pip && pip install pymongo==3.10.1 aiohttp==3.6.2

WORKDIR /app
RUN mkdir -p /app/var
RUN git clone --recursive https://github.com/tanupoo/penguin.git

WORKDIR /app/penguin
CMD [ "/app/penguin/penguin.py", "/app/var/conf/penguin.conf" ]

