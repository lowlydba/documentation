---
title: Azure Getting Started with CSPM
kind: documentation
further_reading:
- link: "security_platform/default_rules"
  tag: "Documentation"
  text: "Explore default cloud configuration detection rules"
- link: "security_platform/cspm/findings"
  tag: "Documentation"
  text: "Search and explore CSPM findings"
- link: "security_platform/cspm/frameworks_and_benchmarks"
  tag: "Documentation"
  text: "Learn about frameworks and industry benchmarks"
---

## Overview 

placeholder text

### Set up the Datadog Azure integration

If you haven't already, set up the [Microsoft Azure integration][1].

### Enable CSPM for Azure

Use one of the following methods to enable CSPM for your Azure subscriptions:

#### Security Setup & Configuration

1. Navigate to **Security** > **Setup and Configuration**.
2. Select **Posture Management**.
3. To enable CSPM for an Azure subscription, turn on the **CSPM Enabled** toggle.

#### Azure integration tile

1. On the Azure integration tile, select an Azure account and click **Resource Collection**.
2. Select **Cloud Security Posture Management Collection** to enable resource collection for CSPM.
3. Click **Save**.

### Visualize the first results

placeholder text

Onboard new accounts following the same process

### Explore Azure detection rules

CSPM comes with a set of out-of-the-box detection rules which aim to catch attack attempts and vulnerability triggers that impact your production systems.

Detection Rules list in product, and tick Azure to see all rules applying to AWS.
Full list of OOTB rules (link)

[out-of-the-box detection rules][3].

Navigate to **Security** > **Detection Rules** and click **Detection Rules**.

[1]: https://docs.datadoghq.com/integrations/azure
[2]: /security_platform/default_rules/#cat-posture-management-cloud