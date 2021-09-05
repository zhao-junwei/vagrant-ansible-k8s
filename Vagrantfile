# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure(2) do |config|
  
  NodeCount = 3

  # Kubernetes Nodes
  (1..NodeCount).each do |i|
    config.vm.define "kc#{i}" do |workernode|
      workernode.vm.box = "generic/centos8"
      workernode.vm.hostname = "kc#{i}.example.com"
      workernode.vm.network "private_network", ip: "172.1.1.1#{i}"
      workernode.vm.provider "virtualbox" do |v|
        v.name = "kc#{i}"
        v.memory = 3072
        v.cpus = 2
      end
    end
  end
end
