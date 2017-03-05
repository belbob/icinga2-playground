# icinga2-playground
This is an Ansible project with a development environment powered by Vagrant, to play with Icinga2.

This project sets up:

* 1 virtual machine with centos/7
* MariaDB and phpMyAdmin
* php 7.1
* Icinga2

This project is intended as a demo/playground for a monitoring-introductory , teaching git, vagrant and ansible, in the most simple way, and still useable in my classroom. Surely , this playbook can still be improved, but this way it is manageable in my classroom with my students.

## Dependencies

I use as host a Fedora workstation, make sure you have installed :

- vagrant
- vagrant-libvirt
- vagrant-hostmanager
- ansible (ver. 2+)
- git

## Getting started

When cloning, choose a more suiteable  name for the target directory!

```ShellSession
$ git clone https://github.com/belbob/icinga2-playground.git my-icinga2-playground
```
After cloning, it's best to remove the `.git` directory and initialise a new repository. The history of the code is most probably irrelevant for your icinga2-playground project...

### Installation glpi-playground with Vagrant

Open a terminal, go to the "my-icinga2-playground" directory to store this project and issue the following commands:

Open hosts file and edit the hostname, only the first hostname will be used by Vagrant.

create the icinga2-vm

```ShellSession
$ vagrant up
```

### Installation glpi-playground as ansible-playbook

Create a machine with a CentOS/7 - minimal install. Use this IP-address for the hosts file.

Open hosts file and edit the hostname and IP-address.

Add id_rsa.pub key for passwordless login.

```ShellSession
ssh-copy-id -i ~/.ssh/id_rsa.pub root@192.168.xxx.xxx
```

```ShellSession
ansible-playbook -i hosts site.yml
```

### Installation glpi-playground on a local machine

Create a updated machine with a CentOS/7 - minimal install. Use use a fix IP-address.

make sure you have installed dependencies:

```ShellSession
# yum -y install epel-release
# yum -y install git ansible
```
clone glpi-playground

```ShellSession
# git clone https://github.com/belbob/icinga2-playground.git
```
goto icinga2-playground

```ShellSession
# cd icinga2-playground
```
Edit hosts file and change the hostname and IP-address before run:

```ShellSession
# ansible-playbook -i hosts -c local site.yml
```

## some issues


## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section. Pull requests are also very welcome. Preferably, create a topic branch and when submitting, squash your commits into one (with a descriptive message).

## License

Licensed under the "GNU GENERAL PUBLIC LICENSE Version 3, 29 June 2007". See [LICENSE.md](/License.md) for details.

## Author Information

Written by Robert Keersse (robert.keersse@gmail.com)

Contributions by:

-
