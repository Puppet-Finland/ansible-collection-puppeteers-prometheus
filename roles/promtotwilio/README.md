# puppeteers.prometheus.promtotwilio

This is an Ansible role for managing a [patched version of
promtotwilio](https://github.com/Puppet-Finland/promtotwilio/tree/multiple_receivers).
Packages can be built with
[podman-builder](https://github.com/Puppet-Finland/podman-builder).

# Usage

Include the role puppeteers.prometheus.promtotwilio. The parameters you need to
set are these:

    puppeteers_prometheus_promtotwilio_sid: 7402ad04474540d56e1f1a79037e2f29a1
    puppeteers_prometheus_promtotwilio_token: 273e41edf72d9a0143c7beada017adb6
    puppeteers_prometheus_promtotwilio_sender: "+12334567890"
    puppeteers_prometheus_promtotwilio_receiver: "+358505050505,+358606060606"
    puppeteers_prometheus_promtotwilio_port: 9191

These are sample values from podman-builder: replace them with correct values
from Twilio.

If you wish to manage firewalld rules:

    puppeteers_prometheus_promtotwilio_manage_firewalld: true
    puppeteers_prometheus_promtotwilio_firewalld_zone: public

See [defaults/main.yml](defaults/main.yml) for a full list of parameters.
