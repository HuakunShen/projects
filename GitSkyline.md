---
title: Git Skyline
---


Website: https://git-skyline.huakun.tech/

GitHub: https://github.com/HuakunShen/git-skyline

<img src="https://hacker-storage.s3.us-east-2.amazonaws.com/2023/10/15/git-skyline-frontpage.png" width="100%" />

![](https://github.com/HuakunShen/git-skyline/raw/main/README.assets/git-skyline-demo.png)

This is a full-stack project trying to clone https://skyline.github.com/.

https://skyline.github.com/ is a cool feature of GitHub that shows your contribution graph in 3D but it stops working, and I decided to built my own version of it.

## Features

- Show GitHub contribution graph in 3D given any username
- I provide transparent background so that you can embed it in your website using iframe

Here is an example of embedding it in my website:

```html
<div class="h-[20em]">
  <iframe
    src="https://git-skyline.huakun.tech/contribution/github/huakunshen/embed?enableZoom=false&autoRotate=false"
    width="100%"
    height="500"
    frameborder="0"
  ></iframe>
</div>
```

<div class="h-[20em]">
    <iframe
        src="https://git-skyline.huakun.tech/contribution/github/HuakunShen"
        width="100%"
        height="500"
        frameborder="0"
    ></iframe>
</div>

<div class="h-[20em]">
    <iframe
        src="https://git-skyline.huakun.tech/contribution/github/huakunshen/embed?enableZoom=false&autoRotate=true"
        width="100%"
        height="500"
        frameborder="0"
    ></iframe>
</div>
