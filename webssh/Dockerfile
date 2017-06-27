FROM xuqplus/centos:6.8

MAINTAINER xuqplus <445172495@qq.com>

ADD source/supervisord.conf /etc/
ADD source/get-pip.py /
RUN python get-pip.py && rm -rf /get-pip.py && pip install supervisor
RUN yum install -y epel-release
RUN yum install -y shellinabox
RUN /usr/sbin/useradd centos && echo 'centos:wayout'|chpasswd && echo 'root:wayout'|chpasswd && usermod -s /bin/bash centos

CMD /usr/bin/supervisord
