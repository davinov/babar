# Babar
Code that serves your drinking.

## Set up

### Set up the development server
- Download and install [Virtualbox](https://www.virtualbox.org/) and [Vagrant](http://www.vagrantup.com/downloads.html)
- Install nfs (for shared folders): `sudo apt-get install nfs-kernel-server`
- Start the virtual machine: `vagrant up`
- Add `199.199.199.87   babar.local` to `/etc/hosts` to access your server from [babar.local](http://babar.local).

### Provision the development server
While running `vagrant up` for the first time, vagrant tries to provision automatically your virtual machine
using Ansible. You can always re-provision it with `vagrant provision`.

Prerequisites:

- Install Python and it's package manager Pip: `sudo apt-get install python-dev python-pip`
- Install [Ansible](www.ansible.com): `sudo pip install ansible`

If you have not yet instanciate any subproject, you should see an (ugly) 404 error when accessing to
[babar.local](http://babar.local) !

### Instanciate diferent subprojects
Independant subprojects are separate git submodules. They're provisionned separatly thanks to roles defined in their
folder.
Current subproject are:
- API
- Frontend

## Usage

## Contributors
Contributors are encouraged to include their names for posterity and worldwide ackowledgment of their belonging to
the Telecom bar'iTech cutting-edge family:

- [David Nowinsky (@davinov)](http://david.nowinsky.net)

