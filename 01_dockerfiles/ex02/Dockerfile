FROM        ft-rails:on-build
FROM ruby:2.5

MAINTAINER hakeemata <hhaakkimm@gmail.com>

RUN apt-get update -qq && apt-get install -y nodejs postgresql-client
RUN mkdir /myapp

WORKDIR /myapp

COPY Gemfile /myapp/Gemfile
COPY Gemfile.lock /myapp/Gemfile.lock

RUN bundle install

COPY . /myapp

COPY entrypoint.sh /usr/bin/

RUN chmod +x /usr/bin/entrypoint.sh

ENTRYPOINT ["entrypoint.sh"]

EXPOSE 3000

CMD         ["rails", "s", "-b", "0.0.0.0", "-p", "3000"]
