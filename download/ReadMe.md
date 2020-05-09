# Download

Downloader services that can be used with the automators in [media](/media)

- Sabnzbd for usenet
- Transmission for torrents

- Hydra for collating usenet indexer searches

**You should be using this with the Træfik service!** 

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- DOMAIN - Your FQDN
- COMPLETED_DOWNLOADS - Where completed downloads are store
- INCOMPLETE_DOWNLOADS - Where incomplete downloads are stored
- NZBS - The dir where nzb files to be use by sab are stored
- TORRENTS - The dir where torrent files to be used by transmission are stored
- HYDRA_CNF - The dir where hydra's config will be stored
- SAB_CNF - The dir where sab's config will be stored
- TRANSMISSION_CNF - The dir where transmission's config will be stored
- VPNPROVIDER - Your VPN provider (e.g. mullvad)
- VPNEMAIL - Your VPN username/email
- VPNPASSWORD - Your VPN password
- LOCAL_SUBNET - Your local address range (e.g. 10.0.30.0/24)
- TRANSMISSIONUSERNAME - The username you wish to use to access transmission
- TRANSMISSIONPASSWORD - The password you wish to use to access transmission