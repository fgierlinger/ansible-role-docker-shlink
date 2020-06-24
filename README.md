Shlink
=========

Deploy shlink with docker

Requirements
------------

- geerlingguy.docker

Role Variables
--------------

All three variables `shlink_domain_host`, `shlink_domain_port` and `shlink_domain_schema` 
are used to dynamically add the shlink server to the shlink web instance.

* `shlink_domain_host` hostname under which the shlink server can be reached

* `shlink_domain_port` port under which the shlink api can be accessed

* `shlink_domain_schema` http or https


```
shlink_image: shlinkio/shlink
shlink_image_tag: latest
shlink_env: []
shlink_publish_port: 8080

shlink_web_image: shlinkio/shlink-web-client
shlink_web_image_tag: latest
shlink_web_env: []
shlink_web_publish_port: 80

shlink_server_json_path: /root/shlink_server.json
```

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      vars:
        shlink_domain_host: shlink.server.example.com
        shlink_domain_port: 443
        shlink_domain_schema: https
      roles:
         - { role: fgierlinger.shlink, tagsx: shlink }

License
-------

GPL-3.0

Author Information
------------------

Frédéric Gierlinger
