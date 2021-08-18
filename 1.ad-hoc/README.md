# Ad-hoc commands

* Test ping module
  ```
  ansible grupo-todos -i ../inventory -m ping
  ```
* Test module that needs become root
  ```
  ansible grupo-2 -i ../inventory -m apt -a "name=* state=latest" -b
  ```
