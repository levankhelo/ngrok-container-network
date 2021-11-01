# ngrok-container-network
## About
system where you can easily host your containerized application using ngrok and docker-compose

## How to make it work for you case:  
Modify `ngrok/Dockerfile` and input your authorization token retrieved from [ngrok.com](ngrok.com)  
### ngrok/Dockerfile
* change auth token    

### docker-compose.yaml
* replace `golang-server:8090` everywhere with `container_name` and `:port` of your application with `container_name:port`
* replace example-server with your server container
  * make sure you expose server port
  * make sure you name container using `container_name` field
* ngrok service
  * in command field, change `golang-server:8090` with `my_container_name:PORT`. for example: `flaskserver:5000`,  `djangoserver:8000` or `myExpress:3000`  


> note: if you are going to change something in this example's golang script, make sure you run `docker compose up --build` or `docker-compose up --build` to rebuild go script