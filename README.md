Ansible Role zabbix_agent
=========

Installs zabbix agent and automatically tries to register client to zabbix server if autoregistering is supported.

Requirements
------------

None

Role Variables
--------------

#### `zabbix_server` (required)
zabbix server ip address(es), comma separated if multiple

#### `zabbix_version` (optional)
agent version to install

#### `zabbix_yum_repo_version` (optional)
yum repo version to use

#### `zabbix_apt_repo_version` (optional)
apt repo version to use

#### `zabbix_agent_hostname` (optional)
zabbix agent host name (typically hostname of the server)

#### `zabbix_auto_register_phrase` (optional)
auto register phrase

#### `zabbix_agent_timeout` (optional)
zabbix agent timeout value

#### `zabbix_agent_user_parameters` (optional)
list of user parameters


Dependencies
------------

Following dependencies are automatically included:

 * ansible-role-selinux. Clients must have necessary configurations for zabbix_agent configured in the inventory.


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: ansible-role-zabbix_agent, tags: zabbix_agent }

License
-------

Propriertary


Author Information
------------------

Tuomas Vallaskangas
