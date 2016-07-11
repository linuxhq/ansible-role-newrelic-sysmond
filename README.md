# ansible-role-newrelic-sysmond

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-newrelic-sysmond.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-newrelic-sysmond)

RHEL/CentOS - NewRelic nrsysmond

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    newrelic_sysmond_logfile: /var/log/newrelic/nrsysmond.log
    newrelic_sysmond_loglevel: info
    newrelic_sysmond_runas: newrelic

You must set the following variable for the role to execute properly:
 
    newrelic_sysmond_license_key: xxxxxxxxxx

Additional variables available, not set by default:

    newrelic_sysmond_cfgfile
    newrelic_sysmond_cgroup_root
    newrelic_sysmond_collector_host
    newrelic_sysmond_disable_docker
    newrelic_sysmond_disable_nfs
    newrelic_sysmond_docker_cacert
    newrelic_sysmond_docker_cert
    newrelic_sysmond_docker_cert_path
    newrelic_sysmond_docker_connection
    newrelic_sysmond_docker_key
    newrelic_sysmond_host_root
    newrelic_sysmond_hostname
    newrelic_sysmond_ignore_reclaimable
    newrelic_sysmond_labels
    newrelic_sysmond_nrdaemon
    newrelic_sysmond_pidfile
    newrelic_sysmond_proxy
    newrelic_sysmond_ssl
    newrelic_sysmond_ssl_ca_bundle
    newrelic_sysmond_ssl_ca_path

## Dependencies

 * https://galaxy.ansible.com/linuxhq/newrelic/
 
## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.newrelic-sysmond
          newrelic_sysmond_disable_docker: True
          newrelic_sysmond_disable_nfs: True
          newrelic_sysmond_hostname: "{{ inventory_hostname }}"
          newrelic_sysmond_labels:
            - Environment:Production
            - DataCenter:EastUS
          newrelic_sysmond_license_key: xxxxxxxxxx        
          newrelic_sysmond_pidfile: /var/run/newrelic/nrsysmond.pid
          newrelic_sysmond_ssl: True
    
## License

BSD

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
