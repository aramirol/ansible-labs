# Loops examples

## Install packages with loops
```
ansible-playbook -i inventory 1.install.yaml
```

## Vars file
```
pkg: [vsftpd, apache2]
packages:
  - tree
  - watch
```

## Install packages using vars.yaml "pkg"
```
ansible-playbook -i inventory 2.install.yaml
```

## Install packages using vars.yaml "packages"
```
ansible-playbook -i inventory 3.install.yaml
```

## Using lists to create users
```
ansible-playbook -i inventory list.yam
```


