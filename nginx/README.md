Role Name
=========

This role install nginx-1.12 version on CentOS6,Centos7,Ubuntu14,Ubuntu16 and AWS AMI.

Requirements
------------

No pre-requirment need for this ansible roles. 

Role Variables
--------------

We don't use any variables in this roles. Because this role is only for nginx installation. 

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


