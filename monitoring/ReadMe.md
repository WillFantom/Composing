# Monitoring

This section is split into the folling stacks:

 - Per Host: This stack collects data from the host it is deployed on, and also store it in a time series database. This databased can then be accessed via an API, locally or remotely.
   - See [here](./per-host/README.md).

 - Frontend: This stack simply provides a friendly UI for the monitoring data. You can connect as many databases from the `per-host` stack to this so you can collate and show all the data in one place.
   - See [here](./frontend/README.md).
