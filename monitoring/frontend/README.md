# Monitoring [frontend]

This is to act as a frontend to your monitoring. You can connect Grafana to N Prometheus instances, so I suggest only running this on a single host, and connecting your N Prometheus services to it.

This monitoring stack uses the following service:
- Grafana: Used for as a front-end for monitoring data. Basically, makes pretty graphs

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- DOMAIN - Your FQDN
- GRAFANA_DATA_DIR - Path to where grafana data will be stored
- GRAFANA_PLUGINS - Comma seperated list of grafana plugins to be installed
