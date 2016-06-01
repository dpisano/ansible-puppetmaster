Ansible-puppetmaster
------------------------

Updates are still a work in progress.

Install and configure puppetmaster via ansible!

Actions
--------

Everything that will get a real puppetmaster up and running.

Install
* puppetserver (4.5.0)
* ~~puppetdb & puppetdb-terinus (2.0.0)~~
* hiera
* facter
* ~~r10k (1.2.1)~~
* git
* puppet-lint

Configure puppetmater
* with puppetdb via ssl (:8081)
* ~~hieradata in /etc/puppet/environments~~
* ~~r10k will sync hieradata~~

Installing
------------

	$ git clone git@github.com:dpisano/ansible-puppetmaster.git
	$ mkvirtualenv ansible
	$ pip install ansible

Running
---------

Install a puppetmaster on a node called 'puppet' (change the hosts.ini)

	$ ansible-playbook -i hosts.ini install.yaml


Testing
---------

The tests assume that you have ansible and docker installed on your
local machine.  By running `./tests/run_tests.sh` a new machine
will be created and ansible will take over and install the puppetmaster.

The `ubuntu:14.04` is also assumed to be installed locally.

Buildout
----------
serverspec will make sure that everything is install and configured as
it should be.
