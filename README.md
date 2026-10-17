# RaZdai Apps for umbrelOS

This community app store currently packages [Journiv](https://github.com/journiv/journiv-app), a self-hosted journaling application.

## Add this store to umbrelOS

1. Open the umbrelOS App Store.
2. Open the menu in the top-right and choose **Community App Stores**.
3. Add this repository URL: `https://github.com/RaZdai/umbrel-journiv-store`.
4. Return to the App Store, find **Journiv**, and install it.

## Journiv deployment notes

- Uses the upstream `swalabtech/journiv-app:latest` image.
- Uses SQLite for the journal database and Valkey for caching and background jobs.
- Journiv's app data, media, and generated signing key are kept in Umbrel's app-data directory, not in this repository.
- The app opts into Journiv's documented insecure-cookie-over-HTTP setting for use behind umbrelOS's local HTTP app proxy. Do not expose this app directly to the public internet over plain HTTP. For remote access, use a properly configured HTTPS route.
- Journiv is beta software. Back up its app-data directory regularly and before updates.

This is a community-maintained package, not an official Journiv or Umbrel release.
