# Sherpany Vagrant Build Environment

This Vagrant setup is for building the Sherpany applications.
There is only one VM defined, which contains several packages needed
for building and packaging applications. The VM is not connected to
the Puppet server.
During provisioning, the GPG keyring from the host is exported into `gpgkey.asc`
and imported into the keyring of the vagrant user.

To see which packages are installed, have a look at `manifests/default.pp`

## Requirements

* GPG installed and key ready in the keyring on the host
* [Vagrant](http://vagrantup.com) installed on local machine

## Setup

1. Clone this git repository `git clone git@git.vshn.net:agilentia/buildvm.git`
1. Change to Vagrant directory `cd buildvm`
1. Start Vagrant environment and wait till everything is installed `vagrant up`

## Usage

1. Login to Vagrant environment `vagrant ssh`
1. Build and package your application
