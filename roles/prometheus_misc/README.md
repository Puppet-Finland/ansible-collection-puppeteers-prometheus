# puppeteers.prometheus.prometheus_misc

This is an Ansible role for managing some aspects of Prometheus not covered by
the official Prometheus role from the Prometheus project. Currently this
includes configuring firewalld and adding extra alerting rules.

# Usage

Include the role puppeteers.prometheus.prometheus_misc. If you wish it to
actually manage firewalld you need to define a variable:

    puppeteers_prometheus_prometheus_misc_manage_firewalld: true

To add extra alert rules:

```
puppeteers_prometheus_prometheus_misc_extra_alert_rules: |
  groups:
    - name: aws.rules
      rules:
      - alert: 'ElastiCacheCPUUtilizationAverageLow'
        expr: '(aws_elasticache_cpuutilization_average offset 15m) < 0.5'
        for: '1m'
        labels:
          severity: 'page'
        annotations:
          summary: '{% raw %}Redis cluster {{ $labels.cache_cluster_id }} has suspiciously low CPU utilization{% endraw %}'
          description: 'Redis cluster has low average CPU utilization'
```

Remember to wrap any strings that have Prometheus-specific templating with the raw/endraw tags.

See [defaults/main.yml](defaults/main.yml) for a full list of parameters.
