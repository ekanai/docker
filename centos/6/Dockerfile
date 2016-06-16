FROM centos:6

# Update
RUN yum -y update

# Time Zone
RUN echo 'ZONE="Asia/Tokyo"' > /etc/sysconfig/clock
RUN rm -f /etc/localtime
RUN ln -fs /usr/share/zoneinfo/Asia/Tokyo /etc/localtime

# yum
RUN yum -y install \
      tar \
      wget \
      zip \
      unzip \
      git \
      tcpdump

