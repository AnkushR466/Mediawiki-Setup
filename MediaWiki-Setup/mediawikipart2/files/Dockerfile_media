FROM centos:latest

RUN echo -e "[new]\nbaseurl=http://mirror.centos.org/centos/7/os/x86_64/\ngpgcheck=0" >> /etc/yum.repos.d/new.repo

RUN yum install http://rpms.remirepo.net/enterprise/remi-release-7.rpm  -y

RUN yum-config-manager --enable remi-php73 

RUN yum install httpd php php-mysql php-gd php-xml php-mbstring php-intl  epel-release python-pip mariadb-devel gcc python-devel -y

RUN /usr/sbin/httpd 

# RUN yum install mariadb-server mysql mariadb-devel
# RUN /usr/libexec/mariadb-prepare-db-dir %n

RUN yum install wget -y
RUN wget https://releases.wikimedia.org/mediawiki/1.32/mediawiki-core-1.32.3.tar.gz

RUN tar -zxpvf mediawiki-core-1.32.3.tar.gz

RUN mv mediawiki-1.32.3 /var/www/html/mediawiki; chown -R apache:apache /var/www/html/mediawiki/ ; chown -R apache:apache /var/www/html/mediawiki/

CMD /usr/sbin/httpd -DFOREGROUND 

