FROM python:3.8.3-slim
USER root
RUN apt update && \
    apt -y upgrade && \
    apt -y install git curl vim && \
    #curl \
    #vim && \
    apt-get clean && \
    apt-get autoremove && \
	mkdir /home/python/ && \
    groupadd -g 1000060000 python && \
    useradd -u 1000 -g python -d /home/python -s /bin/bash python && \
    chown -R python:python /home/python
ADD oc /usr/local/bin/
ADD helm /usr/local/bin/
COPY requirements.txt requirements.txt
WORKDIR /home/python
USER 1000
CMD tail -f /dev/null
