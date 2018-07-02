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
Define a function to test the modules possibile are:\r
host\r
Ansible\r
File\r
Group\r
Interface\r
Iptables\r
MountPoint\r
Package\r
PipPackage\r
Process\r
PuppetResource\r
Facter\r
Salt\r
Service\r
Socket\r
Sudo\r
Supervisor\r
Sysctl\r
SystemInfo\r
User\r
