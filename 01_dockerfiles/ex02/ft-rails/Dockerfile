FROM ruby

RUN apt-get update -y && apt-get upgrade -y && apt-get install nodejs -y

MAINTAINER mcomet <mcomet@student.21-school.ru>

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD EXPOSE 3000

ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed
