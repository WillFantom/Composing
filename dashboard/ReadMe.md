# Dashboard (SUI)

This compose file brings up a dashbard for your hosted apps.

SUI uses the docker socket and the traefik API to always populate your dashboard with the apps that you are running.

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- DOMAIN - Your FQDN

## Config

You must also edit the config file at `./configs/traefik.json` and input your traefik URL (along with your traefik username and password if you have basic auth enabled on your traefik service)
