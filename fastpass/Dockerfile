FROM python:3.7-alpine
MAINTAINER Ronnel Matthew Robles

ENV PYTHONUNBUFFERED 1

WORKDIR /fastpass_api

COPY requirements.txt /fastpass_api
RUN pip3 install --upgrade pip -r requirements.txt

COPY . /fastpass_api

RUN adduser -D user
USER user

EXPOSE 8000
CMD python3 manage.py runserver 0.0.0.0:8000
