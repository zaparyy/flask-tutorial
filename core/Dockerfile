FROM alpine:latest

WORKDIR /

EXPOSE 8080/tcp
VOLUME /app

RUN apk add python3 py3-pip; python3 -m venv /flafla

CMD /flafla/bin/python3 -m pip install /app; \
    /flafla/bin/python3 -m flask --app flaskr init-db; \
    /flafla/bin/python3 -m flask --app flaskr run -h 0.0.0.0

