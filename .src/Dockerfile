FROM alpine:latest

WORKDIR /workspace

RUN apk update \
    && apk add python3 py-pip

WORKDIR /workspace/app

COPY bin .

RUN pip install -r requirements.txt

CMD [ "gunicorn", "-b", "0.0.0.0:5000", "main:app" ]