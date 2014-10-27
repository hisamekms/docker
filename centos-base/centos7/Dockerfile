FROM centos:centos7
MAINTAINER Shinnosuke Ooyama <s.ooyama1003@gmail.com>

RUN \
  yum update -y && \
  yum install -y openssh-server passwd epel-release python-setuptools && \
  yum clean all && \
  easy_install supervisor 

# RUN yum -y install openssh-server passwd; yum clean all
# RUN useradd sshuser
# RUN echo -e "sshuser\nsshuser" | (passwd --stdin sshuser)

# RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key -N '' 

ADD assets /
CMD ["/config/bootstrap.sh"]
# EXPOSE 22
# CMD ["/usr/sbin/sshd", "-D"]
