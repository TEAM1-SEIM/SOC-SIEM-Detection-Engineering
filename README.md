# SOC Lab | SIEM Detection Engineering & Operations

![Wazuh 4.14.9](https://img.shields.io/badge/Wazuh-4.14.9-315672)

This hands-on Security Operations Center (SOC) portfolio follows the path from collecting endpoint logs to using them for detection, alert triage, and threat hunting. Week 1 establishes the foundation in Wazuh and verifies that an analyst can trace activity on a Linux endpoint to a searchable event.

**[View Week 1 Report](Week-01/W1-SIEM-Architecture-Onboarding-Report-SOC-Theme.pdf)** · [Read the Week 1 summary](Week-01/README.md)

## Weekly progress

| Week | Lab | Verified result | Documentation |
| --- | --- | --- | --- |
| 01 | SIEM Architecture & Log Onboarding | One Kali endpoint enrolled. Its events were searchable in Wazuh. | [Summary](Week-01/README.md) · [Full report (PDF)](Week-01/W1-SIEM-Architecture-Onboarding-Report-SOC-Theme.pdf) |

## Project objectives

- Design a SIEM collection pipeline and verify coverage for each onboarded source.
- Build and evaluate detections using events with known origins and documented fields.
- Practice alert triage and threat hunting by tracing rule matches back to the activity that generated them.

## Tools and technologies

| Technology | Role in the Week 1 lab |
| --- | --- |
| Wazuh 4.14.9 | The Manager decodes events and evaluates rules. The Dashboard provides the analyst view. |
| OpenSearch and Filebeat | Filebeat forwards alerts to the OpenSearch-based Wazuh Indexer for storage and search. |
| Ubuntu Server 26.04 LTS and VirtualBox | Guest operating system and hypervisor for the all-in-one Wazuh deployment. |
| Kali Linux | Monitored endpoint used to generate authentication and privilege-use events. |

## SOC skills demonstrated

- **Collection validation.** Checked agent enrollment, generated test activity, and located the resulting PAM and sudo events in Threat Hunting.
- **Alert interpretation.** Traced a sudo log through decoding and rule evaluation to identify the initiating user, target user, command, and MITRE ATT&CK mapping.
- **Retention management.** Measured a daily alert index, applied an index lifecycle policy, and verified that OpenSearch managed the index.

## Practical learning approach

Each completed lab pairs a short summary with a PDF containing the configuration, screenshots, and results. In Week 1, enrollment was the first checkpoint. Generating known activity on Kali and finding the corresponding rule matches in the Dashboard verified that the collection pipeline worked end to end.
