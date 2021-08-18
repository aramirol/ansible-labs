# Ad-hoc commands

* Test ping module
  ```
  ansible group-all -i ../inventory -m ping
  ```
* Test module that needs become root
  ```
  ansible group-2 -i ../inventory -m apt -a "name=* state=latest" -b
  ```
