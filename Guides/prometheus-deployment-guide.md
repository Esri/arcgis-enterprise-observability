# Deploying Prometheus to scrape ArcGIS Enterprise metrics

The following steps are appropriate for installing and configuring a minimal Prometheus deployment for scraping metrics from ArcGIS Enterprise. Refer to the [Prometheus documentation](https://prometheus.io/docs/prometheus/latest/getting_started/) for additional details about the deployment process. 

1. [Download the latest LTS version of Prometheus server](https://prometheus.io/download/) for your operating system.
1. Unzip the downloaded file.
1. Create a configuration file for Prometheus. You can use prometheus-config.yml as a template. 
    - You can have multiple `scrape_config` settings, one for each ArcGIS Server site you want to scrape metrics from. The example template has scrape configurations for a single federated ArcGIS Server site and a single standalone ArcGIS Server site.
    - Give each `scrape_config` a meaningful name, such as the name of the ArcGIS Server site you are scraping metrics for.
    - The `url` value for `http_sd_configs` must match the fully-qualified domain name and context of your ArcGIS Server site. 
    - If you are using an API key from ArcGIS Enterprise for a federated ArcGIS Server site, use that key for the `bearer_token` value.
    - If you are using an administrative token from a standalone ArcGIS Server site, use that token for the `bearer_token` value.
    - If you are using token-based authorization for a standalone ArcGIS Server site, the HTTP referer value in the configuration must match the URL specified for the HTTP referer when the token was created.
    - It is recommended that you use `insecure_skip_verify: false` to ensure Prometheus verifies the validity of the certificate presented by ArcGIS Server. If Prometheus does not recognize the validity of this certificate, it is recommended to [add the `ca` and `ca_file` information](https://prometheus.io/docs/prometheus/latest/configuration/configuration/#tls_config) for the certificate to the configuration file so the certificate can be verified. 
1. From the command line, navigate to the directory where you extracted the downloaded archive and [Start Prometheus server](https://prometheus.io/docs/prometheus/latest/getting_started/#starting-prometheus) specifying the path to the configuration file. For example:

    `./prometheus --config.file=prometheus-config.yml`

1. Note the url, including port number, of Prometheus server. By default this url is `http://localhost:9090`. You will need this URL if you want to configure a Grafana dashboard to visualize metrics scraped by Prometheus.
1. In the Prometheus web application, select Status > Target health to verify that you are able to access ArcGIS Enterprise metrics from Prometheus. It may take 1 - 2 minutes for Prometheus to add data from ArcGIS Enterprise.

