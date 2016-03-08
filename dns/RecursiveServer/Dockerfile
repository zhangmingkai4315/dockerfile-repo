###########################################
# Dockerfile to recursive named server
###########################################

FROM centos
MAINTAINER Mike <zhangmingkai19892013@gmail.com>
#RUN yum -y update && \
RUN yum -y install wget  && \
    yum -y install bind  && \
    mkdir /var/named/log &&  \
    chown named.named /var/named/log && \
    wget -P /tmp https://raw.githubusercontent.com/zhangmingkai4315/dockerfile-repo/master/dns/RecursiveServer/named.conf \
    && mv /etc/named.conf /etc/named.conf_bk \
    && cp -f /tmp/named.conf /etc/named.conf \
    && chown named.named /etc/named.conf

ENTRYPOINT ["named","-u","named","-g"]
EXPOSE 53/udp
