FROM awlodarkiewicz/devops:base

# Composer
RUN apt-get install -y \
        php7.2-cli php7.2-mysql php7.2-bcmath php7.2-bz2 php7.2-cli php7.2-curl \
        php7.2-gd php7.2-intl php7.2-json php7.2-mbstring php7.2-opcache \
        php7.2-readline php7.2-sqlite3 php7.2-xml php7.2-xmlrpc php7.2-xsl php7.2-zip unzip
RUN php -r "copy('https://getcomposer.org/installer', '/tmp/composer-setup.php');"
RUN php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer

RUN composer global require hirak/prestissimo

RUN apt-get -y autoremove
RUN apt-get clean

