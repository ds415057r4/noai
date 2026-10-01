```bash
docker build . --tag noai/hello-nginx:1.0.0
docker images
docker run --rm --detach --publish 80:80 --name hello-nginx noai/hello-nginx:1.0.0
curl -v http://localhost:80
```
