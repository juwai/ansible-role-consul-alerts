Ansible Role: Consul Alerts
===========================

Install Consul Alerts on Amazon EC2 or CentOS server.

Requirements
------------

Written in Ansible 2.0.*

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

### consul_alerts_port

Port to bind to, default is 8700

### consul_alerts_supervisor_enabled

Use Supervisord for controlling Consul Alerts, default is true

### consul_alerts_version

Version of Consul Alerts to install, default is 0.3.0

Dependencies
------------

+ `juwai.consul`
+ `juwai.supervisor`, when consul_alerts_supervisor_enabled == true

Example Playbook
----------------

    - hosts: servers
      roles:
        - juwai.consul-alerts

License
-------

MIT

Author Information
------------------

This role was created in 2016 by [Juwai Limited](http://www.juwai.com).