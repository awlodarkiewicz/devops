FROM awlodarkiewicz/devops:php

# ads
RUN add-apt-repository ppa:adshares/releases -y
RUN apt-get update && apt-get install -y ads

# Yarn
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list

RUN apt-get update && apt-get install -y nodejs npm yarn

RUN apt-get -y autoremove
RUN apt-get clean
