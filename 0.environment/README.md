# Environment

For this lab we will use 2 VMs. Be free to use more VMs if you want.
* ansible-server
* ansible-client

## Virtual Machines

Please, create all VMs and configure a static IP.

## Create Users

After that, create a remote user that we will use to connect via *ssh*:
```sh
$ sudo useradd -m -s /bin/bash ansible_user
```

## SSH Key

From ansible-server VM, create a ssh key and copy to all nodes:
```sh
$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/home/ansible_user/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /home/ansible_user/.ssh/id_rsa
Your public key has been saved in /home/ansible_user/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:xIlqWP9O/2Yv0y2lnktMQQzXBdNn8rqkMYMhvh2kHX0 ansible_user@ansible-client.casare.int
The key's randomart image is:
+---[RSA 3072]----+
|            .o=+o|
|       o .   oo.=|
|    . . +  .  .+.|
|   o o .. + . E..|
|  . o ..S= + ... |
|   .   .o + +oo .|
|        oo . Bo= |
|       o... *.=..|
|        . .+.==o |
+----[SHA256]-----+
```
```sh
$ copy-ssh-id ansible_user@ansible-server
$ copy-ssh-id ansible_user@ansible-client
```

## Edit Sudoers

You need the remote user to have superuser permissions without a password. To do this edit `/etc/sudoers` and copy this lines:
```sh
# Same things without a password
ansible_user    ALL=(ALL)       NOPASSWD: ALL
```

