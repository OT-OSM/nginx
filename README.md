Nginx
=========
[![Opstree Solutions][opstree_avatar]][opstree_homepage]<br/>[Opstree Solutions][opstree_homepage]

[opstree_homepage]: https://opstree.github.io/
[opstree_avatar]: https://img.cloudposse.com/150x150/https://github.com/opstree.png
 
An ansible role to install nginx. We are using nginx hardening as well in this role. 

Version History
---------------

|**Date**| **Version**| **Description**| **Changed By** |
|----------|---------|---------------|-----------------|
|**April '30** | v.1.0 | Initial Draft | Kavit Narwal |

Supported OS
------------
  * CentOS:7
  * CentOS:6
  * Ubuntu:bionic
  * Ubuntu:xenial
  * AWS AMI

Requirements
------------

No pre-requirment need for this ansible roles. 

Role Variables
--------------

We are using below mention default variables for nginx configuration.

|**Variables**| **Default Values**|
|-------------|-------------------|
| nginx_port  | 80 |
| nginx_root_dir| /etc/nginx | 
| nginx_config_conf_dir | /etc/nginx/conf.d |
| nginx_default_conf | /etc/nginx/conf.d/default.conf |
| nginx_service_name | nginx |

We are using below mention variables for nginx hardening.

- nginx_client_body_buffer_size
- nginx_remove_default_site
- nginx_client_max_body_size
- nginx_keepalive_timeout
- nginx_server_tokens
- nginx_client_header_buffer_size
- nginx_large_client_header_buffers
- nginx_client_body_timeout
- nginx_client_header_timeout
- nginx_send_timeout
- nginx_limit_conn_zone
- nginx_limit_conn
- nginx_add_header
- nginx_ssl_protocols
- nginx_ssl_ciphers
- nginx_ssl_prefer_server_ciphers
- nginx_dh_param
- nginx_dh_size

Define above mention variables value as per your requirments. Otherwise it will take default value. 

Inventory
----------
An inventory should look like this for nginx setup:-
```ini
[nginx]                 
192.168.1.198    ansible_user=ubuntu
192.168.2.208    ansible_user=centos 
```

Example Playbook
----------------  
Here is an example playbook:-
```yml
---
- hosts: nginx
  roles:
    - role: osm_nginx
      become: yes
```
Usage
-----
For using this role you have to execute playbook only
```shell
ansible-playbook -i hosts site.yml
```

References
-----------------------
- **[web server](https://www.nginx.com/)**


Author Information
------------------

**[Kavit Narwal](mailto:kavit.narwal@opstree.com)**
