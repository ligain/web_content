FROM python:3.6.10-alpine3.10

WORKDIR /opt/django
COPY ./src .
COPY ./requirements.txt .

RUN apk add build-base zlib-dev jpeg-dev && pip install -r requirements.txt

EXPOSE 8000

ENTRYPOINT python manage.py migrate && python manage.py runserver 0.0.0.0:8000