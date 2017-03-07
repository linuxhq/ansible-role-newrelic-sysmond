# ansible-role-newrelic-sysmond

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-newrelic-sysmond.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-newrelic-sysmond)

RHEL/CentOS - NewRelic nrsysmond

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    newrelic_sysmond_collector_host: collector.newrelic.com
    newrelic_sysmond_disable_docker: False
    newrelic_sysmond_disable_nfs: False
    newrelic_sysmond_ignore_reclaimable: True
    newrelic_sysmond_license_key: REPLACE_WITH_REAL_KEY
    newrelic_sysmond_logfile: /var/log/newrelic/nrsysmond.log
    newrelic_sysmond_loglevel: info
    newrelic_sysmond_pidfile: /var/run/newrelic/nrsysmond.pid
    newrelic_sysmond_runas: newrelic
    newrelic_sysmond_ssl: True

Additional variables available, not defined by default:

    newrelic_sysmond_cfgfile: /etc/newrelic/nrsysmond.cfg
    newrelic_sysmond_cgroup_root: /sys/fs/cgroup
    newrelic_sysmond_docker_cacert: /path/to/cacert
    newrelic_sysmond_docker_cert: /path/to/cert
    newrelic_sysmond_docker_cert_path: /path/to/certdir
    newrelic_sysmond_docker_connection: 'https://localhost:port'
    newrelic_sysmond_docker_key: /path/to/key
    newrelic_sysmond_host_root: /host
    newrelic_sysmond_hostname: "{{ inventory_hostname }}"
    newrelic_sysmond_labels:
      - Environment:Production
      - DataCenter:EastUS
    newrelic_sysmond_nrdaemon: /usr/sbin/nrsysmond
    newrelic_sysmond_proxy: 'user:password@host[:port]'
    newrelic_sysmond_ssl_ca_bundle: /path/to/ca/bundle
    newrelic_sysmond_ssl_ca_path: /path/to/cadir

## Dependencies

 * https://galaxy.ansible.com/linuxhq/newrelic/
 
## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.newrelic-sysmond
          newrelic_sysmond_hostname: "{{ inventory_hostname }}"
          newrelic_sysmond_license_key: xxxxxxxxxx        
    
## License

BSD

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
