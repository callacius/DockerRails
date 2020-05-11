FROM ruby:alpine:3.11
MAINTAINER Daniel Costa <callacius@gmail.com>

RUN apk --update --upgrade add ruby-io-console ruby-json yaml nodejs

RUN apk --update --upgrade add zlib-dev libxml2-dev libxslt-dev tzdata yaml-dev sqlite-dev postgresql-dev mysql-dev

ENV RAILS_VERSION 6.0.2.1

RUN gem install -N rails --version "$RAILS_VERSION" 

EXPOSE 3000

CMD ["rails", "server", "-b", "0.0.0.0"]