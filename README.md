ansible-beats
====================

[![Build Status](https://travis-ci.org/lsst-sqre/ansible-beats.svg?branch=master)](https://travis-ci.org/lsst-sqre/ansible-beats)

Install and configure Elastic [beats](https://www.elastic.co/products/beats) v5 for LSST SQuaRE infrastructure.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: lsst-sqre.beats }

Variables
---------

For complete documentation on configuration options see the [metricbeat](https://www.elastic.co/guide/en/beats/metricbeat/master/index.html), [filebeat](https://www.elastic.co/guide/en/beats/filebeat/master/index.html) and [packetbeat](https://www.elastic.co/guide/en/beats/packetbeat/master/index.html) documentation.

`beats_package_name` *(default "metricbeat")* The package name of the beat. Valid options are "metricbeat", "filebeat" "packetbeat" or "heartbeat".

`beats_package_version` *(default "5.2.2")* The package version of the beat.

`beats_install` *(default true)* Whether to install the beat.

`beats_config_file` * set url to the desired configuration file

Acknowledgements
----------------

This role is based on [Jmatt's](https://galaxy.ansible.com/jmatt/beats/) Ansible Galaxy role "beats"(https://galaxy.ansible.com/cyverse/beats/). It is a more complete implementation and less opinionated than this role. But it doesn't support v5 or follow the variable naming convention my roles follow. Thus this new role.


License
-------

The MIT License. See the [LICENSE file](https://github.com/lsst-sqre/ansible-beats/blob/master/LICENSE).
