# Ghost CMS (blogging platform)

Ghost CMS for a blog.

To learn more about Ghost CMS, check out their [site](https://ghost.org).

**You should be using this with the Træfik service!**

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- DOMAIN - Your FQDN
- GHOST_DB_PASSWORD - The password for your database
  - This should be secure, but don't worry too much, as this db is not exposed fully to the web
- GHOST_APPS - Directory for your ghost apps
- GHOST_DATA - Directory for your ghost data
- GHOST_IMGS - Directory for your ghost images
- GHOST_THEMES - Directory for your ghost themes
- GHOST_DB_DATA - Directory for your ghost database