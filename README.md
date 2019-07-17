# cloudflare-dns-proxy
Cloud flare dns proxy (dns over https) docker image

Dockerfile to build dns-over-https service using cloudflare binary, and dns services.

Example docker-compose file:
```yaml
version: "3.7"

services:
  cloudflared:
    container_name: cloudflared
    image: jordanst3wart/cloudflare-dns-proxy:latest
    ports:
      - "53:53/tcp"
    restart: unless-stopped
``` 


I would like to use the raw binary in the future, create a user to run cloudflare, pull images by the hash.


Original setup instructions are here:
https://developers.cloudflare.com/1.1.1.1/dns-over-https/cloudflared-proxy/
   