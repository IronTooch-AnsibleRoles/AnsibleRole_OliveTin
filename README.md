Role Name
=========

Installs the OliveTin Web Interface tool for system management. OliveTin's main repository is https://github.com/OliveTin/OliveTin  . This has only been tested on Ubuntu 20 server, but should work fine on other Debian-based systems.

Requirements
------------

Jinja2 is required to execute the template module on the control node. No other requirements known at this time. 

Role Variables
--------------

No variables are present currently, but leaving in the directory structure for future growth.

Dependencies
------------

Depends on the tag name and the URL to pull the deb file being the same. So if the tag to download structure changes, it will break grabbing the .deb

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

Author is IronTooch. 
