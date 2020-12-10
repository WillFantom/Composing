# Monitoring [per-node]

This stack of services is intended to be run on ever host that you have. E.g. if you have a home machine and a VPS, this should be run on both as it will monitor only the host it is deployed on.
If you want a convenient way to see any collected data (graphs etc...), look at the other monitoring stack [here](../frontend/README.md).

This monitoring stack uses the following services:
- Prometheus: A Time Series DataBase (TSDB) that scrapes services (polling) for data amd store it. It also provides an API to collect the metrics (what grafana uses).
- Alerts-Manager: Can send alerts based on rules setup in prometheus, allowing you to receive notifications when you need them.
- Node Exporter: Collects metrics from the host system (such as storage, cpu and memory) and provides them in a way where prometheus can 'scrape' them.
- CAdvisor: Collects metrics on containers (memory, cpu etc...) and provides them in a way where prometheus can 'scrape' them.

Of these services, only Prometheus should be exposed to the network, and should also have http basic auth if over `https`.

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- DOMAIN - Your FQDN
- PROMETHEUS_CONFIG_DIR - Path to where the prometheus config will be stored
  - Make sure to move your `prometheus.yml` and `alert.rules` to this directory
- PROMETHEUS_DATA_DIR - Path to where the prometheus data will be stored
- ALERT_MANAGER_CONFIG - Path to where the alert manager config will be stored
  - Make sure to move your alert manager config to here
