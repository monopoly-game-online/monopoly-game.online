# pull official base image
FROM python:2.7-alpine

# set work directory
WORKDIR /usr/src/app

# set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# install psycopg2 dependencies
RUN apk update \
    && apk add postgresql-dev gcc python-dev zlib-dev jpeg-dev musl-dev libffi-dev \
    freetype-dev libjpeg freetype-dev libjpeg-turbo-dev libjpeg-turbo

# install dependencies
RUN pip install --upgrade pip
COPY ./requirements.txt .
RUN pip install -r requirements.txt

# copy project
COPY . .
