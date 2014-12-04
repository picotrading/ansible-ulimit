sysctl
======

Role which helps to manage `ulimit` configuration.


Example
-------

```
---

# Example of how to use the role
- hosts: myhost
  vars:
    ulimit_config:
      - domain: '*'
        type: soft
        item: core
        value: 0
      - domain: '*'
        type: hard
        item: rss
        value: 10000
  roles:
    - ulimit
```


Role variables
--------------

List of variables used by the role:

```
# Default ulimit configuration
ulimit_config: []

# Default limits.conf location
ulimit_config_location: /etc/security/limits.conf
```


License
-------

MIT


Author
------

Jiri Tyr
