# ansible-takahe

[TBC]

Tested with Ubuntu 22.04.

## Cheatsheet

Setup:

```
$ pip install ansible
$ ansible-galaxy install -r requirements.yml
```

Prepare:

- Provision machine (no automated provisioning is provided)
- Open ports 80 and 443 (no automatic firewall configuration is provided)
- Point A DNS record to machine IP (no automatic DNS configuration is provided)

Test:

```
$ cp hosts.template inventory/production  # And edit accordingly
$ ansible all -i inventory/production --list-hosts
$ ansible all -i inventory/production -u root -m ping
```

Execute:

```
$ ansible-playbook -i inventory/production -u root playbooks/configure.yml
```

Verify:

- Launch an HTTPS server on appropriate port (for example https://gist.github.com/astrojuanlu/13c2803bab300d2a8f0e117475a7a1cc)
- Point browser to `https://{domain}`
