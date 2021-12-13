FROM python:3.10-alpine

# Now copy the requirements.txt file for pyhton with all the necessary packages into a temporary folder
COPY requirements.txt /tmp/pip-tmp/

# Now intall all the python packages, that are in that temporary folder

RUN    apk add --update --no-cache --virtual .tmp gcc libc-dev linux-headers jpeg-dev zlib-dev \
    && pip install -r /tmp/pip-tmp/requirements.txt \
    && rm -rf /tmp/pip-tmp \
    && apk del .tmp gcc libc-dev linux-headers jpeg-dev zlib-dev \
    && apk add bash libjpeg\
    && rm -r /tmp/* \
    && rm -rf /var/cache/apk/*
