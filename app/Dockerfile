FROM python:3.12-alpine
LABEL MANTAINER="Pedro Ramos"

WORKDIR /app

COPY . /app

RUN apk upgrade --no-cache && apk add --no-cache curl \
    && pip install --trusted-host pypi.python.org -r requirements.txt

EXPOSE 8000

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "app:app"]
