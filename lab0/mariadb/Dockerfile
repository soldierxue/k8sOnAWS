FROM centos:7
MAINTAINER Student <student@foo.io>
# Deps for mariadb
RUN yum -y install mariadb-server openssl psmisc net-tools hostname && \
    yum clean all

# Add set up scripts
ADD scripts /scripts
RUN chmod 755 /scripts/*

EXPOSE 3306
VOLUME /var/lib/mysql
CMD ["/bin/bash", "/scripts/start.sh"]
