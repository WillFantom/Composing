# Watchtower

Watchtower will ensure all the containers running (and are visible over the local docker socket) are updated.

This uses the default check interval of 5mins.

**You should be using this with the [Gotify](/gotify/ReadMe.md) service!** 

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- TZ - Your Timezone
- GOTIFY_DOMAIN - The url (including schema (e.g. `https://`)) of your Gotify instance
- GOTIFY_TOKEN - The application token of a created Gotify application
