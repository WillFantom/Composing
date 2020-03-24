# Composing

Here you will find a selection of docker compose files that, for those wanting to get into self-hosting, might find useful.

This is a summary of docker-compose repos I have created in the past, along with a few new useful services and updates to existing services.

To use, you simply need `Docker`, `Docker-Compose`. It works best if can forward ports `443` and `80` in you router to your server device and have a domain that uses CloudFlare DNS (other provides are normally still easy to change to with træfik).

## Services

Each service has a short description in their directory. Below is a list of all services, existing here now, and to exist here in the near future.

- [X] Ingress Service (træfik)
- [ ] Container Manager (portainer)
- [ ] Blogging Platform (ghost - works well with Ulysses Note Editor)
- [ ] Notification Platform (gotify)
- [ ] Torrent Downloader (transmission)
- [ ] Usenet Downloader (sabnzbd)
- [ ] TV Show Download Automator (sonarr)
- [ ] Film Download Automator (radarr)
- [ ] Music Download Automator (lidarr)
- [ ] Transcoder (tdarr)
- [ ] Media Server (plex... for now)
- [ ] Media Server Monitor (tautulli)
- [ ] Media Server Manager (organizr v2)
- [ ] Media Request Manager (ombi)
- [ ] Container Monitor (cadvisor)
- [ ] Node Monitor (prom node monitor)
- [ ] Time Series DB (prometheus)
- [ ] Stats Graph Tool (grafana)
- [ ] Dashboard (coming soon....!)
- [ ] Self Hosted Git (gitea)
- [ ] Self Hosted Cloud (nextcloud)