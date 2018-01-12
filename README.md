ansible-metricbeat
====================

[![Build Status](https://travis-ci.org/lsst-sqre/ansible-beats.svg?branch=master)](https://travis-ci.org/lsst-sqre/ansible-beats)

Install and configure Elastic [metricbeat](https://www.elastic.co/products/beats).

Example Playbook
----------------

    - hosts: servers
      roles:
        - MattiDeGrauwe.metricbeat
      vars: 
      	- beats_config_file: "path to configuration file"   	
Variables
---------

For complete documentation on configuration options see the [metricbeat](https://www.elastic.co/guide/en/beats/metricbeat/master/index.html), [filebeat](https://www.elastic.co/guide/en/beats/filebeat/master/index.html) and [packetbeat](https://www.elastic.co/guide/en/beats/packetbeat/master/index.html) documentation.

* `beats_package_version` *(default "5.2.2")* The package version of the beat.

* `beats_install` *(default true)* Whether to install the beat.

* `beats_config_file` *(required)* set url to the desired configuration file

Metricbeat comes packaged with a script that you can use to import the example dashboards, visualizations, and searches for Metricbeat. The script also creates an index pattern, metricbeat-*, for Metricbeat.

* `beats_dashboard_output_url` *(default "localhost:9200")* Initializes the host where the output of the predefined dashboards should be generated.


Acknowledgements
----------------

This role is based on [Jmatt's](https://galaxy.ansible.com/jmatt/beats/) Ansible Galaxy role "beats". It is a more complete implementation and less opinionated than this role. But it doesn't support v5 or follow the variable naming convention my roles follow. Thus this new role.


License
-------

The MIT License. See the [LICENSE file](https://github.com/lsst-sqre/ansible-beats/blob/master/LICENSE).
