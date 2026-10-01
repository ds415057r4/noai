```bash
docker build . -t noai/go-http:1.0.0
docker run --rm --detach --publish 8080:8080 --name=go-http noai/go-http:1.0.0
curl -v http://localhost:8080
docker stop go-http
```
