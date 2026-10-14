# CLOB

The launchpad for order book exchanges on Solana. Launch a coin. Own the market.

Static site: one `index.html` plus images. No build step.

## Files

- `index.html`: the whole site (HTML, CSS, JS)
- `logo.png`, `mark.png`, `favicon.png`: logo assets
- `vercel.json`: Vercel config

## Deploy on Vercel

1. Push these files to the root of a GitHub repo.
2. In Vercel, click **Add New > Project** and import the repo.
3. Framework preset: **Other**. Leave build command and output directory empty.
4. Click **Deploy**.

## Run locally

```
npx serve .
```

## Notes

- The demo terminal and the 3D depth chart (three.js r128, cdnjs) run on a simulated market. No real orders or funds.
- Wallet connect uses `@solana/web3.js` 1.95.3 (jsDelivr): Phantom, Solflare, Backpack.
- The SOL balance uses the public mainnet RPC, which often blocks browser requests. Replace `web3.clusterApiUrl("mainnet-beta")` in `index.html` with your own RPC URL.
- The Live markets section shows an empty state until launches open.
