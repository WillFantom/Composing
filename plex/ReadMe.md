# Plex Media Server

A pretty decent media server with tonnes of features. However, due to a few reasons, such as the use of sqlite, this might change soon...

Tautulli is also included for stats collection.

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- DOMAIN - Your FQDN
- PUID - Your user ID (run the command `id`)
- PGID - The ID of the docker group (can also be found via `id`)
- TZ - Your timezone (e.g. `Europe/London`)
- PLEX_DIR - The dir where you will store your plex data
- MEDIA_DATA - The dir where you media collection is
- TRANSCODE_DIR - The dir where to store tmp transcode files

## Claiming

When running for the first time, get a plex claim token for your plex account from [here](https://www.plex.tv/claim/).

Then run the following command:

```bash
export PLEX_CLAIM=<your-token-here>
```

## Transcoding

I suggest making `TRANSCODE_DIR` a directory on a RAM disk for better performance and less writes to an SSD!
