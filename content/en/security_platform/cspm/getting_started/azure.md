---
title: Azure Getting Started with CSPM
kind: documentation
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

CSPM comes with a set of [out-of-the-box detection rules][2] that evaluate the configuration of your Azure resources and identifies potential misconfigurations so you can immediately take steps to remediate.

Datadog continuously develops new default rules, which are automatically imported into your account, your Application Security Management library, and the Agent, depending on your configuration.

Navigate to **Security** > **Detection Rules** and click **Detection Rules**.

[1]: https://docs.datadoghq.com/integrations/azure
[2]: /security_platform/default_rules/#cat-posture-management-cloud