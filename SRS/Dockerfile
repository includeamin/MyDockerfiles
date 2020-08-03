FROM ubuntu:18.04

WORKDIR app
RUN apt update -y
RUN apt install -y git
RUN apt-get install -y --force-yes gcc
#RUN git clone https://github.com/ossrs/srs -b 4.0release
RUN apt-get install -y --force-yes g++
RUN apt-get install -y --force-yes make
RUN apt-get install -y --force-yes unzip
RUN apt-get install -y --force-yes pkg-config
RUN apt-get update -y
RUN apt-get dist-upgrade -y  
RUN apt install -y python
RUN git clone https://github.com/ossrs/srs -b 4.0release
RUN cd srs/trunk && ./configure && make
EXPOSE 8000
EXPOSE 1935
EXPOSE 8080
EXPOSE 1985
EXPOSE 8544
WORKDIR srs/trunk
ADD rtc_flv.conf rtc_flv.conf

CMD ./objs/srs -c rtc_flv.conf
 
#conf/rtc.conf
