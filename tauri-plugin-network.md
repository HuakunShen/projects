---
title: Tauri Plugin Network
tags: [Rust, Tauri, TypeScript, Network, SvelteKit, Desktop]
---

# Tauri Plugin Network

> A tauri plugin written in Rust and TypeScript to provide network related functionalities to a tauri desktop app.

https://github.com/HuakunShen/tauri-plugin-network

Added to [awesome-tauri](https://github.com/tauri-apps/awesome-tauri)

## Features

- Retrieve network interface information
- TCP host up detection
- Scan local network ips on specified port using HTTP
  - With optional response keyword detection
  - Batch scanning with multi-threading
- ICMP scan
- Network data transmission monitoring
- Packet sniffing (This is harder on Windows as [pnet](https://crates.io/crates/pnet) on Windows requires installation of WinPcap or npcap)

## Example

<img src="https://hacker-storage.s3.us-east-2.amazonaws.com/2023/10/15/f54f0db4-f540-4ede-bde2-2e70468c01cd.png" width="100%" />

<img src="https://hacker-storage.s3.us-east-2.amazonaws.com/2023/10/15/50f03ac2-8972-4942-a1ba-a759647afd9e.png" width="100%" />

## Tech Stack

- Rust
- Tauri
- TypeScript
- Network
- SvelteKit
