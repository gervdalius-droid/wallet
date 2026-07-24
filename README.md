# Cards

A tiny, offline-first web app for keeping your loyalty/reward cards on your phone and
showing their **barcode or QR code** at checkout — so you can leave the plastic at home.

No account, no server, no tracking. Your cards are stored **only in your browser**
(`localStorage`) and never leave your device.

## Features

- **Add cards** — name, number, color, and an emoji badge
- **Scan a physical card** with the camera to auto-fill the number and detect the barcode type
- **Every barcode format** via [bwip-js](https://github.com/metafloor/bwip-js): Code 128, QR,
  PDF417, Aztec, EAN-13, UPC-A, EAN-8, Code 39, ITF, Codabar, Data Matrix
- **Auto-detect** the right format from the number
- **Full-screen, high-contrast display** built for fast scanning at the register
- **Backup & restore** as a JSON file so you never lose your cards
- **Installable** — "Add to Home Screen" on iPhone/Android; works fully **offline**

## Use it on your phone

1. Open the hosted page in Safari (iPhone) or Chrome (Android).
2. Tap **Share → Add to Home Screen**.
3. Launch it from your home screen like a native app.

## Deep links

- `#add` — jump straight to the *new card* screen (handy for a home-screen shortcut)
- `#show=<cardId>` — open a specific card's barcode

## Run locally

```bash
python3 -m http.server 8750
# then open http://localhost:8750
```

Camera scanning requires `https://` or `localhost` (browser security rule).

## Roadmap

- **Real Apple Wallet passes** (`.pkpass`) — requires an Apple Developer certificate to sign
  the passes; the generation pipeline is planned as a follow-up.

## Tech

Single-page vanilla JS. No build step. Libraries are vendored in `lib/` so the app works offline.
