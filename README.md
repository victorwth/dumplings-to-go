# Dumplings To Go

Responsive restaurant website for Dumplings To Go in Sunrise, Florida.

## Run locally

Requires Node.js. No dependencies or build step.

```sh
node server.cjs
```

Open http://localhost:3000.

## Files

- `index.html`: complete website, styles, and local-time hours display.
- `server.cjs`: HTTP server (localhost by default; configurable HOST and PORT).

Fonts load from Google Fonts; illustrative food photography loads from Unsplash. Replace illustrative photos with approved restaurant photography before a production launch. Confirm menu details, business hours and contact information with the restaurant.

## Docker deployment

From the repository root:

```sh
docker build -t dumplings-to-go .
docker run --rm -p 3000:3000 dumplings-to-go
```

Set the deployment build context to the repository root and Dockerfile path to `Dockerfile`. The container listens on `0.0.0.0:3000` by default and honors the `PORT` environment variable. No install or build command is required.
