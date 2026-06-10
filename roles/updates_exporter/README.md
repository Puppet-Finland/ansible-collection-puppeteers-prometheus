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

Select which release version without the 'v':


    puppeteers_prometheus_updates_exporter_release_version: "0.1.3"

If you wish to manage config yourself instead of using the default:


    puppeteers_prometheus_updates_exporter_manage_config: true

To tweak the configuration that gets managed:

    puppeteers_prometheus_updates_exporter_port: 9101
    puppeteers_prometheus_updates_exporter_interval_seconds: 3600
    puppeteers_prometheus_updates_exporter_log_level: "info"

See [defaults/main.yml](defaults/main.yml) for a full list of parameters.
