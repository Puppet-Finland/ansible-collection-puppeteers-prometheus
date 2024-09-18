# puppeteers.prometheus.prometheus_misc

This is an Ansible role for managing some aspects of Prometheus not covered by
the official Prometheus role from the Prometheus project. Currently this
includes configuring firewalld.

# Usage

Include the role puppeteers.prometheus.prometheus_misc. If you wish it to
actually manage firewalld you need to define a variable:

    puppeteers_prometheus_prometheus_misc_manage_firewalld: true

See [defaults/main.yml](defaults/main.yml) for a full list of parameters.
