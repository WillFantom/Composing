# Media Services

This compose file provides several media download automators:

- Sonarr: A service for automating TV downloads
- Radarr: A service for automating Movie downloads
- Lidarr: A service for automating Music downloads
- Ombi: A frontend to add content to the above services (can be used by N users)
- Tdarr (Intel QSV variant): A services for automating the transcoding process

An smtp server is also included to allow Ombi to send out notification mail. Also noteworthy here: Ombi can also send out notifications via the Gotify service.

Tdarr is provided here in an example that uses Intel QuickSync Video. QSV is excellent if you wish to convert a large library from h264 to h265(hevc) to save some storage space. There are other variants that can just use software transcoding or use an NVidia GPU.

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- DOMAIN - Your FQDN
- PUID - Your user ID (run the command `id`)
- PGID - The ID of the docker group (can also be found via `id`)
- TZ - Your timezone (e.g. `Europe/London`)
- SONARR_CNF - The dir where you will store your sonarr config and db
- RADARR_CNF - The dir where you will store your radarr config and db
- LIDARR_CNF - The dir where you will store your lidarr config and db
- OMBI_CNF - The dir where you will store your ombi config
- TDARR_DATA - The directory where Tdarr will store any application data
- TDARR_DB - The directory where Tdarr will store its database
- TRANSCODE_CACHE - The directory where any temp files for transcoding will be stored. To increase the lifespan of your disks/ssds, I suggest this directory being on a RAM Disk

- MEDIA_DATA - The dir where you media collection is
- DOWNLOADS_DIR - The dir where your completed download will be stored
