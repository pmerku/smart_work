FROM ubuntu:latest as dev

RUN apt-get update -y && \
    apt-get install -y git build-essential curl zsh \
    clang nasm \
    make zlib1g-dev && \
    rm -rf /var/lib/apt/lists/*

RUN sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

WORKDIR /home
USER root

################ NEW IMAGE ######################

FROM ubuntu:latest as debug

RUN apt-get update -y && \
    apt-get install -y git build-essential curl zsh \
    clang nasm \
    lldb valgrind strace ltrace \
    make zlib1g-dev && \
    rm -rf /var/lib/apt/lists/*

RUN sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

WORKDIR /home
USER root