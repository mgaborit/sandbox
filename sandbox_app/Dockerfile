FROM python:3.8-slim-buster

ENV SRC_DIR=/src
WORKDIR $SRC_DIR

COPY src/requirements.txt $SRC_DIR/requirements.txt

RUN pip install -r requirements.txt

COPY src/ .

CMD [ "gunicorn", "--bind", "0.0.0.0:8000", "wsgi" ]

EXPOSE 8000