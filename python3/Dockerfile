FROM python:3.6
RUN set -x && \
    apt-get update && \
    apt-get install -y sudo && \
    useradd -G sudo -m -s /bin/bash kiyoshi && \
    gpasswd -a kiyoshi sudo && \
    mkdir -p /home/kiyoshi/my_python && \
    pip install requests==2.18.4 click==6.7

USER kiyoshi
WORKDIR /home/kiyoshi

