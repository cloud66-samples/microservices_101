FROM php:5.6-cli

RUN apt-get update
RUN apt-get install netcat -y

#set working dir
RUN mkdir /home/app
WORKDIR /home/app
COPY . /home/app
RUN docker-php-ext-install mbstring bcmath

#start the rainbowcake minion
CMD /home/app/start_rainbowcake_minion.sh