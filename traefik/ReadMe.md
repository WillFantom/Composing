# Træfik

Secure reverse proxy / load-balancer. This is used as an ingress to access all services.

To learn more about træfik, read the docs [here](https://docs.traefik.io).

Some basic træfik middlewares are also included for: hsts, basic-auth, forward-auth (google oauth), rate limiting and ssl redirection.

All the middlewares stated above will work with little to no configuration steps required. However, forward auth will require some steps to be taken.

To use, ensure you have created the external `docker network create traefik-network`!

## TLS

There are 2 options for TLS provided in this compose file: TLS Challenge and DNS Challenge. If you plan to use a mix of both for any reason, ensure that the email address that you use for both are the same.

Use the certificate resolver `tlsc` to use the TLS Challenge.

Use the certificate resolver `cfdns` to use the DNS Challenge. This uses Cloudflare as I find it good to use for hosting my services. If you prefer an alternative DNS provider, this compose file can be easily adapted to use others. See the træfik docs for a full list of supported DNS provides that work with the DNS Challenge.

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- CERT_DIR - The path to store TLS certs for your domain and sub-domains
- RULES_DIR - The path to the directory where file rules can be stored. This allows you to add non-docker services to your traefik reverse proxy
- LOGS_DIR - The path to the directory where traefik will store its logs (can be in /tmp)
- CF_API_EMAIL - The email address of your cloudflare account
- CF_API_KEY - Your global cloudflare API key
- USERNAME - A username for use with basic auth
- HASHEDPASS - A hashed password for use with basic auth (can use a .htpasswd gen)
- ALLOWED_SUBNETS - A list of subnets that your inner serves should be accessible from (not used by default)
- WHITELISTED_EMAILS - Email address of google accounts that can access your server through sso (use with forward auth)
- AUTH_ID - Your google oauth ID
- AUTH_SECRET - Your google oauth secret
- RANDOM_SECRET - A random string that you create

DOMAIN - your FQDN