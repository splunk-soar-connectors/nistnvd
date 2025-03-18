# NIST NVD

Publisher: Trisha Pancho \
Connector Version: 1.0.1 \
Product Vendor: NIST \
Product Name: NVD \
Minimum Product Version: 5.3.2.88192

App to query NIST for CVEs

### Configuration variables

This table lists the configuration variables required to operate NIST NVD. These variables are specified when configuring a NVD asset in Splunk SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**api_version** | required | string | Supported API Version |

### Supported Actions

[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration \
[cve lookup](#action-cve-lookup) - Query NVD for specific CVE ID

## action: 'test connectivity'

Validate the asset configuration for connectivity using supplied configuration

Type: **test** \
Read only: **True**

#### Action Parameters

No parameters are required for this action

#### Action Output

No Output

## action: 'cve lookup'

Query NVD for specific CVE ID

Type: **generic** \
Read only: **False**

#### Action Parameters

PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**cve** | required | CVE ID | string | |

#### Action Output

DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.cve | string | | |
action_result.data.\*.vulnerabilities.\*.cve.cisaVulnerabilityName | string | | |
action_result.data.\*.vulnerabilities.\*.cve.descriptions.\*.value | string | | |
action_result.data.\*.vulnerabilities.\*.cve.references.\*.url | string | | |
action_result.data.\*.vulnerabilities.\*.cve.published | string | | |
action_result.data.\*.vulnerabilities.\*.cve.metrics.cvssMetricV31.\*.cvssData.baseScore | string | | |
action_result.data.\*.vulnerabilities.\*.cve.metrics.cvssMetricV31.\*.cvssData.baseSeverity | string | | |
action_result.data.\*.vulnerabilities.\*.cve.metrics.cvssMetricV31.\*.cvssData.attackVector | string | | |
action_result.data.\*.vulnerabilities.\*.cve.metrics.cvssMetricV31.\*.impactScore | string | | |
action_result.data.\*.vulnerabilities.\*.cve.metrics.cvssMetricV31.\*.exploitabilityScore | string | | |
action_result.data.\*.vulnerabilities.\*.cve.metrics.cvssMetricV31.\*.cvssData.attackComplexity | string | | |
action_result.status | string | | success failed |
action_result.message | string | | |
summary.total_objects | numeric | | |
summary.total_objects_successful | numeric | | |
action_result.summary | string | | |

______________________________________________________________________

Auto-generated Splunk SOAR Connector documentation.

Copyright 2025 Splunk Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and limitations under the License.
