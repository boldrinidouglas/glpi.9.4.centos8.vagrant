# -*- mode: ruby -*-
# vi: set ft=ruby :
# Vagrantfile para ambiente de estudos para criar um Cluster HA com K8s de 3 Masters e 1 HAproxy  
vms = {
  'glpi' => {'memory' => '2048', 'cpus' => 2, 'ip' => '10'},
}

Vagrant.configure('2') do |config|

   config.vm.box = "centos/8"
   config.vm.box_version = "1905.1"
   config.vm.box_check_update = false

   vms.each do |name, conf|
     config.vm.define "#{name}" do |k|
       k.vm.hostname = "#{name}.example.com"
       k.vm.network 'private_network', ip: "192.168.1.#{conf['ip']}"
       k.vm.provider 'virtualbox' do |vb|
         vb.memory = conf['memory']
         vb.cpus = conf['cpus']
       end
       k.vm.provision "shell", path: "./glpifast.sh"
     end
   end
 end