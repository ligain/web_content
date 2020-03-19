FROM python:3.8-alpine3.10

ENV SANIC_HOST="0.0.0.0"
ENV SANIC_PORT="8081"

WORKDIR /app

COPY app.py .

RUN apk add build-base libffi && pip install sanic

EXPOSE ${SANIC_PORT}

CMD ["python", "app.py"]