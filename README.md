Role Name
=========

Installs the OliveTin Web Interface tool for system management. OliveTin's main repository is https://github.com/OliveTin/OliveTin  . This has only been tested on Ubuntu 20 server, but should work fine on other Debian-based systems.

![Ansible Role](https://img.shields.io/ansible/role/57702)
![Galaxy Downloads](https://img.shields.io/badge/dynamic/json?color=blueviolet&label=Galaxy%20Downloads&query=%24.download_count&url=https%3A%2F%2Fgalaxy.ansible.com%2Fapi%2Fv1%2Froles%2F57702%2F%3Fformat%3Djson) 
![GitHub all releases](https://img.shields.io/github/downloads-pre/irontooch/AnsibleRole-OliveTin/total)
![GitHub repo size](https://img.shields.io/github/repo-size/IronTooch/AnsibleRole-OliveTin)
![GitHub issues](https://img.shields.io/github/issues-raw/Irontooch/AnsibleRole-OliveTin)
![GitHub Open PRs](https://badgen.net/github/open-prs/Irontooch/AnsibleRole-OliveTin)
![GitHub last commit](https://img.shields.io/github/last-commit/IronTooch/AnsibleRole-OliveTin)
![GitHub Maintained](https://img.shields.io/maintenance/yes/2022)
![GitHub](https://img.shields.io/github/license/IronTooch/AnsibleRole-OliveTin)
![Forks](https://img.shields.io/github/forks/Irontooch/AnsibleRole-OliveTin.svg)
![Stars](https://img.shields.io/github/stars/Irontooch/AnsibleRole-OliveTin.svg)
![Watchers](https://img.shields.io/github/watchers/Irontooch/AnsibleRole-OliveTin.svg)
![Follow](https://img.shields.io/github/followers/IronTooch.svg?style=social&label=Follow&maxAge=2592000)

Requirements
------------

Jinja2 is required to execute the template module on the control node. No other requirements at this time. 

Role Variables
--------------

default_port: The port OliveTin will listen on. Defaults to 1337

log_level: The log level for OliveTin. Defaults to INFO

config_data: An override of the default configuration file. 


Future Work
-----------
Make the override of the default configuration file a bit more effective. Maybe a Block in File, so it doesn't override the log and default port variables. 

Dependencies
------------

Depends on the tag name and the URL to pull the deb file being the same. So if the tag to download structure changes, it will break grabbing the .deb

Example Playbook
----------------

Basic installation with default configuration file on default port (1337)
```
  - hosts: servers
    roles:
      - role: irontooch.olivetin
```

Basic installation with default configuration file and different listening port
```
  - hosts: servers
    roles:
      - role: irontooch.olivetin
        vars:
          default_port: 1344
```

Installation with new configuration file
```
  - hosts: servers
    roles:
      - role: irontooch.olivetin
        vars:
          config_data: "{{ lookup('file', 'MY_NEW_CONFIG_FILE.txt')}}"
```
License
-------

BSD

Author Information
------------------

Author is IronTooch. 
