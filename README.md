ansible-epel
============

Ansible role installs and enables EPEL for RHEL and CentOS systems.

You will want to import this role conditionally, perhaps as such:

	- hosts: all
	  roles:
	    - { role: ansible-epel, when: ansible_os_family == 'RedHat' }

This will import the correct GPG package signing key for your release, and add the correct EPEL repositor for it.
