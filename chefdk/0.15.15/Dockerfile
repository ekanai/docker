FROM ekanai/centos6-ssh

# default
RUN yum clean all
RUN yum -y update glibc rsh rsh-server
RUN yum -y install epel-release
RUN yum -y update
RUN yum -y groupinstall 'Development tools'
RUN yum -y install \
      wget \
      which \
      gcc \
      rpm-build \
      make \
      asciidoc \
      git \
      python-setuptools \
      python2-devel \
      PyYAML \
      python-httplib2 \
      python-crypto2.6 \
      python-jinja2 \
      python-paramiko \
      python-keyczar \
      python-six \
      sshpass


# run
WORKDIR /usr/local/src
RUN mkdir chefdk
WORKDIR /usr/local/src/chefdk
RUN wget https://packages.chef.io/stable/el/6/chefdk-0.15.15-1.el6.x86_64.rpm
RUN rpm -i chefdk-0.15.15-1.el6.x86_64.rpm

# expose
EXPOSE 22

