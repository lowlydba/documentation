---
title: Kubernetes Getting Started with CSPM
kind: documentation
---

Cloud Security Posture Management (CSPM) makes it easier to assess and visualize the current and historic security posture of your Kubernetes clusters, automate audit evidence collection, and catch misconfigurations that leave your organization vulnerable to attacks.

## Enable CSPM for Kubernetes

1. If you haven't already, install the [Datadog Agent][1] (version 7.27+).
2. Add the following to the `datadog` section of the `values.yaml` file:
    {{< code-block lang="yaml" filename="values.yaml" >}}
    # values.yaml file
    datadog:
    [...]
      # Add this to enable Cloud Security Posture Management and Cloud Workload Security
      securityAgent:
        runtime:
          enabled: true
        compliance:
          enabled: true
    {{< /code-block >}}
3. Restart the Agent.

## Visualize the first results

CSPM evaluates resources in increments between 15 minutes and four hours (depending on type). New findings from each scan are generated as soon as the scan completes.

To view the findings for your Kubernetes clusters, go to the [CSPM homepage][7].

## Explore Kubernetes detection rules

CSPM comes with a set of [out-of-the-box detection rules][2] that evaluate the configuration of your Kubernetes clusters and identifies potential misconfigurations so you can immediately take steps to remediate. When new configuration detection rules are added, they are automatically imported into your account.

To explore the Kubernetes detection rules:

1. Navigate to **Security** > **Detection Rules**.
2. Choose **framework:cis-kubernetes** from the **Tag** facet.

After you explore the default detection rules, you can review and take action on your Kubernetes misconfigurations in the [Security Findings Explorer][6], [customize how each rule scans your environment][3], and [set up notification targets][4].

[1]: https://app.datadoghq.com/account/settings#agent/kubernetes
[2]: /security_platform/default_rules/#cat-posture-management-infra
[3]: /security_platform/cspm/frameworks_and_benchmarks#customize-how-your-environment-is-scanned-by-each-rule
[4]: /security_platform/cspm/frameworks_and_benchmarks#set-notification-targets-for-detection-rules
[5]: https://app.datadoghq.com/security/configuration
[6]: https://app.datadoghq.com/security/compliance?time=now
[7]: https://app.datadoghq.com/security/compliance/homepage