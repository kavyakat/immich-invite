# immich-invite

A friendly single-page guide for inviting friends to a self-hosted [Immich](https://immich.app) instance over [Tailscale](https://tailscale.com).

**Live page:** https://kavyakat.github.io/immich-invite/

## What it does

When a friend opens the page, they:

1. See a polaroid-themed welcome with a quick explainer of Immich and Tailscale
2. Fill in their name and email
3. The page opens their email client with a pre-filled message to me requesting access
4. The rest of the guide unlocks, walking them through installing Tailscale, connecting, opening Immich, and creating an account

Their name + email are saved to `localStorage` so refreshes don't re-prompt.

## How I use it

1. Share `https://kavyakat.github.io/immich-invite/` with the friend
2. They submit the form → I get an email with their name + Tailscale email
3. I share my Immich device with them via the [Tailscale admin console](https://login.tailscale.com/admin/machines) → click the `...` menu on the device → **Share** → paste their email
4. They follow the rest of the guide

## Editing

It's a single self-contained `index.html` — no build step, no dependencies beyond two CDN scripts (Inter/Caveat fonts, canvas-confetti). Edit and push to deploy.

If the Tailscale IP or Immich port ever changes, update both occurrences of `100.79.182.10:2283` in `index.html`.

## Easter eggs

- Confetti on form submit
- Bigger confetti when clicking the Immich URL
- Konami code (↑↑↓↓←→←→BA) triggers party mode
