FROM alpine:latest

#EXPOSE 3000  

RUN apk add --update tini

RUN apk add bash ansible git openssh-client mlocate && updatedb

RUN mkdir /home/ansible && mkdir /home/ansible/.ssh

WORKDIR /home/ansible

COPY gitclone.sh gitclone.sh 

CMD ["sh","gitclone.sh"] && /bin/bash

#WORKDIR /usr/src/app

#COPY package.json package.json

#COPY . .

#CMD ["/sbin/tini","--","node","./bin/www"]
