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

Checkout the VDE repository (if you haven't already):
```
$ git clone git@github.com/martyn82/librarian-vde
```

In the root directory of the VDE repository, run the following command to create a virtual machine and provision this machine for working (checkout the ansible file to determine what tasks are executed when provisioning):
```
$ vagrant up
```

After privisioning has been completed, the machine is up and ready. Finally, run the following command to log in to the VDE. All dependent projects should be there in the `/home/vagrant/p` directory.
```
$ vagrant ssh
```
