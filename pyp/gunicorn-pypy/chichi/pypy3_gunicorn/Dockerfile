
FROM pypy:3.6


RUN apt-get update -y 
#&& \
#    apt-get install -y python3 python3-dev python3-pip


RUN apt-get install -y sudo curl wget locales
RUN locale-gen en_CA.UTF-8
ENV LC_ALL=en_CA.UTF-8
ENV LANG=en_CA.UTF-8
ENV LANGUAGE=en_CA.UTF-8

# We copy just the requirements.txt first to leverage Docker cache
COPY ./requirements.txt ./app/requirements.txt

COPY . ./app



WORKDIR app


RUN pypy3 -m pip  install -r requirements.txt
RUN pypy3 -m pip install uvicorn
RUN pypy3 -m pip install fastapi
RUN pypy3 -m pip install fastapi[all]
RUN pypy3 -m pip install email-validator
RUN pypy3 -m pip install pymongo
RUN pypy3 -m pip install gunicorn
