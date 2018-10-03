FROM ubuntu:18.04

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install -y aptitude software-properties-common
RUN apt-get install -y python curl git

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
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

RUN apt-get update && apt-get install -y yarn

# Composer
RUN apt-get install -y php7.2-cli php7.2-curl php7.2-zip
RUN php -r "copy('https://getcomposer.org/installer', '/tmp/composer-setup.php');"
RUN php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer

RUN composer global require hirak/prestissimo
