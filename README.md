# DiddyDiffusion

A tiny browser image playground powered by [Pollinations](https://pollinations.ai) and its Bring Your Own Pollen (BYOP) flow.

## What it does

- Connects a visitor's Pollinations account through the BYOP authorize flow.
- Requests only a small, short-lived user-approved budget.
- Generates images with Pollinations' `flux` model.
- Stores the user-authorized key only in `sessionStorage`.
- Contains no developer secret key.

## Live app

https://raw.githack.com/umm-dev/DiddyDiffusion/main/index.html

## Pollinations integration

The app uses a publishable Pollinations App Key (`pk_...`) as its `client_id`. Visitors authorize their own temporary `sk_...` key, which is then used only for their image-generation requests. Pollinations is visibly credited in the UI.

The redirect URI registered on the App Key must exactly match:

```text
https://raw.githack.com/umm-dev/DiddyDiffusion/main/index.html
```

## Files

- `index.html` — zero-build static web app.
- `config.js` — public Pollinations App Key only; never put a secret `sk_...` key here.

## License

MIT
