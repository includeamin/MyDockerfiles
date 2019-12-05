FROM pypy:3.6


RUN apt-get update -y
RUN apt-get install -y sudo curl wget locales
RUN locale-gen en_CA.UTF-8
ENV LC_ALL=en_CA.UTF-8
ENV LANG=en_CA.UTF-8
ENV LANGUAGE=en_CA.UTF-8

COPY ./requirements.txt ./requirements.txt

RUN pip  install -r requirements.txt
RUN pip install gunicorn
RUN pip install termcolor

