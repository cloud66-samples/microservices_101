FROM ruby:2.2

RUN apt-get update
RUN apt-get install netcat -y

#set working dir for caching
WORKDIR /tmp

#cache bundle install
ADD Gemfile /tmp/Gemfile
ADD Gemfile.lock /tmp/Gemfile.lock
RUN bundle install

#set working dir
RUN mkdir /home/app
WORKDIR /home/app
COPY . /home/app

#start the bagel minion
CMD /home/app/start_counter.sh
