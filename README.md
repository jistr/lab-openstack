lab-openstack
=============

Ansible playbooks for preparing lab machines (installed by Beaker) for
running various OpenStack development environments. Currently only
TripleO devtest support is in development.

Getting ready
-------------

On your local machine:

    # run this on your local machine

    yum install ansible
    git clone https://github.com/jistr/lab-openstack.git
    cd lab-openstack
    cp inventory.example inventory
    $EDITOR inventory  # provide fqdn of your lab machine


Devtest
-------

This will prepare the machine in your `inventory` for running devtest.

    # run this on your local machine

    ./install-devtest.sh

It ensures that on the target machine:

* qemu-kvm is present and kvm_intel is modprobed

* libvirt is present and running

* libvirt default storage pool is in `/home/vm_storage_pool` (to
  compensate for small size of root partition in Beaker installs)

* squid is present and running on port 3128 as devtest documentation
  suggests

* standard package group is installed (things like bash completion,
  wget, compression utilities, ...)

* `devtest` user is present and has passwordless sudo rights

* `tripleo-incubator` is cloned
