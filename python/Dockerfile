 
FROM ubuntu:latest as dev

RUN apt-get update && \
    apt-get install -y git build-essential zsh \
    libssl-dev libffi-dev \
    python3-dev python3-pip && \
    rm -rf /var/lib/apt/lists/*

RUN sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

WORKDIR /home
USER root
