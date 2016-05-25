FROM java:alpine
RUN apk add --no-cache bash
RUN mkdir /home/app
WORKDIR /home/app
COPY . /home/app
RUN javac -cp rabbitmq-client.jar:json.jar Worker.java
RUN chmod +x /home/app/start_stroopwafel_minion.sh
CMD /home/app/start_stroopwafel_minion.sh