# RackForm

**Static GitHub Pages demo** of RackForm, a parametric roof-rack studio.

Open the app at:

https://thedevthatcantcode.github.io/RACKFORM/

This repository contains only the production HTML, CSS and JavaScript needed to run the demo.

The built-in templates, editing, BOM, bend list, welded crossbars, connectors and client-side CSV downloads work without a server.

## STEP import/export

STEP import/export requires the local FastAPI/OpenCascade service. Chrome blocks an HTTPS GitHub Pages site from calling `http://127.0.0.1` directly, so use a secure tunnel:

```bash
# from the RackForm project folder
./scripts/start-tunnel.sh
```

The script starts the local API, creates a Cloudflare quick tunnel, copies a ready-to-open link like this to the clipboard, and prints it:

```text
https://thedevthatcantcode.github.io/RACKFORM/?api=https://example.trycloudflare.com
```

Open that link and the app connects automatically. You can also paste the tunnel URL into **Connect local API**.

Keep the tunnel running while importing or exporting. The backend source is not published in this repository.
