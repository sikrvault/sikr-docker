FROM python:3-alpine

RUN apk update && apk upgrade \
    && apk add python3-dev build-base linux-headers pcre-dev git \
               libffi libffi-dev openssl openssl-dev libssl1.0 libpq \
               postgresql-client postgresql-libs postgresql-dev \
    && pip install uwsgi psycopg2

RUN git clone https://github.com/sikrvault/sikr.git sikr

WORKDIR /sikr
RUN pip install -r requirements/common.txt

CMD uwsgi --http :8080 --wsgi-file app.py --callable api


