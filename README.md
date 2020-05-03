Shlink
=========

Deploy shlink with docker

Requirements
------------

- geerlingguy.docker

Role Variables
--------------

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
      roles:
         - { role: fgierlinger.shlink, tagsx: shlink }

License
-------

GPL-3.0

Author Information
------------------

Frédéric Gierlinger
