FROM python:3.9-slim

WORKDIR /app

COPY . /app

RUN pip install -r requirements.txt

EXPOSE 8443

CMD ["gunicorn", "wsgi:webhook", "--log-level=info", "--workers", "3", "--bind", "0.0.0.0:8443", "--keyfile", "/certs/webhook.key", "--certfile", "/certs/webhook.crt"]
