# Tags examples

## Testing tags
```
ansible-playbook -i inventory 1.tag.yaml
```
```
ansible-playbook -i inventory 2.tag.yaml
```
```
ansible-playbook -i inventory 2.tag.yaml --tags dev
```
```
ansible-playbook -i inventory 2.tag.yaml --skip-tags dev
```
```
ansible-playbook -i inventory 3.main.yaml --tags=qa,vars
```

## Testing rescue
```
ansible-playbook -i inventory 4.rescue.yaml
```

