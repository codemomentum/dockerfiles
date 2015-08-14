FROM java:8

##Flink 0.9.0 Installation
###Download:
RUN mkdir ~/downloads && cd ~/downloads && \
    wget -q -O - http://mirrors.advancedhosters.com/apache/flink/flink-0.9.0/flink-0.9.0-bin-hadoop2.tgz | tar -zxvf - -C /usr/local/
RUN cd /usr/local && ln -s ./flink-0.9.0 flink

ENV FLINK_HOME /usr/local/flink
ENV PATH $PATH:$FLINK_HOME/bin

EXPOSE 8081

CMD ["/usr/local/flink/bin/start-local.sh"]
