# DOCKER NGROK IMAGE

## BUILD IMAGE

```linux
git clone https://github.com/hteen/docker-ngrok.git
cd docker-ngrok
docker build -t ngrok_server_image .
```

## RUN
* you must mount your folder (E.g `./data`) to container `/myfiles`
* if it is the first run, it will generate the binaries file and CA in your floder `./data`

# tunnel.baidu.com 是你的代理域名
```linux
docker run -idt --name ngrok-server \
-v ./data:/myfiles \
-e DOMAIN='ingrok.****.com' ngrok_server_image /bin/sh /server.sh
```
