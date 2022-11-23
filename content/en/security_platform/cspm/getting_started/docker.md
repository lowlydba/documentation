---
title: Docker Getting Started with CSPM
kind: documentation
---

Cloud Security Posture Management (CSPM)...

## Enable CSPM for Docker

1. Navigate to **Security** > **Setup and Configuration**.
2. Follow the [in-app instructions][5] to activate CSPM for your account.
3. On the **Setup and Configuration** > **Host and containers** tab, click the **Docker** tile.
4. Click **Select API key** to choose the API key you want to use with CSPM.
5. Run the following command to enable CSPM in your Docker environment:
{{< code-block lang="bash" >}}
DOCKER_CONTENT_TRUST=1 \
  docker run -d --name dd-agent \
  --security-opt apparmor:unconfined \
  --cap-add SYS_ADMIN \
  --cap-add SYS_RESOURCE \
  --cap-add SYS_PTRACE \
  --cap-add NET_ADMIN \
  --cap-add IPC_LOCK \
  -v /var/run/docker.sock:/var/run/docker.sock:ro \
  -v /proc/:/host/proc/:ro \
  -v /sys/fs/cgroup/:/host/sys/fs/cgroup:ro \
  -v /etc/passwd:/etc/passwd:ro \
  -v /etc/group:/etc/group:ro \
  -v /:/host/root:ro \
  -v /etc/os-release:/host/etc/os-release \
  -v /sys/kernel/debug:/sys/kernel/debug \
  -e DD_COMPLIANCE_CONFIG_ENABLED=true \
  -e DD_RUNTIME_SECURITY_CONFIG_ENABLED=true \
  -e DD_SYSTEM_PROBE_ENABLED=true \
  -e HOST_ROOT=/host/root \
  -e DD_API_KEY=<DATADOG_API_KEY> \
  -e DD_SITE="datadoghq.com" \
  datadog/agent:latest
{{< /code-block >}}

## Visualize the first results

CSPM evaluates resources in increments between 15 minutes and four hours (depending on type). New findings from each scan are generated as soon as the scan completes.

To view the findings for your Docker containers, go to the [CSPM homepage][7].

## Explore Docker detection rules

CSPM comes with a set of [out-of-the-box detection rules][2] that analyze your Docker containers to find configuration issues as defined in the popular CIS compliance benchmark for Docker. When new configuration detection rules are added, they are automatically imported into your account.

To explore the Docker detection rules:

1. Navigate to **Security** > **Detection Rules**.
2. Choose **framework:cis-docker** from the **Tag** facet.

After you explore the default detection rules, you can review and take action on your  Docker misconfigurations in the [Security Findings Explorer][6], [customize how each rule scans your environment][3], and [set up notification targets][4].

[1]: https://docs.datadoghq.com/integrations/azure
[2]: /security_platform/default_rules/#cat-posture-management-infra
[3]: /security_platform/cspm/frameworks_and_benchmarks#customize-how-your-environment-is-scanned-by-each-rule
[4]: /security_platform/cspm/frameworks_and_benchmarks#set-notification-targets-for-detection-rules
[5]: https://app.datadoghq.com/security/configuration
[6]: https://app.datadoghq.com/security/compliance?time=now
[7]: https://app.datadoghq.com/security/compliance/homepage