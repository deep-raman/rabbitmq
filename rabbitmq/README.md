rabbitmq installation
=====================

This role installs and configures the rabbitmq 

Role Variables
--------------

	- erlang_repo_name
	- erlang_repo_url
	- rabbitmq_repo_script
	- rabbitmq_package

Example Playbook
----------------

Rabbitmq yml file to install it on servers.

 
    - hosts: all
      roles:
         - { role: rabbitmq, tags: "rabbitmq" }
      become: true

To install only rabbitmq run the following command :

	ansible-playbook -i [host_file or ip] install_rabbitmq.yml --tags install_rabbitmq

To install and configure :

	ansible-playbook -i [host_file or ip] install_rabbitmq.yml --tags install_and_configure_rabbitmq


Tested on
---------

	- Debian 9

Vagrant test
------------

Just run vagrant up in tests directory that will execute and configure the rabbitmq on virtual machine. Once the execution is finished you can login to : http://localhost:15672 with used and pass radmin.

Requirements :

	- vagrant
	- virtualbox
	- ansible

Author Information
------------------

	Raman Deep
	April 2018
	deep.raman85@gmail.com
