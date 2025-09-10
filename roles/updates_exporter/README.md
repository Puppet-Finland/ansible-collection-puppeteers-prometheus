# puppeteers.prometheus.updates_exporter

This is an Ansible role for managing a
[updates_exporter](https://github.com/Puppet-Finland/updates-exporter).
Packages can be built with
[podman-builder](https://github.com/Puppet-Finland/podman-builder).

# Usage

Include the role puppeteers.prometheus.updates_exporter. You don't necessarily
need to set any parameters. With the default settings updates_exporter rpm is
downloaded from Hetzner Object Storage (built with podman-builder, see above).

If you wish to manage firewalld rules:

    puppeteers_prometheus_updates_exporter_manage_firewalld: true

See [defaults/main.yml](defaults/main.yml) for a full list of parameters.
