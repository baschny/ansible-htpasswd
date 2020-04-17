Create an htpasswd
==================

Ansible role that uses `htpasswd` module to create a file with user/password
hashes to be used by Apache / Nginx / etc.

This will automatically install requirements (passlib).

Configuration
-------------

Possible variables:

* `htpasswd_file`: The file to save
* `htpasswd_file_owner`: optional owner (default=root)
* `htpasswd_file_group`: optional group (default=root)
* `htpasswd_file_mode`: optional mode (default=0640)
* `htpasswd_users`: list with keys `name` and `password`

Example
-------
```
  - role: baschny.htpasswd
    vars:
      htpasswd_file: /etc/htaccess
      htpasswd_users:
        - name: dev
          password: dev
        - name: admin
          password: admin
```

License
---

Licensed under the MIT License. See the LICENSE file for details.

Feedback, bug-reports, requests
---

Use the [github issue tracker](https://github.com/baschny/ansible-htpasswd/issues).
