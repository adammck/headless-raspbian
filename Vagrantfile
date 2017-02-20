Vagrant.configure("2") do |config|
  config.vm.box = "debian/jessie64"
  config.vm.provision "shell", path: "bin/provision"

  # Don't copy images back into the VM.
  config.vm.synced_folder ".", "/vagrant", type: "rsync",
    rsync__exclude: [".git/", "raspbian.img"]
end
