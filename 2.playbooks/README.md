# Playbooks

## Check playbooks
We have some yaml files to check the syntax with `--syntax-check`.
```
ansible-playbook --syntax-check -i inventory 1.playbook.yaml
```

## Run with 1.playbook.yaml
Copy file from local to remote VM:
```
ansible-playbook -i inventory 1.playbook.yaml
```
Check that file was copied with:
```
ansible group2 -m command -a 'ls -lart /tmp' -i inventory
```
## Run with 2.playbook.yaml
You will add content to the file upload last playbook:
```
ansible-playbook -i inventory 2.playbook.yaml
```
With `-C` or `--check` you run the playbook in test mode. In this example we test `--step` to approve each task separately:
```
ansible-playbook -i inventory 2.playbook.yaml -C
ansible-playbook -i inventory 2.playbook.yaml -C --step
```

## Run with 3.playbook.yaml
New playbook to test modules:
```
ansible-playbook -i inventory 3.playbook.yaml --syntax-check
```

## Run with 4.playbook.yaml
Test block module, used for related tasks. In this case we will install and powered on a service.
```
ansible-playbook -i inventory 4.playbook.yaml
```

## Run with 5.playbook.yaml
Same as last playbook. This time adding the install and powered on apache service.
```
ansible-playbook -i inventory 5.playbook.yaml
```

