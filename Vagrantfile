$script = <<SCRIPT
  # Install git
  sudo apt-get install -y git

  # Download the Git repository that contains analysis scripts/code
  git clone https://github.com/srp33/PAE_Analysis.git

  # Move the analysis files to the home directory
  mv PAE_Analysis/* .
  mv PAE_Analysis/.git* .
  rm -rf PAE_Analysis

  # Update permissions on .git directory so it can be updated
  sudo chmod 777 .git -R

  # Create directory that will be shared between host and guest operating systems
  mkdir -pv Data
SCRIPT

# https://docs.vagrantup.com for details about the settings below
Vagrant.configure("2") do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  config.vm.provision :shell, :inline => $script

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
    vb.customize ["modifyvm", :id, "--cpus", "1"]
  end

  config.vm.synced_folder "Data", "/home/vagrant/Data", :create => "true"
end
