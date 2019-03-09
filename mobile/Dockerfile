FROM node:10.15.1
MAINTAINER Adam Gasiorek "<adam.bjp@gmail.com>"
ENV REFRESHED_AT 2019_02_21

RUN useradd --user-group --create-home --shell /bin/false app && npm install -g @angular/cli && npm install -g nativescript

ENV HOME=/home/app
WORKDIR $HOME

ENV APP_NAME=mobile

COPY . $HOME/$APP_NAME/
RUN chown -R app:app $HOME/*

USER app

WORKDIR $HOME/$APP_NAME
RUN npm install

EXPOSE 4200 49152
