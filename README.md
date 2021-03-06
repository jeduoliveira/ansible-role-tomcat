Tomcat For LumisXP
=========
[![Build Status](https://travis-ci.org/jeduoliveira/ansible-role-tomcat.svg?branch=master)](https://travis-ci.org/jeduoliveira/ansible-role-tomcat)

Install Tomcat For LumisXP  

Requirements
------------

none.

Role Variables
--------------

    tomcat_name: tomcat
    tomcat_directory: /opt

    tomcat_user:  tomcat
    tomcat_group: tomcat
    tomcat_xms: 512M
    tomcat_xmx: 1024M

    tomcat_maxThreads_http: 6
    tomcat_maxThreads_ajp: 80
    tomcat_valve_internalProxies: "192\\.168\\.\\d{1,3}\\.\\d{1,3}"

    tomcat_heapdump_enabled: false
    tomcat_heapdump_directory: /opt/heapdump/
    tomcat_g1gc_enabled: false

    tomcat_gc_log_enabled: false
    tomcat_gc_log_directory: /opt/logs/gc
    tomcat_gc_log_file: "{{ tomcat_gc_log_directory }}/gc.log"

    tomcat_jmx_enabled: false

Dependencies
------------

jeduoliveira.zulu_openjdk

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: jeduoliveira.tomcat
          tomcat_version: 9
          tomcat_release: 9.0.19

License
-------

BSD

Author Information
------------------

This role was created in 2019 by [Jorge Eduardo](https://www.linkedin.com/in/jorgeeduardo/)
