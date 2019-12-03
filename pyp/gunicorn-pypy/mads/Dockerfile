FROM pypy:3.6




COPY ./requirements.txt ./app/requirements.txt

COPY . ./app

RUN ls
RUN cd /app/Configures && ls

WORKDIR /app


RUN pip  install -r requirements.txt
RUN pip install gunicorn
RUN pip install termcolor

