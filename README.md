# Babar
Code that serves your drinking.

## Set up

### Set up the development server
- Download and install [Virtualbox](https://www.virtualbox.org/) and [Vagrant](http://www.vagrantup.com/downloads.html)
- Install nfs (for shared folders): `sudo apt-get install nfs-kernel-server`
- Start the virtual machine: `vagrant up`
- Add `199.199.199.87   babar.local` to `/etc/hosts` to access your server from [babar.local](http://babar.local).

## Provision the development server
While running `vagrant up` for the first time, vagrant tries to provision automatically your virtual machine
using Ansible. You can always re-provision it with `vagrant provision`.
Prerequisites:
- Install Python and it's package manager Pip: `sudo apt-get install python-dev python-pip`
- Install [Ansible](www.ansible.com): `sudo pip install ansible`

## Usage

### Contributors

