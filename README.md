# ansible-role-newrelic_sysmond

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-newrelic_sysmond.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-newrelic_sysmond)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-newrelic_sysmond-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/newrelic_sysmond)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

RHEL/CentOS - NewRelic nrsysmond

## Requirements

This role requires that you have the newrelic repository installed.

 * https://galaxy.ansible.com/linuxhq/newrelic/

## Role Variables

Available variables are listed below, along with default values:

    newrelic_sysmond_cfgfile: ''
    newrelic_sysmond_cgroup_root: /sys/fs/cgroup
    newrelic_sysmond_collector_host: collector.newrelic.com
    newrelic_sysmond_disable_docker: false
    newrelic_sysmond_disable_nfs: false
    newrelic_sysmond_docker_cacert: ''
    newrelic_sysmond_docker_cert: ''
    newrelic_sysmond_docker_cert_path: ''
    newrelic_sysmond_docker_connection: ''
    newrelic_sysmond_docker_key: ''
    newrelic_sysmond_host_root: /host
    newrelic_sysmond_hostname: "{{ inventory_hostname }}"
    newrelic_sysmond_ignore_reclaimable: true
    newrelic_sysmond_labels: []
    newrelic_sysmond_license_key: REPLACE_WITH_REAL_KEY
    newrelic_sysmond_logfile: /var/log/newrelic/nrsysmond.log
    newrelic_sysmond_loglevel: info
    newrelic_sysmond_nrdaemon: ''
    newrelic_sysmond_pidfile: /var/run/newrelic/nrsysmond.pid
    newrelic_sysmond_proxy: ''
    newrelic_sysmond_runas: newrelic
    newrelic_sysmond_ssl: true
    newrelic_sysmond_ssl_ca_bundle: ''
    newrelic_sysmond_ssl_ca_path: ''

## Dependencies

None
 
## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.newrelic_sysmond
          newrelic_sysmond_license_key: a62ae178defeb26006cec54baf5055a4
          newrelic_sysmond_labels:
            - Environment:Production
            - DataCenter:EastUS
          newrelic_sysmond_proxy: 'fred:secret@proxy.mydomain.com:8181'
    
## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
