FROM python:3.6-alpine

# Install Ansible & boto
RUN apk add --no-cache --virtual .build-deps  \
    gcc \
    libc-dev \
    libffi-dev \
    make \
    openssl-dev \
    # https://github.com/paramiko/paramiko/issues/1369
    && pip install cryptography==2.4.2 \ 
    && pip install ansible \
    && pip install boto \
    && pip install boto3 \
    && apk del .build-deps