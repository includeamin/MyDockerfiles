SRS V4 Dockerfile

## Build
default config is for WebRTC.

```bash
docker build -t srs:v4 .
```

## RUN
`CANDIDATE` should change to your IP or Domain address.
```bash
sudo docker run -p 1935:1935 -p 8080:8080 -p 1985:1985 -p 8000:8000/udp --env CANDIDATE=192.168.1.65    srs:v4
```

## Note:
you can change the config in `Dockerfile` with changin of `CMD` command in it. for example: `#CMD ./objs/srs -c conf/full.conf`
