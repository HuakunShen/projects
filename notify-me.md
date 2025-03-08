---
title: Notify Me
tags: [Nuxt, Vue, Tailwind, TypeScript, Netlify, Notion, Telegram, Email]
---

# Notify Me

GitHub: https://github.com/HuakunShen/Notify-Me

This project is for sending notification to oneself.

Seems like a boring useless tool, but I can find some use cases.

The web app has a frontend and backend both written with Nuxt 3.

The frontend is only for development and demo purpose. The useful part is the API.

The API allows you to send message to yourself with both GET and POST requests. With GET request support you can send the message within browser.

The notion integration not only allows you to send message to yourself, but also record the messages in a database.

Think about when you need to send message to yourself using an API.

## Use Cases

### Send Automatic Message to Yourself

1. A monitor app or CRON job can send automatic notification to yourself.
2. Automatic script such as [Wifi Password Thief](https://github.com/HuakunShen/rubber-ducky-toolbox).
3. Web Cralwer Notification.
4. Transfer message from one device to another using only Browser Address Bar.

### Upload to Notion or Database

1. "Leave a Message" or "Contact Form" information can be uploaded to Notion Database (for free).

## Supported Platforms

- [x] Email
- [x] Telegram
- [x] Notion
- [ ] Slack
- [ ] Discord

## Example

<img src="https://hacker-storage.s3.us-east-2.amazonaws.com/2023/10/15/e71c1422-32d7-47fa-86bd-62a838164c55.png" width="100%" />

## Tech Stack

- Netlify
- Nuxt
- Daisyui
- Tailwind CSS
- TypeScript
- Vue
