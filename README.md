# WG Manager demo

A live demo of the [WG Manager](https://github.com/elmedico27/wgmanager) web interface.

**Try it:** https://wgmanager-demo.pages.dev

- Any password signs you in.
- Add, delete, enable and disable clients all "work". 
- QR codes and downloaded configs contain random keys and a placeholder endpoint `vpn.example.com`.
- No backend server.  Your changes stay in your browser tab; closing the tab resets the demo.

To run WG Manager on your own PiVPN server, see the [main repository](https://github.com/elmedico27/wgmanager).

## Build

```
npm ci
npm run build:demo
```

## License

GPL-3.0, the same as WG Manager. See [LICENSE](LICENSE).
