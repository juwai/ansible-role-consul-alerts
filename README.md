Ansible Role: Consul Alerts
===========================

Install Consul Alerts on Amazon EC2 or CentOS server.

Requirements
------------

Written in Ansible 2.0.*

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

### consul_alerts_supervisor_enabled

Use Supervisord for controlling Consul Alerts, default is true

### consul_alerts_version

Version of Consul Alerts to install, default is 0.3.0

### consul_alerts_url

Source URL, default is templatized

### consul_alerts_bind_address

IP address to bind to, default is inherited from consul_bind_address of consul role

### consul_alerts_port

Port to bind to, default is 8700

### consul_alerts_dir

Path where to install consul alerts's files, default is templatized (ie. `/home/consul/consul_alerts_0.0.1`)

### consul_alerts_log_dir

Path where to store log files, default is templatized (ie. `/home/consul/consul_alerts_0.0.1/logs`)

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