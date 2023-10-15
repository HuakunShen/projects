---
title: Web Request Viewer
---

# Web Request Viewer

> Send a request to this server and it tells what your request look like.

## Use cases

It's hard to know the exact information of a request sent out from your code. The best and eaiset way is of course have a real server listening to your requests and reply with what information they can see from your request.

For example, if you are writing a web scrapying bot and you want to change your user-agent to hide this bot, how can you make sure the request sent indeed hides your user-agent?

Or if request headers contains any information that could leak your identity.

What about you are using a VPN and you are unsure whether the VPN indeed hides your IP. You can send to request to this server and check the IP this server sees.

### VPN

Some VPN protocols like shadowsocks work in layer 4 (transport layer) in the 7-layer OSI model, some work in layer 3 (network layer). It feels the same in browsers.

<img src="https://hacker-storage.s3.us-east-2.amazonaws.com/2023/10/15/osi_model_7_layers.png" width="100%" />

If you use terminal (`curl` command or `git`), VPNs like OpenVPN automatically handles the traffic for you. While VPNs using shadowsocks requires extra http/socks proxy configuration.

If you are a hacker/pentester, how can you verify whether you hide your identity behind VPN successfully? Simply send a request to the request viewer server and compare with your real ip. It also returns the intermmediate routers' ip.

## Features

- `/online`: check if the server is online
- `/headers`: return all headers in the request
- `/ip`: return the ip of the request, including intermediate routers
- `/user-agent`: return the user-agent of the request
- `/cookies`: return the cookies of the request
- `/time`: return the time of the request

<img src="https://hacker-storage.s3.us-east-2.amazonaws.com/2023/10/15/carbon.png" width="100%" />