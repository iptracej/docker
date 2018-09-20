FROM python:3.6
RUN set -x && \
    apt-get update && \
    apt-get install -y sudo && \
    useradd -G sudo -m -s /bin/bash kiyoshi && \
    gpasswd -a kiyoshi sudo && \
    mkdir -p /home/kiyoshi/scikit-learn && \
    pip install requests==2.18.4 click==6.7
ADD requirement.txt /home/kiyoshi/scikit-learn

USER kiyoshi
WORKDIR /home/kiyoshi/scikit-learn
RUN pip install -r requirement.txt --user


