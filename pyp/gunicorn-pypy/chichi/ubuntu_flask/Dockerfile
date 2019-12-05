FROM pypy:3.6


RUN apt-get update -y

COPY ./requirements.txt ./app/requirements.txt

RUN pip3  install -r requirements.txt
RUN pip3 install gunicorn
RUN pip3 install termcolor

