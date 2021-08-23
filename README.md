Satellite Receptor Installer
============================

An installer playbook for setting up Satellite with a Receptor node connected to console.redhat.com

Requirements
------------

This role requires Receptor be installed on the system.

Role Variables
--------------

* `install_receptor_from_rpm` - Whether you want the role to install Receptor for you (default: `yes`)
* `satellite_url` - The base URL for the Satellite API (default: `https://satellite.example.com/`)
* `satellite_user` - The user to connect to the Satellite API with (default: `fifi_user`)
* `satellite_password` - The password to authenticate against the Satellite API with (default: `0p3ns3s4m3!`)
* `satellite_ca_file` - The path to the CA file to validate Satellite's certificate (default: `/etc/pki/tls/certs/ca-bundle.crt`)
* `satellite_validate_certs` - Whether to validate the Satellite certificate is trusted (default: `yes`)
* `receptor_config_dir` - The path to Receptor's configuration files (default: `/etc/receptor`)
* `receptor_data_dir` - The path to Receptor's data files (default: `/var/data/receptor`)
* `receptor_packages` - The packages required to be installed for Receptor to work (default: `receptor` and `python3-receptor-satellite`)
* `c_rh_c_host` - The API endpoint to connect to for cloud.redhat.com (default: `cert.cloud.redhat.com`)
* `skip_satellite_org_id_list` - A list of Satellite organizations to skip during setup
* `source_display_name` - The name for this Satellite in Sources on cloud.redhat.com (default: the hostname of the `satellite_url`)
* `http_proxy` - HTTP Proxy to used when talking to cloud.redhat.com (default: "", e.g. do not use any proxy)

License
-------

GPLv3

Author Information
------------------

This role is written and maintained by Red Hat.
