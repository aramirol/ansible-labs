# Loops examples

## Install packages with loops
```sh
ansible-playbook -i inventory 1.install.yaml
```

## Vars file
```yml
pkg: [vsftpd, apache2]
packages:
  - tree
  - watch
```

## Install packages using vars.yaml "pkg"
```sh
ansible-playbook -i inventory 2.install.yaml
```

## Install packages using vars.yaml "packages"
```sh
ansible-playbook -i inventory 3.install.yaml
```

## Using lists to create users
```sh
ansible-playbook -i inventory list.yam
```


