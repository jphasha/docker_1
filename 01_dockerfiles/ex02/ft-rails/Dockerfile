FROM ruby

RUN apt-get update -y
RUN gem install rails
RUN apt-get install -y nodejs
RUN apt-get install -y sqlite3
RUN apt-get install -y build-essential
RUN apt-get install -y libpq-dev
RUN gem update

ONBUILD EXPOSE 3000
ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed