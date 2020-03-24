# Træfik

Secure reverse proxy / load-balancer. This is used as an ingress to access all services.

To learn more about træfik, read the docs [here](https://docs.traefik.io).

Some basic træfik middlewares are also included for: hsts, basic-auth, forward-auth (google oauth), rate limiting and ssl redirection.

All the middlewares stated above will work with little to no configuration steps required. However, forward auth will require some steps to be taken.

To use, ensure you have created the external `docker network create traefik-network`!