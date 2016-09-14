mablanco.sectools
=

Ansible role to install several security related tools on a Linux system. Initially, this role will work on Debian platforms and will be adapted to other distros in the future.

Role Variables
-

The following variables control whether a tool is installed (*true*) or not (*false*). 

- **the_harvester**: 'The Harvester' is a gathering information tool about an URL.


Example Playbook
-

Example of how to use this role:

    - hosts: sec_nodes
      vars:
         the_harvester: true
      roles:
         - { role: mablanco.sectools }

TODO
-
- Add lots of tools!!!

License
-

GPLv3

Author Information
-

Marco Antonio Blanco <mablanco@correolibre.eu>
