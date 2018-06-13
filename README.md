# mablanco.sectools

Ansible role to install several security related tools on a Linux system. This role should work on any modern Linux and Unix platforms.

## Requirements
- git CLI client

## Role Variables

The following variables control whether a tool is installed (*true*) or not (*false*).

- **the_harvester**: 'The Harvester' is a gathering information tool about an URL.
- **golismero**: 'GoLismero' is an open source framework for security testing.
- **reconscan**: 'ReconScan' is a set of network reconnaissance and vulnerability assessment tools.
- **wascan**: 'WAScan' is a web application security scanner using "black-box" methods.

## Example Playbook

Example of how to use this role:

    - hosts: sec-nodes
      vars:
         the_harvester: true
         golismero: true
         reconscan: true
         wascan: true
      roles:
         - { role: mablanco.sectools }

## TODO

- Add lots of tools!!!

## License

GPLv3
