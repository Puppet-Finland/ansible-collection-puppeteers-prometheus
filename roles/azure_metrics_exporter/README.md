# puppeteers.prometheus.azure_metrics_exporter

This is an Ansible role for managing
[azure-metrics-exporter](https://github.com/webdevops/azure-metrics-exporter).
Packages can be built with
[podman-builder](https://github.com/Puppet-Finland/podman-builder).

# Usage

Include the role puppeteers.prometheus.azure_metrics_exporter. The parameters you need to
set are these:

    puppeteers_prometheus_azure_metrics_exporter_client_id
    puppeteers_prometheus_azure_metrics_exporter_client_secret
    puppeteers_prometheus_azure_metrics_exporter_tenant_id
    puppeteers_prometheus_azure_metrics_exporter_servicediscovery_subscription_id

For details see https://github.com/webdevops/go-common/blob/main/azuresdk/README.md

If you wish to manage firewalld rules:

    puppeteers_prometheus_azure_metrics_exporter_manage_firewalld: true
    puppeteers_prometheus_azure_metrics_exporter_firewalld_zone: public

If you do not wish to manage the package:

    puppeteers_prometheus_azure_metrics_exporter_manage_package: false

See [defaults/main.yml](defaults/main.yml) for a full list of parameters.
