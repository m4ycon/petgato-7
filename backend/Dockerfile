# syntax=docker/dockerfile:1
FROM ruby:2.7.3-alpine
RUN apk update -qq && apk upgrade
RUN apk add --virtual build-dependencies build-base
RUN apk add nodejs postgresql-client postgresql-dev
WORKDIR /home/api
COPY . /home/api
COPY Gemfile /home/api/Gemfile
COPY Gemfile.lock /home/api/Gemfile.lock
RUN bundle install

# Add a script to be executed every time the container starts.
COPY entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/entrypoint.sh
ENTRYPOINT ["entrypoint.sh"]
EXPOSE 3001

# Configure the main process to run when running the image
CMD ["rails", "s", "-b", "0.0.0.0"]

