# Party Parrot

Displays an animated parrt when the URL is cURLd.

`curl https://parrot.example.tld`

This will do the same as `curl parrot.live`, but just self-hosted. Although a little bit pointless for many, it can act as quite a nice landing page, simply redirecting back to a site such as `duck duck go` when seen via a browser, yet showing the party parrot when curld.


**You should be using this with the Træfik service!** 

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- DOMAIN - Your FQDN
- REDIRECT - The URL to direct a client to if they connect via a web browser (not cURL)
