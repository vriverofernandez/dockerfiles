# syntax=docker/dockerfile:1
FROM python:3.7-alpine
WORKDIR /code
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
ENV FLASK_ENV=development
RUN apk add --no-cache gcc musl-dev linux-headers
COPY web/requirements.txt requirements.txt
RUN pip install -r requirements.txt
EXPOSE 5000
COPY web/. .
CMD ["flask", "run"]
