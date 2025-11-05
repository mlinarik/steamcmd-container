FROM ubuntu:latest

RUN apt update -y && \
  apt install lib32gcc-s1 -y && \
  apt install libc6-dev -y && \
  apt install tmux screen -y && \
  apt install curl -y && \
  mkdir /gamedata

WORKDIR /gamedata

RUN curl -sqL "https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz" | tar zxvf -