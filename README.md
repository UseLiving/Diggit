# Diggits

**The more Diggits you hold, the more BTC they dig for you.**

Hold $DIGIT and you get a crew of tiny pixel miner bots: one Diggit for every 250,000 $DIGIT, up to 80. Creator fees from $DIGIT trading rent Bitcoin hashrate, and whatever it mines lands in a public BTC vault that's shared with holders in proportion to their $DIGIT.

## What's in here

- `index.html` — the whole site in one file. Host it anywhere static (GitHub Pages: Settings → Pages → deploy from `main`).
- `assets/` — logo (SVG + transparent PNG), 1000×1000 profile picture and the Twitter header. The SVG is also the favicon.

## Wallet connect

The **Connect wallet** buttons work with Phantom, Solflare and Backpack (desktop extensions and in-app mobile browsers). Connecting is read-only: the site asks only for the public address, never a signature.

It works once the site is hosted over https (GitHub Pages is fine). Wallet extensions don't connect to a file opened straight from your computer, or inside the Claude preview.

Balances are read in the browser with no API key: the site works out the holder's token account address and reads it from the public `solana-rpc.publicnode.com` endpoint, falling back to `api.mainnet-beta.solana.com`. Visitors can also look up any address without connecting.

**At launch:** open `index.html`, find `const CONFIG=` and paste the $DIGIT mint address into `DIGIT_MINT`. That hides the test field and every connected wallet shows its real crew. Until then, the "Token to read" field lets you test with any token mint (for example USDC, `EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v`). For heavy traffic, put your own RPC (Helius, QuickNode) first in `RPCS`.

## What the site does

- **The mine:** animated pixel cross-section, one crew per holder (demo crews until launch). Hover a crew for its tier and share.
- **My crew:** type a holding to see your crew digging, its tier, your share, and estimated sats per day.
- **Crew tiers:** Prospector → Dig crew → Shaft team → Tunnel gang → Quarry → Deep mine → Motherlode.
- **Dig calculator:** holding, daily volume, fee rate, hashrate efficiency and BTC price in; sats per day and BTC per 30 days out, with the formula shown.
- **Deepest crews, transparency notes and token section.**

## Not live

$DIGIT isn't launched. The mine shows demo crews, the vault reads 0 BTC, and every BTC figure is a hypothetical estimate, not a promise. Renting hashrate typically returns somewhat less than it costs and output varies with network difficulty. Not financial advice.
