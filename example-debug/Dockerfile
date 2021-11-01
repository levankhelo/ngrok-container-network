FROM ubuntu:latest
RUN apt-get update && apt-get install -y dnsutils net-tools nmap wget curl
RUN touch /tmp/log && chmod a+r /tmp/log
COPY scan /bin/scan
RUN chmod a+x /bin/scan