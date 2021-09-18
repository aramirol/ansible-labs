# ansible-labs

![](https://img.shields.io/badge/ansible-v2.10.13-white?logo=ansible)
![](https://img.shields.io/badge/ubuntu-20.04-critical?logo=ubuntu)

<img src="images/ansible-header-1024x640.png" width="20%" />

## Prerequisites

For your control node (the machine that runs Ansible), you can use any machine with Python 2 (version 2.7) or Python 3 (versions 3.5 and higher) installed. ansible-core 2.11 and Ansible 4.0.0 will make Python 3.8 a soft dependency for the control node, but will function with the aforementioned requirements. ansible-core 2.12 and Ansible 5.0.0 will require Python 3.8 or newer to function on the control node. Starting with ansible-core 2.11, the project will only be packaged for Python 3.8 and newer. This includes Red Hat, Debian, CentOS, macOS, any of the BSDs, and so on.

Although you do not need a daemon on your managed nodes, you do need a way for Ansible to communicate with them. For most managed nodes, Ansible makes a connection over SSH and transfers modules using SFTP. If SSH works but SFTP is not available on some of your managed nodes, you can switch to SCP in ansible.cfg. For any machine or device that can run Python, you also need Python 2 (version 2.6 or later) or Python 3 (version 3.5 or later).

## Installation

Ansible can be installed on many systems with pip, the Python package manager.

### Prerequisites: Installing `pip`
If pip is not already available on your system, run the following commands to install it:

```sh
$ curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
$ python get-pip.py --user
```
You may need to perform some additional configuration before you are able to run Ansible. See the Python documentation on installing to the user site for more information.

### Installing Ansible with `pip`

Once pip is installed, you can install Ansible 1:
```sh
$ python -m pip install --user ansible
```

In order to use the paramiko connection plugin or modules that require paramiko, install the required module 2:
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
