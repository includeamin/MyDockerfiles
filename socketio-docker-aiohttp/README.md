# Create Dockerfile based on this BaseImage

## build and push
``` sh
sudo docker build -t includeamin/socket_io_aiohttp:v1 .
sudo push includeamin/socket_io_aiohttp:v1
```


## Sample 
``` Dockerfile
FROM includeamin/socket_io_aiohttp:v1
EXPOSE 8001
COPY . app
WORKDIR app
CMD ["gunicorn", "server:app", "--bind"," 0.0.0.0:8001", "--worker-class","aiohttp.GunicornWebWorker"]

```
