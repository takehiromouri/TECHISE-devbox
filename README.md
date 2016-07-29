# TECHISE-devbox

# Setting Up Vagrant
Make sure you have 1GB or 2GB of free RAM on your computer before proceeding because Vagrant runs a full operating system inside a virtual machine to run your Rails applications.

### The first step is to install Vagrant and VirtualBox on your computer.

Install Vagrant - https://www.vagrantup.com/downloads.html
Install VirtualBox - https://www.virtualbox.org/wiki/Downloads

VirtualBox is where your virtual machines will run. They will be headless which means that they will run in the background and you will interact with them over SSH.

Next we're going to install two plugins for Vagrant.

vagrant-vbguest automatically installs the host's VirtualBox Guest Additions on the guest system.
vagrant-librarian-chef let's us automatically run chef when we fire up our machine.

`vagrant plugin install vagrant-vbguest`
`vagrant plugin install vagrant-librarian-chef-nochef`

This can take a while.

# CLoning the Git Repo

In the terminal, run the following command:

`git clone git@github.com:takehiromouri/TECHRISE-devbox.git`

Then avigate to the repository:

`cd TECHRISE-devbox`


# Running Vagrant
Now that we've got Vagrant and Chef configured properly, we'll start up the Vagrant virtual machine and ssh into it.

`vagrant up`

This might take some time.

After this is set up, let's run the following command:

`vagrant ssh`

Once this has started up, type the following command:

`cd /vagrant`

`gem install bundler`
`gem install rails -v 4.2.1`

This will take a while.

`rbenv rehash`

After this, you're all set!

