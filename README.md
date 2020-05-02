![Ansible Lint](https://github.com/johanneskastl/ansible-role-install_and_configure_coturn/workflows/Ansible%20Lint/badge.svg)

install_and_configure_coturn
=========

Install coturn and configure it.

Requirements
------------

None.

Role Variables
--------------

Variables for the role to work:
- `coturn_package`: name of the coturn package, default value is `coturn`.
- `coturn_service`: name of the coturn service, default value is `coturn`.
- `path_to_turnserver_configfile`: Path to turnserver.conf, default value is `/etc/coturn/turnserver.conf`.

coturn-related variables:
- `coturn_static_auth_secret`: (Required) Shared secret to be used in the configuration.
- `coturn_realm`: (Required) Realm to set in the configuration.
- `path_to_coturn_tls_cert`: (Required) Path to the TLS certificate for coturn to use.
- `path_to_coturn_tls_cert_key`: (Required) Path to the private key for the TLS certificate.
- `path_to_coturn_tls_dh_file`: (Required) Path to a DH params file.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: 'ojkastl.install_and_configure_coturn' }

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via mail@ojkastl.de or kastl@b1-systems.de.
