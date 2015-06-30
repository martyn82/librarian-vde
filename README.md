Librarian VDE
=============

A virtual development environment (VDE) for the [Librarian](https://github.com/martyn82/librarian) project.
It will create and provision a virtual machine on Vagrant that contains the global environment required for developing
the Librarian project.

How to use
----------

### Prerequisites
- Vagrant
- Ansible

### Setup
If you are using VirtualBox as your VM provider for Vagrant, then make sure to install the VirtualBox guest additions plugin for Vagrant:
```
$ vagrant plugin install vagrant-vbguest
```

Checkout this repository:
```
$ git clone git@github.com/martyn82/librarian-vde
```

In the root directory of the repository, run:
```
$ vagrant up
```
This will create a virtual machine and provision this machine for working.

After privisioning has been completed, make sure to prepare your SSH configuration to handle SSH commands from within the VDE.
You can do this by adding the output of the following command to your `~/.ssh/config` file:
```
$ vagrant ssh-config
```

Alter the line that says `UserKnownHostsFile` (which states /dev/null) to the location of your known_hosts file (usually ~/.ssh/known_hosts).

Finally, run the following command to log in to the VDE:
```
$ vagrant ssh
```
