# WG Manager demo

A live demo of the [WG Manager](https://github.com/elmedico27/wgmanager) web interface. It runs entirely in your browser with made-up data and is not connected to any server.

**Try it:** https://wgmanager-demo.pages.dev

- Any password signs you in.
- Add, delete, enable and disable clients. QR codes and downloaded configs contain random keys and the placeholder address `vpn.example.com`, so they connect to nothing.
- Your changes stay in your browser tab. A refresh keeps them, closing the tab resets the demo, and nobody else sees them.

To run WG Manager on your own PiVPN server, see the [main repository](https://github.com/elmedico27/wgmanager).

## How this repository is made

Everything here except this README, `LICENSE`, `.gitattributes` and `.nvmrc` is a copy of `web/` from the main repository. Make changes there, not here, then copy again. The demo-only behaviour (no Preview panel, the demo notice, keeping changes per tab) lives in the main repository behind `npm run build:demo`.

Copied from [`elmedico27/wgmanager@4e49da9`](https://github.com/elmedico27/wgmanager/commit/4e49da972bacb0a6b1086d669acbe3b283b704c3) (Add browser-isolated public demo build).

## Build

```
npm ci
npm run build:demo
```

The site is written to `dist-demo/`. Cloudflare Pages builds it on every push with build command `npm run build:demo`, output directory `dist-demo`, and the Node.js version from `.nvmrc`.

There is deliberately no `404.html`: without one, Cloudflare Pages serves `index.html` for every address, so links like `/clients/Alice_Phone` work on refresh.

## License

GPL-3.0, the same as WG Manager. See [LICENSE](LICENSE).
