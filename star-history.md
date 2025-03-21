---
title: Star History
---

GitHub: https://github.com/HuakunShen/star-history

This is a simple tool to show the star history of any GitHub repository.

PocketBase is used for caching.

## Usage

Send a `GET` request to `https://star-history.pockethost.io/api/star-history/<username>/<repo>`

e.g. `https://star-history.pockethost.io/api/star-history/kunkunsh/kunkun`

If you request a repo with lots of stars (e.g. 80k stars), it may take a while to get the result if it's the first time the repo is requested.

You could get timeout error if the request takes too long, but the request is still being processed. Come back in a few minutes and try again.

After the first request, the result will be cached and the next request will be instant.

The GitHub Token can only send 5000 requests per hour. If it reaches the limit, the request will fail.
You can add your own GitHub Token with `github_token` query parameter. Append `?github_token=<your_token>` to the URL.
