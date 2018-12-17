Role Name
=========

Ansible role to install a custom-packaged RPM of Ruby that is hosted on the UCLA Library's internal yum repository on a RHEL system.

Requirements
------------

Is is expected the system has the UCLA Library internal yum repository configured and has access to download files from the repository.

Role Variables
--------------

* ruby_version - define the version of ruby to install on the system - this must match a version available in the UCLA Library yum repository


Dependencies
------------

* `uclalib_role_uclalibrepo` should have already been run on the system.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: uclalib_role_ruby, ruby_version: '2.5.1' }
