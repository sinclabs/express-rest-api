FROM node:lts-alpine
WORKDIR /workspace

RUN apk add --no-cache \
        python3 \
        py3-pip \
    && pip3 install --upgrade pip \
    && pip3 install \
        awscli \
    && rm -rf /var/cache/apk/*

RUN aws --version   # Just to make sure its installed alright

RUN apk add openssh git

COPY package.json .
RUN npm install --quiet