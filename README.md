lab-openstack
=============

Ansible playbooks for preparing lab machines (installed by Beaker) for
running various OpenStack development environments. Currently only
TripleO devtest support is in development.

Usage
=====

On your local machine:

    yum install ansible

    git clone https://github.com/jistr/lab-openstack.git
    cd lab-openstack
    cp inventory.example inventory
    $EDITOR inventory  # provide fqdn of your lab machine
    ./install-devtest.sh
