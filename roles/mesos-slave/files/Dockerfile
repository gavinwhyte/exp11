FROM centos:7

#ENV MESOS_ZK
#ENV MESOS_CONTAINERIZERS

RUN rpm -i http://repos.mesosphere.io/el/7/noarch/RPMS/mesosphere-el-repo-7-1.noarch.rpm && yum -y install mesos

RUN yum install -y epel-release && yum install --enablerepo=epel-testing -y docker-io

COPY sbin/init /usr/local/sbin/init

ENTRYPOINT ["/bin/sh", "/usr/local/sbin/init"]
