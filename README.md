prometheus-bird-exporter
=========

Install and configure prometheus-bird-exporter.

Requirements
------------

None.

Role Variables
--------------

| Variable Name | Default Value | Description |
--------------- |---------------|--------------
`prometheus_bird_exporter_enable_ospf` | `false` | whether to enable ospf support
`prometheus_bird_exporter_use_version_2` | `{{ bird_use_version_2 }}` if defined, else `false` | whether to use bird version 2 (incompatible with version 1.6)
`prometheus_bird_exporter_web_listen_address` | `127.0.0.1:9324` | what the exporter listens on

Dependencies
------------

None.

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

[Unredacted](https://unredacted.org/).
