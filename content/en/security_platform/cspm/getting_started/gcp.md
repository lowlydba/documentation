---
title: Google Cloud Platform Getting Started with CSPM
kind: documentation
---

Cloud Security Posture Management (CSPM) makes it easier to assess and visualize the current and historic security posture of your Google Cloud Platform (GCP) resources, automate audit evidence collection, and catch misconfigurations that leave your organization vulnerable to attacks.

## Set up the Datadog GCP integration

If you haven't already, set up the [Google Cloud Platform integration][1].

## Enable CSPM for CCP

Use one of the following methods to enable CSPM for your GCP projects:

### Security Setup & Configuration

1. Navigate to **Security** > **Setup and Configuration**.
2. Follow the [in-app instructions][5] to activate CSPM for your account.
3. On the **Setup and Configuration** > **Cloud Providers** tab, click the **GCP** tile.
4. Enable CSPM for your GCP projects by turning on the **CSPM Enabled** toggle.

### GCP integration tile

1. On the GCP integration tile, select a GCP project.
2. Under **Enable resource collection for Cloud Security Posture Management**, select the **Resource collection** checkbox.
3. Click **Update Configuration**.

## Visualize the first results

CSPM evaluates resources in increments between 15 minutes and four hours (depending on type). New findings from each scan are generated as soon as the scan completes.

To view the findings for your GCP resources, go to the [CSPM homepage][7].

## Explore GCP detection rules

CSPM comes with a set of [out-of-the-box detection rules][2] that evaluate the configuration of your GCP resources and identifies potential misconfigurations so you can immediately take steps to remediate. When new configuration detection rules are added, they are automatically imported into your account.

To explore the GCP detection rules:

1. Navigate to **Security** > **Detection Rules**.
2. Choose **cloud_provider:gcp** from the **Tag** facet.

After you explore the default detection rules, you can review and take action on your GCP misconfigurations in the [Security Findings Explorer][6], [customize how each rule scans your environment][3], and [set up notification targets][4].

[1]: https://docs.datadoghq.com/integrations/google_cloud_platform
[2]: /security_platform/default_rules/#cat-posture-management-cloud
[3]: /security_platform/cspm/frameworks_and_benchmarks#customize-how-your-environment-is-scanned-by-each-rule
[4]: /security_platform/cspm/frameworks_and_benchmarks#set-notification-targets-for-detection-rules
[5]: https://app.datadoghq.com/security/configuration
[6]: https://app.datadoghq.com/security/compliance?time=now
[7]: https://app.datadoghq.com/security/compliance/homepage