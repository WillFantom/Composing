# Gitea

Self hosted Git server. 

**You should be using this with the Træfik service!** 

## Warning

You should uncomment the environmental vars in the compose file after you have completed the web based setup of this service! (You should also restart the service after un-commenting the lines in the file)

Also, the env var for `DISABLE_REGISTRATION` does not seem to work, thus you must edit the generated config file in the container to set this option.

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- DOMAIN - Your FQDN
- GITEA_DATA - The path where you want your gitea data to be stored
- SECRET - Global secret key
