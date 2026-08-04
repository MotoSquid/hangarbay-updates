# Hangar Bay Catalog OTA Updates

This repository is the static hosting source for Hangar Bay catalog OTA updates.
It currently contains only the publishing scaffold; **do not publish a real
catalog release yet.**

## Layout

- `stable/latest.json` points stable clients to the current stable release.
- `developer/latest.json` points developer clients to the current developer
  release.
- `releases/` contains versioned release directories.

Both channel pointers are disabled placeholders until the first catalog release
is ready.

## Publishing rules

1. Release directories are immutable after publication. Publish corrections as
   a new release instead of changing an existing release directory.
2. Upload all pack files, `manifest.json`, and `manifest.sig` before updating a
   channel pointer.
3. Publish `latest.json` last, after every release artifact is available.
4. Never commit Android keystores, OTA private keys, passwords, credentials,
   `local.properties`, or `.env` files.
5. Do not publish a real catalog release yet.
