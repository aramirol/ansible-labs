# Vars examples

## Create user with variables inside the playbook.
```
ansible-playbook -i inventory user.yaml
```
```
ansible -i inventory group2 -m command -a 'ls -l /home'
```
```
ansible -i inventory group2 -m command -a 'id ansibleuser1'
```

## Create user with variables outside the playbook.
```
ansible-playbook -i inventory 2.user.yaml
```
ansible -i inventory group2 -m command -a 'id ansibleuser2'
```


