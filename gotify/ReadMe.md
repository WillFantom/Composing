# Gotify

A notification service you can use a bit like PushBullet.

**You should be using this with the Træfik service!** 

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- DOMAIN - Your FQDN
- GOTIFY_DATA - The path where you want your gotify data to be stored
- USERNAME - The username for the admin account
- PASSWORD - The quoted password for the admin account (quotes are needed in most cases)
