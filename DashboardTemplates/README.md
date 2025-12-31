The `.json` files in this directory are example Grafana dashboard templates for common use cases for ArcGIS Enterprise metrics. You can [import a dashboard](https://grafana.com/docs/grafana/latest/dashboards/build-dashboards/import-dashboards/) by uploading a file to your Grafana server.

- ArcGIS_11.5_on_k8s_observability.json: A template for ArcGIS Enterprise 11.5 on Kubernetes.
- ArcGIS_12.0_observability_beta.json: A template for ArcGIS Enterprise 12.0 on Windows and Linux. Note that the metrics endpoints used for this dashboard are a beta feature in ArcGIS Enterprise 12.0 on Windows and Linux.

These templates were created and tested using Grafana release v12.1.1.

Older or newer versions may require changes to the dashboards, refer to the Grafana [release documentation](https://grafana.com/docs/grafana/latest/whatsnew/) for potential breaking changes.

If any problems are found with the templates, please [provide feedback via an issue](https://github.com/Esri/arcgis-enterprise-observability/issues/new) and an accompanying pull request if available.