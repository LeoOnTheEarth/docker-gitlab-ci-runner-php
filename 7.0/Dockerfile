# docker-gitlab-ci-runner-php (PHP 7.0)
FROM centos:7
LABEL Leo "leo.on.the.earth@gmail.com"

# Install epel repo & remi repo & PHP 7.0 & composer & box.phar
RUN cd /tmp && \
    curl -O https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm && \
    curl -O https://rpms.remirepo.net/enterprise/remi-release-7.rpm && \
    rpm -Uvh remi-release-7*.rpm epel-release-latest-7*.rpm && \
    yum -y update && \
    yum --enablerepo=remi,remi-php70 install -y \
    which \
    git \
    unzip gzip tar bzip2 \
    rsync \
    php \
    php-bcmath \
    php-cli \
    php-common \
    php-dba \
    php-devel \
    php-embedded \
    php-enchant \
    php-fpm \
    php-gd \
    php-gmp \
    php-imap \
    php-interbase \
    php-intl \
    php-ldap \
    php-litespeed \
    php-mbstring \
    php-mcrypt \
    php-mssql \
    php-mysqlnd \
    php-odbc \
    php-opcache \
    php-pdo \
    php-pear \
    php-pgsql \
    php-process \
    php-pspell \
    php-recode \
    php-snmp \
    php-soap \
    php-tidy \
    php-xml \
    php-xmlrpc \
    php-pecl-memcache \
    php-pecl-memcached \
    php-pecl-redis \
    php-pecl-xdebug \
    php-pecl-zip && \
    yum clean all && \
    echo 'date.timezone="UTC"' > /etc/php.d/docker-gitlab-ci-runner-php.ini && \
    echo 'phar.readonly=off' >> /etc/php.d/docker-gitlab-ci-runner-php.ini && \
    mkdir /root/.composer && \
    mkdir /root/.ssh && \
    mkdir /cache && \
    php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" && \
    php -r "if (hash_file('sha384', 'composer-setup.php') === '906a84df04cea2aa72f40b5f787e49f22d4c2f19492ac310e8cba5b96ac8b64115ac402c8cd292b8a03482574915d1a8') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;" && \
    php composer-setup.php && \
    php -r "unlink('composer-setup.php');" && \
    mv composer.phar /usr/local/bin/composer

VOLUME ["/cache", "/root/.composer", "/root/.ssh"]
