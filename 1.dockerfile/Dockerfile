FROM python:3.6.8-jessie
RUN ln -snf /usr/share/zoneinfo/Europe/Moscow /etc/localtime && echo Europe/Moscow > /etc/timezone

RUN apt-get update -y && apt-get install -y curl
RUN pip install django

ADD . /app
ENTRYPOINT python /app/manage.py runserver 0.0.0.0:8000
