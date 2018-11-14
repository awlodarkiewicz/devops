FROM awlodarkiewicz/devops:base

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get install -y python python-pip

RUN pip install pipenv

RUN apt-get -y autoremove
