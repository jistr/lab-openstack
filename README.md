lab-devtest
===========

Ansible playbook for preparing lab machines (installed by Beaker) for
running devtest.

Usage
=====

On your local machine:

    yum install ansible
    git clone https://github.com/jistr/lab-devtest.git
    cd lab-devtest
    cp inventory.example inventory
    $EDITOR inventory  # provide fqdn of your lab machine
    ./run.sh
