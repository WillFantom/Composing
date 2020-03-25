# Gitea

Self hosted Git server. 

**You should be using this with the Træfik service!** 

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- DOMAIN - Your FQDN
- GITEA_DATA - The path where you want your gitea data to be stored
- SECRET - Global secret key
