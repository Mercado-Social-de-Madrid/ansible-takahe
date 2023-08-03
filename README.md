# ansible-takahe

[TBC]

## Cheatsheet

Setup:

```
$ pip install ansible
$ ansible-galaxy install -r requirements.yml
```

Prepare:

- Provision machine (tested with Ubuntu 22.04)
- Open ports 80 and 443
- Point A DNS record to machine IP

Test:

```
$ cp hosts.template hosts  # And edit accordingly
$ ansible all -i hosts -m ping
```

Execute:

```
$ ansible-playbook -i hosts playbooks/main.yml
```

Verify:

- Launch an HTTPS server on appropriate port (for example https://gist.github.com/astrojuanlu/13c2803bab300d2a8f0e117475a7a1cc)
- Point browser to `https://{domain}`
