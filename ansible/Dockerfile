FROM ekanai/centos6-ssh

# default
RUN yum clean all
RUN yum -y update glibc rsh rsh-server
RUN yum -y install epel-release
RUN yum -y update
RUN yum -y groupinstall 'Development tools'
RUN yum -y install \
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
#RUN curl https://bootstrap.pypa.io/get-pip.py | python - ; pip install httplib2


# run
WORKDIR /usr/local/src
RUN git clone git://github.com/ansible/ansible.git --recursive
WORKDIR /usr/local/src/ansible
RUN make rpm
RUN rpm -Uvh ./rpm-build/ansible-*.noarch.rpm

# expose
EXPOSE 22

