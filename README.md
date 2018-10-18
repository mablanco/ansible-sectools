# mablanco.sectools

Ansible role to install several security testing and auditing tools on a Linux system. This role should work on any modern Linux and Unix platforms.

## Requirements
- git CLI client
- Python 2.6+ or 3.x & Setuptools
- PIP & Virtualenv (for both Python 2 and 3). You can optionally install them with this role (read below)

## Role Variables
If you need/want to install PIP and Virtualenv with this role, give the **install_pip** variable a *true* value. Make sure that `easy_install` (part of Python Setuptools) is already available in the host.

The following variables control whether a tool is installed (*true*) or not (*false*).

- **golismero**: 'GoLismero' is an open source framework for security testing.
- **reconscan**: 'ReconScan' is a set of network reconnaissance and vulnerability assessment tools.
- **wascan**: 'WAScan' is a web application security scanner using "black-box" methods.
- **ssh_audit**: 'ssh-audit' is a tool for ssh server auditing.
- **testssl**: 'testssl.sh' is a tool for SSL ciphers and protocols auditing.

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
