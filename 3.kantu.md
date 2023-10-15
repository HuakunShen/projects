---
title: Kantu
tags: [AI, ML, Nuxt, Tauri, Vue]
---

# Kantu

GitHub: https://github.com/HuakunShen/kantu

<div class="grid grid-cols-2 gap-4">
<img src="https://hacker-storage.s3.us-east-2.amazonaws.com/2023/10/15/fc0408eb-53f6-43fb-be55-71f3f928d4e3.png" width="100%" />

<img src="https://hacker-storage.s3.us-east-2.amazonaws.com/2023/10/15/e624d921-0409-48b3-9c8e-b04235942d26.png" width="100%" />
</div>

Deployment:

- https://kantu.huakun.tech/
- https://kantu.vercel.app/

Kantu is a image browser with some cool features I implemented for my other machine learning projects.

It is mainly a desktop application built with [Tauri](https://tauri.app/) and [Nuxt](https://nuxt.com/). I also built a web version with [Nuxt](https://nuxt.com/) with limited features.

## Features

- Image Browser
  - Browse images in a given folder on desktop
- Image labelling, you can label images with keyboard
  - I am too lasy to label images using mouse, so I implemented this feature which allows me to label images using keyboard. When I press the keyboard arrow keys, the images will be swiped left and right.
  - After labelling, the labels will be saved in a json file in the same folder.
- Image slideshow, you can play a slideshow of images in a given folder

## Supported Platforms

- Windows, Mac, Linux
- Web

## Plan to Support

- iOS, Android

## Tech Stack

- [Tauri](https://tauri.app/)
- [Nuxt](https://nuxt.com/)
- [Vue](https://vuejs.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Vite](https://vitejs.dev/)
- [TypeScript](https://www.typescriptlang.org/)
- [Node.js](https://nodejs.org/en/)