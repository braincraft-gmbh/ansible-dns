Role Name
=========

A role to setup a small private DNS server for a cluster based on `dnsmasq`. It serves the contents of a dynamically generated `/etc/hosts` containing all hosts in the inventory.

Requirements
------------

None.

Role Variables
--------------

The IP addresses will be read from the interface defined in `dns_interface`. These addresses will be present in the hosts file together with the inventory hostname and their FQDN (appended `ansible_hostname` appended by with the `domain` variable).

Following defaults are present:

```
domain: local
dns_interface: eth0
```

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: lb
      roles:
         - bc.dns

License
-------

GNU GPLv3

Author Information
------------------

Gualter Barbas Baptista <gualter@ecobytes.net>
