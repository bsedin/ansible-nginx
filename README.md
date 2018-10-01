# nginx ansible role

Create `./library` directory in your ansible project:

```
mkdir ./library
```

And configure `ansible.cfg`:

```
[defaults]
roles_path = ./library
```

Add submodule:

```
git submodule add git@github.com:kressh/ansible-nginx.git library/nginx
```

See `defaults/main.yml`

Use role:

```yaml
---
- hosts: yourserver.io
  remote_user: ansible
  become: true
  roles:
    - nginx
```
