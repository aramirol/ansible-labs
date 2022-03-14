# Tags examples

## Testing tags
```sh
ansible-playbook -i inventory 1.tag.yaml
```
```sh
ansible-playbook -i inventory 2.tag.yaml
```
```sh
ansible-playbook -i inventory 2.tag.yaml --tags dev
```
```sh
ansible-playbook -i inventory 2.tag.yaml --skip-tags dev
```
```sh
ansible-playbook -i inventory 3.main.yaml --tags=qa,vars
```

## Testing rescue
```sh
ansible-playbook -i inventory 4.rescue.yaml
```

