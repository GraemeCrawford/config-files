FROM scratch
MAINTAINER The CentOS Project <cloud-ops@centos.org>
ADD centos-7.2.1511-docker.tar.xz /

RUN yum remove -y iputils && yum update -y && \ 
    yum install -y epel-release && \ 
    yum install -y docker python-pip graphviz rpm-python dpkg && \
    pip install anchore && \
    /usr/bin/anchore feeds sync

LABEL name="CentOS Base Image"
LABEL vendor="CentOS"
LABEL license=GPLv2

CMD ["/bin/bash"]
