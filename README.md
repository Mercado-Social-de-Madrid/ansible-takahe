# ansible-takahe

[TBC]

## Cheatsheet

Setup:

```
$ pip install ansible
$ ansible-galaxy install -r requirements.yml
```

Verify:

```
$ cp hosts.template hosts  # And edit accordingly
$ ansible all -i hosts -m ping
```

Execute:

```
$ ansible-playbook -i hosts playbooks/main.yml
```
