# cloudwatch-exporter

This is an Ansible role for managing cloudwatch-exporter. This supports
installation of cloudwatch-exporter from a DNF repo (if such exists for you)
and optionally firewalld configuration.

# Usage

Include the role puppeteers.prometheus.cloudwatch_exporter. See
[defaults/main.yml](defaults/main.yml) for parameters.
