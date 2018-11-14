FROM ubuntu:18.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install -y aptitude software-properties-common
RUN apt-get install -y python curl git gettext-base

# ads
RUN add-apt-repository ppa:adshares/releases -y
RUN apt-get install -y ads

# Ansible
RUN apt-get -y update
RUN apt-get -y install software-properties-common
RUN apt-add-repository -y ppa:ansible/ansible
RUN apt-get -y update
RUN apt-get -y install ansible

# Docker
RUN ansible-galaxy install geerlingguy.docker

# Yarn
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list

RUN apt-get install -y nodejs npm
RUN apt-get update && apt-get install -y yarn

# Composer
RUN apt-get install -y \
        php7.2-cli php7.2-mysql php7.2-bcmath php7.2-bz2 php7.2-cli php7.2-curl \
        php7.2-gd php7.2-intl php7.2-json php7.2-mbstring php7.2-opcache \
        php7.2-readline php7.2-sqlite3 php7.2-xml php7.2-xmlrpc php7.2-xsl php7.2-zip unzip
RUN php -r "copy('https://getcomposer.org/installer', '/tmp/composer-setup.php');"
RUN php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer

RUN composer global require hirak/prestissimo

RUN apt-get install -y python python-pip

RUN pip install pipenv

RUN apt-get -y autoremove
