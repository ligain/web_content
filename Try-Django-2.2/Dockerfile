FROM python:3.6.10-alpine3.10

ENV DJANGO_HOST="0.0.0.0"
ENV DJANGO_PORT="8000"

WORKDIR /opt/django
COPY ./src .
COPY ./requirements.txt .

RUN apk add build-base zlib-dev jpeg-dev && pip install -r requirements.txt

EXPOSE ${DJANGO_PORT}

ENTRYPOINT python manage.py migrate && python manage.py runserver ${DJANGO_HOST}:${DJANGO_PORT}