# Gitlab w/ Chef & Vagrant

(Install Vagrant)[http://vagrantup.com/docs/getting-started/index.html]

Get the 'Lucid 32' box (it should work on others, but only tested with
lucid)

    vagrant box add lucid32 http://files.vagrantup.com/lucid32.box

Clone repository

    git clone git://github.com/dpmcnevin/gitlab.git

Init and update the submodules

    git submodule init
    git submodule update

Start up vagrant
  
    vagrant up

Connect to vagrant machine and start rails process

    vagrant ssh

    cd /vagrant/gitlabhq
    bundle exec thin start -e production

On your local machine, update /etc/hosts and add:

    33.33.33.20 gitlab.local

Connect to the site

    http://gitlab.local:3000

Login with:

    Email:    admin@local.host
    Password: 5iveL!fe
  