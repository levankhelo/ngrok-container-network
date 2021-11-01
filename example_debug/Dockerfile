FROM ubuntu:latest
RUN apt-get update
RUN apt-get install -y dnstools net-tools wget curl
RUN touch /tmp/log && chmod a+r /tmp/log
COPY scan /bin/