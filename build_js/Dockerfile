FROM awlodarkiewicz/devops:base

# Yarn
RUN apt-get update && \
    apt-get -qq -y --no-install-recommends install \
        gpg-agent nodejs npm && \
    curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
    apt-get update && \
    apt-get -qq -y --no-install-recommends install \
        yarn && \
    apt-get -y autoremove && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
