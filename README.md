# multivagrant
Vagrant template of a 3-node Ubuntu VM cluster.

The goal is provide a basic Vagrantfile that provisions three machines with a commaon hosts file for interconnectivity.

### Use

`vagrant up`

Which will create a 3-node ubuntu (xenial64) cluster.

### Details

This setup uses Vagrant's file provisioner and inline shell provisioner to move the `hosts` file from the root directory to `/etc/hosts` file. The hosts reside on a private network, `192.168.56.0/24`. Each host is simply named `host$` where `$` is the associated host number. No other applications or files are installed, beyond what's included in the base Vagrant box.

