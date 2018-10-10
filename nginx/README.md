Role Name
=========

This role install nginx-1.12 version on CentOS6,Centos7,Ubuntu14,Ubuntu16 and AWS AMI. We are using nginx hardening as well in this role. 

Requirements
------------

No pre-requirment need for this ansible roles. 

Role Variables
--------------

We are using below mention variables in this role.

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

Dependencies
------------

No dependency required for this ansible role.

Example Playbook
----------------

In tests directory of this roles, We have a test.yml playbook. In which we define hosts details.

- hosts: localhost
  remote_user: root
  roles:
    - nginx

How to run this Role
--------------------



Author Information
------------------

Name: Kavit Narwal
MailID: kavit.narwal@opstree.com


