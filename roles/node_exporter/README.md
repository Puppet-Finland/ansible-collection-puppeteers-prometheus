# node_exporter

An Ansible role for installing and configuring Prometheus node exporter.

## Requirements

Currently this role only supports RHEL 9 and derivatives.

## Dependencies

This role has no external dependencies.

## Role variables

This role has the following variables:

* *node_exporter_firewalld_zone:* the firewall zone in which traffic to the Node Exporter port (9100/tcp) should allowed (defaults to "public")

## License

BSD-2-Clause
