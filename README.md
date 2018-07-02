# Infrastructural Test ![CI status](https://img.shields.io/badge/build-passing-brightgreen.svg)

There are the infrastructural test created with testinfra

### Installation


### Requirements
Python 2.x or 3.x

testinfra

`pip install testinfra`

paramiko

`pip install paramiko`

### Usage
Example:
```python
#!/usr/bin/env python3

def test_ngix(host):
    http = host.socket("tcp://80")
    https = host.socket("tcp://443")
    assert http.is_listening
    assert https.is_listening
```
Define a function to test the modules possibile are:
host
Ansible
File
Group
Interface
Iptables
MountPoint
Package
PipPackage
Process
PuppetResource
Facter
Salt
Service
Socket
Sudo
Supervisor
Sysctl
SystemInfo
User
