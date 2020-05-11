FROM ruby
MAINTAINER Daniel Costa <callacius@gmail.com>

RUN apt-get update \
    && apt-get install -y nodejs --no-install-recommends \
    && rm -rf /var/lib/apt/lists/*

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        postgresql-client \
    && rm -rf /var/lib/apt/lists/*

ENV RAILS_VERSION 6.0.2.1

RUN gem install rails --version "$RAILS_VERSION"

EXPOSE 3000
CMD ["rails", "server", "-b", "0.0.0.0"]