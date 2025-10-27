# Deploying Grafana to visualize ArcGIS Enterprise metrics

The following steps are appropriate for installing and configuring a minimal Grafana deployment for visualizing metrics collected from ArcGIS Enterprise. Refer to the [Grafana documentation](https://grafana.com/docs/grafana/latest/setup-grafana/) for additional details about the deployment process. Before you can visualize metrics with Grafana, you will need to [configure Prometheus](prometheus-deployment-guide.md) to scrape metrics from ArcGIS Enterprise. 

1. [Download the latest version of Grafana](https://grafana.com/grafana/download) for your operating system. The most recent version of Grafana may not be available for your operating system, and you may need to choose an older version. Make sure the architecture of the download (64 bit or ARM64) matches your system.
1. Follow the installation guide:
    - [Debian or Ubuntu](https://grafana.com/docs/grafana/latest/setup-grafana/installation/debian/)
    - [RHEL or Fedora](https://grafana.com/docs/grafana/latest/setup-grafana/installation/redhat-rhel-fedora/)
    - [SUSE or OpenSUSE](https://grafana.com/docs/grafana/latest/setup-grafana/installation/suse-opensuse/)
    - [macOS](https://grafana.com/docs/grafana/latest/setup-grafana/installation/mac/)
    - [Windows](https://grafana.com/docs/grafana/latest/setup-grafana/installation/windows/)
1. [Start the Grafana server](https://grafana.com/docs/grafana/latest/setup-grafana/start-restart-grafana/) and open the web application. By default the url is `localhost:3000`.
1. Sign in with the default username `admin` and password `admin`.
1. Update the password for the `admin` username.
1. [Configure the Prometheus data source](https://grafana.com/docs/grafana/latest/datasources/prometheus/configure/).
    1. In the Grafana web application, expand Connections and click Data sources > Prometheus.
    1. For the Prometheus server URL, add the URL of your Prometheus server, including port number (for example, http://localhost:9090).
    1. Click Save & test to verify you can successfully query the Prometheus API.
1. [Import a dashboard](https://grafana.com/docs/grafana/latest/dashboards/build-dashboards/import-dashboards/)
    1. Click Dashboards
    1. Click New > Import
    1. Drag and drop a `.json` dashboard configuration file to upload it. The [example template dashboard configurations](../DashboardTemplates) are appropriate for common use cases for ArcGIS Enterprise metrics.


