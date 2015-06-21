FROM centos:7

#ENV MESOS_ZK

RUN rpm -i http://repos.mesosphere.io/el/7/noarch/RPMS/mesosphere-el-repo-7-1.noarch.rpm && yum -y install marathon mesos

COPY sbin/init /usr/local/sbin/init

ENTRYPOINT ["/bin/sh", "/usr/local/sbin/init"]
