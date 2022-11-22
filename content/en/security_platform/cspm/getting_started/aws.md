---
title: AWS Getting Started with CSPM
kind: documentation
---

Cloud Security Posture Management (CSPM)...

## Set up the Datadog AWS integration

If you haven't already, set up the [Amazon Web Services integration][1]. For CSPM, you must also add the [necessary permissions][2] for resource collection.

## Enable CSPM for AWS

Use one of the following methods to enable CSPM for your AWS accounts:

### Security Setup & Configuration

1. Navigate to **Security** > **Setup and Configuration**.
2. Select **Posture Management**.
3. To enable CSPM for an AWS account, turn on the **Collect Resources** toggle.

### AWS integration tile

1. On the AWS integration tile, select an AWS account and click **Resource Collection**.
2. Select **Cloud Security Posture Management Collection** to enable resource collection for CSPM.
3. Click **Save**.

## Visualize the first results

Navigate to **Security** > **Posture Management**.

Go to the homepage and wait for the first run to be complete

## Explore AWS detection rules

CSPM comes with a set of [out-of-the-box detection rules][3] that evaluate the configuration of your AWS resources and identifies potential misconfigurations so you can immediately take steps to remediate.

To explore the AWS detection rules:

1. Navigate to **Security** > **Detection Rules**.
2. Choose **cloud_provider:aws** from the **Tag** facet.

After you explore the default detection rules, you can [customize how each rule scans your environment][4] and [set up notification targets][5].

[1]: https://docs.datadoghq.com/integrations/amazon_web_services/
[2]: /integrations/amazon_web_services/?tab=roledelegation#cloud-security-posture-management
[3]: /security_platform/default_rules/#cat-posture-management-cloud
[4]: /security_platform/cspm/frameworks_and_benchmarks#customize-how-your-environment-is-scanned-by-each-rule
[5]: /security_platform/cspm/frameworks_and_benchmarks#set-notification-targets-for-detection-rules