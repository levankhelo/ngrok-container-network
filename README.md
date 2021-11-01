# ngrok-container-network

Modify `ngrok/Dockerfile` and input your authorization token retrieved from [ngrok.com](ngrok.com)  

## How to make it work for you case:  
### ngrok/Dockerfile
* change auth token    

### docker-compose.yaml
* replace `golang-server:8090` everywhere with `container_name` and `:port` of your application with `container_name:port`
* replace example-server with your server container
  * make sure you expose server port
  * make sure you name container using `container_name` field
* ngrok service
  * in command field, change `golang-server:8090` with `my_container_name:PORT`. for example: `flaskserver:5000`,  `djangoserver:8000` or `myExpress:3000`  