FROM centos
RUN yum install -y https://rpms.remirepo.net/enterprise/remi-release-7.rpm
RUN yum install -y --enablerepo=remi-php71 php php-devel php-fpm php-gd php-intl php-mbstring php-mysqlnd php-opcache php-pecl-redis php-process php-xml
RUN yum install -y redis vim less
RUN useradd nginx
COPY ./localtime /etc/localtime
COPY ./www.conf /etc/php-fpm.d
RUN rm -f /usr/lib/systemd/system/systemd-udevd.service
RUN ln -s /usr/lib/systemd/system/php-fpm.service /etc/systemd/system/multi-user.target.wants/
CMD ["/sbin/init"]
