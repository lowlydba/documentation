---
title: AWS Getting Started with CSPM
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

## Setup

### Installation

If you haven't already, set up the [Amazon Web Services integration][1] first.

### Set up the Datadog AWS integration

If you haven't already, set up the Amazon Web Services integration first.

Make sure to give correct permissions

### Enable CSPM for AWS

one of the following ways:

On the AWS integration tile, ensure that Cloud Security Posture Management Collection is checked under resource collection.

   1. Click on the AWS account where you wish to enable resource collection.
   2. Go to the **Resource collection** tab for that account and enable `Cloud Security Posture Management Collection`.


CSPM (in the product):

1. Navigate to **Security** > **Setup and Configuration**.
2. Select **Posture Management**.
3. Ensure necessary permissions...
4. To enable CSPM for an AWS account, turn on the **Collect Resources** toggle.

AWS integration tile:

1. On the AWS integration tile, select an AWS account and click **Resource Collection**.
2. Select **Cloud Security Posture Management Collection** to enable resource collection for CSPM.
3. Click **Save**.


> Resource Collection tab, ensure 

### Visualize the first results

placeholder text

### Onboard new accounts following the same process

## Explore AWS detection rules

CSPM comes with a set of out-of-the-box detection rules which aim to catch attack attempts and vulnerability triggers that impact your production systems.

Detection Rules list in product, and tick “AWS” to see all rules applying to AWS.
Full list of OOTB rules (link)

[out-of-the-box detection rules][2].

Navigate to **Security** > **Detection Rules** and click **Detection Rules**.

[1]: https://docs.datadoghq.com/integrations/amazon_web_services/
[2]: /security_platform/default_rules/#cat-posture-management-cloud