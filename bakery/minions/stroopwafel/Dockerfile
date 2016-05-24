FROM java:alpine
RUN apk add --no-cache bash
RUN mkdir /home/app
WORKDIR /home/app
COPY . /home/app
RUN javac -cp rabbitmq-client.jar:json.jar Worker.java
CMD /home/app/start_stroopwafel_minion.sh