prometheus-bird-exporter
=========

Install and configure prometheus-bird-exporter, including TLS authentication.

Requirements
------------

A TLS server certificate (certificate and key concatenated) placed in
`/etc/haproxy/prometheus-server.pem`, and the corresponding CA certificate
placed in `/etc/haproxy/prometheus-ca.pem`.

Role Variables
--------------


| Variable Name | Default Value | Description |
--------------- |---------------|--------------
`prometheus_bird_exporter_enable_ospf` | `false` | whether to enable ospf support
`prometheus_bird_exporter_use_version_2` | `{{ bird_use_version_2 }}` if defined, else `false` | whether to use bird version 2 (incompatible with version 1.6)

Dependencies
------------

* [SOSETH haproxy](https://github.com/SOSETH/haproxy) role, or a role providing an identical `conf.d` style configuration interface for haproxy.
* (optional) [SOSETH local-ca](https://github.com/SOSETH/local-ca) role, or a role providing a similar interface for automatic CA cert generation.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: prometheus-bird-exporter

License
-------

BSD

Author Information
------------------

Find me on [GitHub](https://github.com/ThreeFx).
