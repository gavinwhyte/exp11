FROM centos:7

RUN yum install -y unzip wget

ENV CONSUL_VERSION 0.5.2

RUN cd /tmp && wget https://dl.bintray.com/mitchellh/consul/${CONSUL_VERSION}_linux_amd64.zip && unzip ${CONSUL_VERSION}_linux_amd64.zip -d /usr/local/bin && rm ${CONSUL_VERSION}_linux_amd64.zip

VOLUME /tmp/consul

ENTRYPOINT ["consul"]
