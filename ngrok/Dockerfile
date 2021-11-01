FROM alpine:latest

# download and install ngrok
RUN apk update && apk add wget unzip curl jq
RUN wget https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-amd64.zip 
RUN unzip ngrok-stable-* -d /bin && rm ngrok-stable-* && apk del wget unzip 

# input NGROK Authentication token here
RUN ngrok authtoken YOUR_NGROK_AUTH_TOKEN_HERE
COPY ./getaddress /bin/
RUN chmod +x /bin/getaddress
