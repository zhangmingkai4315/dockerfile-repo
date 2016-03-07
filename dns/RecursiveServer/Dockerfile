###########################################
# Dockerfile to recursive named server
###########################################

FROM centos
MAINTAINER Mike <zhangmingkai19892013@gmail.com>
#RUN yum -y update && \
RUN yum -y install wget  && \
    yum -y install bind  && \
    mkdir /var/named/log &&  \
    wget -P /tmp https://raw.githubusercontent.com/zhangmingkai4315/dockerfile-repo/master/dns/RecursiveServer/named.conf \
    && cp -f /tmp/named.conf /etc/named.conf \
    && chown root.named /etc/named.conf

ENTRYPOINT ["named","-g"]
EXPOSE 53
