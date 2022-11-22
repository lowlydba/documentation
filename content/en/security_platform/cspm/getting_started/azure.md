---
title: Azure Getting Started with CSPM
kind: documentation
---

Cloud Security Posture Management (CSPM)...

## Set up the Datadog Azure integration

If you haven't already, set up the [Microsoft Azure integration][1].

## Enable CSPM for Azure

Use one of the following methods to enable CSPM for your Azure subscriptions:

### Security Setup & Configuration

1. Navigate to **Security** > **Setup and Configuration**.
2. Follow the [in-app instructions][5] to activate CSPM for your account.
3. On the **Setup and Configuration** > **Cloud Providers** tab, click the **Azure** tile.
4. Enable CSPM for your Azure subscriptions by turning on the **CSPM Enabled** toggle.

### Azure integration tile

1. On the Azure integration tile, select an Azure app.
2. Under **Resource Collection**, select the **Enable resource collection for Cloud Security Posture Management** checkbox.
3. Click **Update Configuration**.

## Visualize the first results

Navigate to **Security** > **Posture Management**.

Go to the homepage and wait for the first run to be complete

## Explore Azure detection rules

CSPM comes with a set of [out-of-the-box detection rules][2] that evaluate the configuration of your Azure resources and identifies potential misconfigurations so you can immediately take steps to remediate.

To explore the Azure detection rules:

1. Navigate to **Security** > **Detection Rules**.
2. Choose **cloud_provider:azure** from the **Tag** facet.

After you explore the default detection rules, you can [customize how each rule scans your environment][3] and [set up notification targets][4].

[1]: https://docs.datadoghq.com/integrations/azure
[2]: /security_platform/default_rules/#cat-posture-management-cloud
[3]: /security_platform/cspm/frameworks_and_benchmarks#customize-how-your-environment-is-scanned-by-each-rule
[4]: /security_platform/cspm/frameworks_and_benchmarks#set-notification-targets-for-detection-rules
[5]: https://app.datadoghq.com/security/configuration