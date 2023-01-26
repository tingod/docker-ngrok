# DOCKER NGROK IMAGE

## BUILD IMAGE

```linux
git clone https://github.com/tingod/docker-ngrok.git
cd docker-ngrok
docker build -t tingod/ngrok .
```

## RUN
* you must mount your folder (E.g `/data/ngrok`) to container `/myfiles`
* if it is the first run, it will generate the binaries file and CA in your floder `/data/ngrok`

```linux
docker run -idt --name ngrok-server \
-v /data/ngrok:/myfiles \
-e DOMAIN='n.v2c.cc' tingod/ngrok /bin/sh /server.sh
```
