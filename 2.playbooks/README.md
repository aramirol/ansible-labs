# Playbooks

## Check playbooks
We have some yaml files to check the syntax with `--syntax-check`.
```
ansible-playbook --syntax-check -i inventory 1.tasks.yaml
```

## Run tasks

### Run and check playbooks

Copy file from local to remote VM:
```
ansible-playbook -i inventory 1.tasks.yaml
```
Check that file was copied with:
```
ansible group2 -m command -a 'ls -lart /tmp' -i inventory
```

You will add content to the file upload last playbook:
```
ansible-playbook -i inventory 2.tasks.yaml
```

With `-C` or `--check` you run the playbook in test mode. In this example we test `--step` to approve each task separately:
```
ansible-playbook -i inventory 2.tasks.yaml -C
ansible-playbook -i inventory 2.tasks.yaml -C --step
```

New playbook to test modules:
```
ansible-playbook -i inventory 3.tasks.yaml --syntax-check
```

## Run blocks

### Install app and powered on its service
Test block module, used for related tasks. In this case we will install and powered on a service.
```
ansible-playbook -i inventory 4.block.yaml
```

Same as last playbook. This time adding the install and powered on apache service.
```
ansible-playbook -i inventory 5.block.yaml
```

