# Change-line-in-file-with-ansible


## Change simple line in /etc/hosts
```bash

---

- hosts: jeff
  tasks:
    - name: Modify line in hosts katello.allin.com.br
      lineinfile:
        path: /etc/hosts
        regexp: '(katello.*)'
        line: '10.0.0.1 katello.allin.com.br'
        backrefs: yes
```
