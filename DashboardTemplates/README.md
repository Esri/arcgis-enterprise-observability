The `.json` files in this directory are example Grafana dashboard templates for common use cases for ArcGIS Enterprise metrics. You can [import a dashboard](https://grafana.com/docs/grafana/latest/dashboards/build-dashboards/import-dashboards/) by uploading a file to your Grafana server. 

This directory includes the following template files:

- `ArcGIS_12.1_UsageAnalytics.json`:  Usage analytics, such as number of users and number of requests for ArcGIS Enterprise 12.1 on Windows, Linux, and Kubernetes. 
- `ArcGIS_12.1_on_Windows_Linux_System_Diagnostics.json`: ArcGIS Enterprise 12.1 on Windows and Linux system diagnostic metrics, such as uptime, performance, and system load. On Windows and Linux, ArcGIS Enterprise system diagnostics include machine-level metrics, such as CPU usage.
- `ArcGIS_12.1_on_Kubernetes_System_Diagnostics.json`. ArcGIS Enterprise 12.1 on Kubernetes system diagnostic metrics, such as uptime, performance, and system load. On Kubernetes, ArcGIS Enterprise system diagnostics do not include cluster or node-level metrics.
- `ArcGIS_12.0_observability_beta.json`: ArcGIS Enterprise 12.0 on Windows and Linux. Note that the metrics endpoints used for this dashboard are a beta feature in ArcGIS Enterprise 12.0 on Windows and Linux.
- `ArcGIS_11.5_on_k8s_observability.json`: ArcGIS Enterprise 11.5 and 12.0 on Kubernetes.

These templates were created and tested using Grafana release v12.1.1.

Older or newer versions may require changes to the dashboards, refer to the Grafana [release documentation](https://grafana.com/docs/grafana/latest/whatsnew/) for potential breaking changes.

If any problems are found with the templates, please [provide feedback via an issue](https://github.com/Esri/arcgis-enterprise-observability/issues/new) and an accompanying pull request if available.
