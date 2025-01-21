# IP-Geo Cache DB

**GitHub:** https://github.com/HuakunShen/ip-geo-cache-pb

This is a IP to geolocation lookup server with cache. Written in Golang and Pocketbase.

> This is a small project I created as a helper for my other project https://github.com/kunkunsh/kunkun
> If you want to deploy it, you can build a docker image and run it on a server. e.g. fly.io, railway.app
> Since it's a cache server, it requires storage attached. 

IP info APIs costs money. e.g. ipgeolocation.io has a free tier of 30k requests/month

It's hard to request 30k unique ips in a month, but if the same ip address is checked frequently the free quota could be used up quickly. Thus I built this simple cache server. This cache server is used as a proxy server, requests sent to `/api/<:ip>` is forwarded to API service and cached in pocketbase.

```bash
make build # build docker image
make run # run docker image on port 8090
```
