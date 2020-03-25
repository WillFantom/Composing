# Monitoring

This monitoring stack uses the flowwoing services:
- Grafana: Used for as a front-end for monitoring data. Basically, makes pretty graphs!
- Prometheus: A Time Series DataBase (TSDB) that scrapes services (polling) for data amd store it. It also provides an API to collect the metrics (what grafana uses).
- Alerts-Manager: Can send alerts based on rules setup in prometheus, allowing you to receive notifications when you need them.
- Node Exporter: Collects metrics from the host system (such as storage, cpu and memory) and provides them in a way where prometheus can 'scrape' them.
- Cadvisor: Collects metrics on containers (memory, cpu etc...) and provides them in a way where prometheus can 'scrape' them.

This is networked as so that only grafana is web accessible (using træfik)! This is best for your security.

## ENV file

To run this, you must create a `.env` file in this directory. Below are the required fields:

- DOMAIN - Your FQDN
- GRAFANA_DATA_DIR - Path to where grafana data will be stored
- GRAFANA_PLUGINS - Comma seperated list of grafana plugins to be installed
- PROMETHEUS_CONFIG_DIR - Path to where the prometheus config will be stored
  - Make sure to move your `prometheus.yml` and `alert.rules` to this directory
- PROMETHEUS_DATA_DIR - Path to where the prometheus data will be stored
- ALERT_MANAGER_CONFIG - Path to where the alert manager config will be stored
  - Make sure to move your alert manager config to here
