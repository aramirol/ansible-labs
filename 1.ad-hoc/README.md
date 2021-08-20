# Ad-hoc commands

## Test ping module

Simple command to test ansible modules.

```
ansible group-all -i ../inventory -m ping
```

## Test module that needs become root

Using become to grant root permissions via command line.

```
ansible group-2 -i ../inventory -m apt -a "name=* state=latest" -b
```
