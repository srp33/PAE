PAE
===

Example of how to create a Portable Analytical Environment.

# Prerequisite software

The following software must be downloaded and installed manually. 

1. VirtualBox (<http://www.virtualbox.org>).

2. Vagrant (<http://www.vagrantup.com>).

# Demo

1. Download "Vagrantfile" from this repository to your local computer.

2. Open a command prompt / terminal window on the computer and navigate to the directory where "Vagrantfile" is stored.

3. Execute the following steps at the command line.

```
vagrant up # Start the virtual machine via Vagrant

vagrant ssh -- ./install # Install software within the virtual machine

vagrant ssh -- ./update_git # Update the Git repository within the virtual machine

vagrant ssh -- ./analyze # Execute the analysis

vagrant package --output demo.box # Package the virtual machine in a binary file

vagrant destroy -f # Stop the virtual machine
```

To modify the analysis, you would update the "analyze" script, which is part of the Git repository at https://github.com/srp33/PAE_Analysis
