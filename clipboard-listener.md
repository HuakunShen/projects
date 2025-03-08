---
title: Clipboard Listener
---

# Clipboard Listener

NodeJS doesn't have package for reading clipboard image and listening to clipboard.

I created this package to solve this problem with a Golang package.

GitHub Repo: https://github.com/HuakunShen/general-clipboard-listener

GitHub Repo: https://github.com/CrossCopy/clipboard

> A Cross-Platform clipboard listener that listens for both text and image (screenshots).
> Designed for NodeJS, not for web.
> Provides API to read and write text/image from/to clipboard.

npm package: https://www.npmjs.com/package/@crosscopy/clipboard

## Tech Stack

- Golang
- NodeJS
- TypeScript

## Sample Usage

```ts
import clipboardEventListener from "@crosscopy/clipboard";

console.log(clipboard.readTextSync());
console.log(await clipboard.readText());
const imgBuf = clipboard.readImageSync();
// console.log(imgBuf.toString("base64"));
// console.log(clipboard.readImageBase64Sync());
// await clipboard.writeImage(base64img); // add fake image to clipboard
clipboard.writeImageSync(base64img); // add fake image to clipboard
console.log(""); // give some time
console.assert(clipboard.readImageBase64Sync() === base64img);

// * test readimage
clipboard.writeImageSync(base64img);
console.log();
console.assert((await clipboard.readImage()).toString("base64") === base64img);

await clipboard.writeImage(base64img);
console.log();
console.assert((await clipboard.readImageBase64()) === base64img);
clipboard.on("text", (text) => {
  console.log(text);
});
clipboard.on("image", (data) => {
  fs.writeFileSync("test.png", data);
});
clipboard.listen();
setTimeout(() => {
  clipboard.close();
}, 10000);
```
