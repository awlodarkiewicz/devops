FROM awlodarkiewicz/devops:php

# ads
RUN add-apt-repository ppa:adshares/releases -y && \
    curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
    apt-get update && \
    apt-get -qq -y --no-install-recommends install \
        nodejs npm yarn ads && \
    apt-get -y autoremove && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    curl https://raw.githubusercontent.com/adshares/adserver/master/composer.json --output composer.json && \
    composer install --no-autoloader --no-scripts && \
    curl https://raw.githubusercontent.com/adshares/adserver/master/package.json --output package.json && \
    yarn install
