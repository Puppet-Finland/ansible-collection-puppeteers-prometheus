# puppeteers.prometheus.alertmanager_misc

This is an Ansible role for managing some aspects of Alertmanager not covered by
the official Alertmanager role from the Prometheus project. Currently this
includes configuring firewalld.

# Usage

Include the role puppeteers.prometheus.alertmanager_misc. If you wish it to
actually manage firewalld you need to define a variable:

    puppeteers_prometheus_alertmanager_misc_manage_firewalld: true

See [defaults/main.yml](defaults/main.yml) for a full list of parameters.
