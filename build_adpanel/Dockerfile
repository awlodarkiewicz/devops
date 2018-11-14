FROM awlodarkiewicz/devops:js

RUN curl https://raw.githubusercontent.com/adshares/adpanel/master/package.json --output package.json
RUN yarn install

RUN apt-get -y autoremove
RUN apt-get clean
