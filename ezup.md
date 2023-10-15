---
title: EzUp
tags: [SvelteKit, Svelte, Rust]
---

# EzUp

> A quick file/image uploaded built with Tauri (Rust + SvelteKit)

- Main purpose: a imagebed client, I use it for writing blog and notes in Markdown
  - I take screenshot all the time, saving screenshots as files and moving them is too time consuming, and takes lots of space in git repo.
  - Images from other website can also to uploaded to my own imagebed as a mirror, in case original images were removed, then references on my website will expire too.
- [GitHub](https://github.com/huakunshen/ezup)
- I you have a image file path, screnshot in your clipboard, or a image url, you can upload it to your imagebed with a keyboard hotkey.

<div>
  <img
    src="https://hacker-storage.s3.us-east-2.amazonaws.com/2023/1/16/8b5952f9-0e2b-4eab-b994-29916911cd0f.png"
    width="60%"
  />
  <img
    src="https://hacker-storage.s3.us-east-2.amazonaws.com/2023/1/16/d84046a6-b213-4635-ac56-c649399f16df.png"
    width="60%"
  />
  <img
    src="https://hacker-storage.s3.us-east-2.amazonaws.com/2023/1/16/8e044453-2dfc-4f43-be28-e2666f33e5d0.png"
    width="60%"
  />
</div>

## Tech Stack

- [Tauri](https://tauri.studio/en/)
  - Rust + SvelteKit
  - Tauri is a framework for building tiny, blazing fast binaries for all major desktop platforms. Developers can integrate any front-end framework that compiles to HTML, JS and CSS for building their user interface. The backend of the application is a rust-sourced binary with an API that the front-end can interact with.
- [SvelteKit](https://kit.svelte.dev/)
  - SvelteKit is a framework for building web applications of all sizes, with a beautiful development experience and flexible filesystem-based routing.
- [TailwindCSS](https://tailwindcss.com/)
  - A utility-first CSS framework for rapidly building custom designs.
- [Flowbite](https://flowbite-svelte.com/)
