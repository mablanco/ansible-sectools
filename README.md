# mablanco.sectools

Ansible role to install several security testing and auditing tools on a Linux system. This role should work on any modern Linux and Unix platforms.

## Requirements
- git CLI client
- Python 2.6+ and 3.5+ & Setuptools
- PIP & Virtualenv (for both Python 2 and 3)

## Role Variables
The following variables control whether a tool is installed (*true*) or not (*false*).

- **golismero**: 'GoLismero' is an open source framework for security testing.
- **reconscan**: 'ReconScan' is a set of network reconnaissance and vulnerability assessment tools.
- **wascan**: 'WAScan' is a web application security scanner using "black-box" methods.
- **ssh_audit**: 'ssh-audit' is a tool for ssh server auditing.
- **testssl**: 'testssl.sh' is a tool for SSL ciphers and protocols auditing.
- **pompem**: 'Pompem' is an open source tool designed to automate the search for Exploits and Vulnerability in the most important databases.

## Example Playbook

Example of how to use this role:

    - hosts: sec-nodes
      vars:
         golismero: true
         wascan: true
         ssh_audit: true
      roles:
         - { role: mablanco.sectools }

## TODO

- Add lots of tools!!!

## License

GPLv3
