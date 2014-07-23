PAE
===

Example of how to create a Portable Analytical Environment.

# Prerequisite software

The following software must be downloaded and installed manually. 

1. VirtualBox (<http://www.virtualbox.org>).

2. Vagrant (<http://www.vagrantup.com>).

# Executing the following steps at the command line

```
vagrant up # Start the virtual machine via Vagrant

vagrant ssh -- ./install # Install software within the virtual machine

vagrant ssh -- ./update_git # Update the Git repository within the virtual machine

vagrant ssh -- ./analyze # Execute the analysis
```

To modify the analysis, you would update the "analyze" script, which is part of the Git repository at https://github.com/srp33/PAE_Analysis
