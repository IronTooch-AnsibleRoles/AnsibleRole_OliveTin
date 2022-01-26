Role Name
=========

Installs the OliveTin Web Interface tool for system management. OliveTin's main repository is https://github.com/OliveTin/OliveTin  . This has only been tested on Ubuntu 20 server, but should work fine on other Debian-based systems.

Requirements
------------

Jinja2 is required to execute the template module on the control node. No other requirements known at this time. 

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

  - hosts: servers
    roles:
      - role: irontooch.olivetin


Basic installation with default configuration file and different listening port
  - hosts: servers
    roles:
      - role: irontooch.olivetin
        vars:
          default_port: 1344

Installation with new configuration file
  - hosts: servers
    roles:
      - role: irontooch.olivetin
        vars:
          config_data: "{{ lookup('file', 'MY_NEW_CONFIG_FILE.txt')}}"

License
-------

BSD

Author Information
------------------

Author is IronTooch. 
