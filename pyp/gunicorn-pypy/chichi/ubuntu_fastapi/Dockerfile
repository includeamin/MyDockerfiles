FROM ubuntu:18.04

RUN apt-get update -y && \
   apt-get install -y python3 python3-dev python3-pip


RUN apt-get install -y sudo curl wget locales
RUN locale-gen en_CA.UTF-8
ENV LC_ALL=en_CA.UTF-8
ENV LANG=en_CA.UTF-8
ENV LANGUAGE=en_CA.UTF-8

# We copy just the requirements.txt first to leverage Docker cache
COPY ./requirements.txt ./app/requirements.txt

COPY . ./app



WORKDIR app


RUN pip3  install -r requirements.txt
RUN pip3 install uvicorn
RUN pip3 install fastapi
RUN pip3 install fastapi[all]
RUN pip3 install email-validator
RUN pip3 install pymongo
RUN pip3 install gunicorn

