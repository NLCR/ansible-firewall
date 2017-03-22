Firewall
=========

Sets firewall for machines. It is very simple playbook, is does not define services in /etc/firewalld/services. Maybe later.

Example Playbook
----------------

- name: Firewalling machines
  hosts:
  - all
  roles:
  - { role: firewall }

- name: Firewalling Solr
  hosts: solr
  roles:
  - { role: firewall, open_port: [ 8983/tcp ] }

- name: Firewalling Fedora
  hosts: fedora
  roles:
  - { role: firewall, open_port: [ 18080/tcp ] }

License
-------

BSD

Author Information
------------------

Rudolf Kreibich, https://github.com/westfood
