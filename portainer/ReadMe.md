# Portainer

A web service for managing containers. Useful for viewing container logs remotely.

**You should be using this with the Træfik service!** 

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- DOMAIN - Your FQDN
- PORTAINER_DATA - The path where you want your portainer data to be stored
