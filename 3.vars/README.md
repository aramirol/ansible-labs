# Vars examples

## Create user with variables inside the playbook.
```sh
ansible-playbook -i inventory user.yaml
```
```sh
ansible -i inventory group2 -m command -a 'ls -l /home'
```
```sh
ansible -i inventory group2 -m command -a 'id ansibleuser1'
```

## Create user with variables outside the playbook.
```sh
ansible-playbook -i inventory 2.user.yaml
```
```sh
ansible -i inventory group2 -m command -a 'id ansibleuser2'
```

## Using vars arrays
```sh
ansible-playbook -i inventory array.yaml
```

## Using register and debug
```sh
ansible-playbook -i inventory register.yaml
```

## Using facts
```sh
ansible group2 -i inventory -m setup
```
```sh
ansible-playbook -i inventory facts.yaml
```


