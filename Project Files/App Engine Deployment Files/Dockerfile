FROM python:3.8.2-alpine
LABEL maintainer="londonappdeveloper.com"

COPY ./requirements.txt /requirements.txt
COPY ./app /app
WORKDIR /app

RUN python -m venv /py && \
    /py/bin/pip install -r /requirements.txt && \
    adduser --disabled-password --no-create-home django-user

ENV PATH="/py/bin:$PATH"

USER django-user
