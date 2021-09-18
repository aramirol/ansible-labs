# ansible-labs

![](https://img.shields.io/badge/ansible-v2.10.13-white?logo=ansible)
![](https://img.shields.io/badge/ubuntu-20.04-critical?logo=ubuntu)

<img src="images/ansible-header-1024x640.png" width="20%" />

Ansible is an IT automation tool. It can configure systems, deploy software, and orchestrate more advanced IT tasks such as continuous deployments or zero downtime rolling updates.

## Installation

Ansible can be installed on many systems with pip, the Python package manager.

### Prerequisites: Installing `pip`
If pip is not already available on your system, run the following commands to install it:

```sh
$ curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
$ python get-pip.py --user
```

### Installing Ansible with `pip`

Once pip is installed, you can install Ansible:
```sh
$ python -m pip install --user ansible
```

In order to use the paramiko connection plugin or modules that require paramiko, install the required module:
```sh
$ python -m pip install --user paramiko
```

If you wish to install Ansible globally, run the following commands:
```sh
$ sudo python get-pip.py
$ sudo python -m pip install ansible
```

## Content

0. [Create environment](0.environment)
1. [Ad-hoc commands](1.ad-hoc)
2. [Playbooks examples](2.playbooks)
3. [Vars examples](3.vars)
4. [Includes examples](4.includes)
5. [Loops examples](5.loops)
6. [Conditionals examples](6.conditionals)
7. [Handlers example](7.handlers)
8. [Tags examples](8.tags)
9. [Roles examples](9.roles)
10. [Galaxy examples](10.galaxy)

## License

MIT License

See [LICENSE](https://github.com/aramirol/ansible-labs/blob/main/LICENSE) to see the full text.
