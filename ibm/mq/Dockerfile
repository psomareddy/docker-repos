FROM ibmcom/mq:latest

LABEL author="Prakash Reddy"

ENV LICENSE=accept
ENV MQ_QMGR_NAME=QM1

WORKDIR /app

EXPOSE 1414
EXPOSE 9443

USER root
RUN useradd newrelic -G mqm && \
    echo newrelic:passw0rd | chpasswd
	
USER mqm 
COPY Docker-config.mqsc /etc/mqm/

