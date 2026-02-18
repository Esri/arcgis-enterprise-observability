# ArcGIS Enterprise observability resources

This repository contains resources related to configuring beta observability capabilities for ArcGIS Enterprise 12.0. For full documentation of these features, refer to the instructions in the [Early Adopter Community](https://www.esri.com/en-us/user-research-testing/early-adopter). 

## Features

This repository contains the following resources:

- Guides: Deployment guides for Prometheus and Grafana
- `prometheus-config.yml`: an example configuration to discover and add ArcGIS Server metrics as a scrape target for an existing Prometheus deployment.
- DashboardTempates: Example Grafana dashboard configurations.

## Instructions

1. Clone this repository to a machine where you will run Prometheus and/or Grafana.
1. If you do not already have Prometheus and Grafana running, following the instructions in the deployment guides to install and configure both.
1. Edit the `prometheus-config.yml` file to use values for your ArcGIS Enterprise deployment. 
1. To collect metrics, start Prometheus using the edited configuration file or merge the values into an existing Prometheus configuration.
1. Import the example Grafana dashbaord to visualize metrics.

## Requirements
- ArcGIS Server services must be configured to enable metrics before they can be collected
- To collect metrics from ArcGIS Enterprise, you will need a Prometheus server configured to collect them.
- To visualize metrics, you will need Grafana or some other third-party visualization tool.

## Resources
- Full documentation of the beta observability features is available in the [Early Adopter Community](https://www.esri.com/en-us/user-research-testing/early-adopter). 
- Additional documentation on [monitoring ArcGIS Enterprise](https://enterprise.arcgis.com/en/portal/latest/administer/windows/monitoring-best-practices.htm).
- The [Observability pillar](https://architecture.arcgis.com/en/framework/architecture-pillars/observability/overview.html) of a well-architected ArcGIS system.

## Issues

Find a bug or want to request a new feature?  Please let us know by submitting an issue.

## Contributing

Esri welcomes contributions from anyone and everyone. Please see our [guidelines for contributing](https://github.com/esri/contributing).

## Licensing

Copyright 2025 Esri

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.


A copy of the license is available in the repository's [LICENSE.txt](LICENSE.txt?raw=true) file.

