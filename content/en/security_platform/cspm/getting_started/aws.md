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

Go to the homepage and wait for the first run to be complete

## Explore AWS detection rules

CSPM comes with a set of [out-of-the-box detection rules][3] that evaluate the configuration of your AWS resources and identifies potential misconfigurations so you can immediately take steps to remediate.

To explore the AWS detection rules:

1. Navigate to **Security** > **Detection Rules**.
2. Choose **cloud_provider:aws** from the **Tag** facet.

Datadog continuously develops new default rules, which are automatically imported into your account, your Application Security Management library, and the Agent, depending on your configuration.

[1]: https://docs.datadoghq.com/integrations/amazon_web_services/
[2]: /integrations/amazon_web_services/?tab=roledelegation#cloud-security-posture-management
[3]: /security_platform/default_rules/#cat-posture-management-cloud