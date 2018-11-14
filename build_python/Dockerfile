FROM awlodarkiewicz/devops:base

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get -qq -y --no-install-recommends install \
        python python-pip python-dev && \
    apt-get -y autoremove && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    pip install pipenv
