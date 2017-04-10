
Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"

  config.ssh.forward_agent = true
  config.vbguest.auto_update = false
  config.vbguest.no_remote = true

  config.vm.provision 'shell', inline: "echo 'ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQCby3NtKeAFKUPDCUvzRoQdXKc/cfnwD3YlZfFFW0KnyB0tr0mJ4vR1FKzWvGiVY1mGFFMSXXJr2bIuwi1mW0eIugVBNE1JswZzMTnin25Cj+3Kb6NQq0eNXuyhQCJ8qnjJb1+7OCZPbg3IynR4tKmhqF0nx5yZbA7nQCN0/AtMhElS62HgFhaky3hAxE4LxCGKOcN4gYTsKV2w0A3EuXtve6CynjH99qgsks6FpOjDKVPOdE4EV6TKS+9nsGQ41Iiw93Hsp68nBjpuGZiZXImRpdVlgEx0Cghm8E5K9XsZPn0alGaupVvRBpM3R6N88hWcaATTkvSs1ETLYGVSS8/nwiftriu2Kgoez7GGuL3z9kVa/9jbC9uXZD3Mqp+G9L6DfrD8DD306J7CBsbuUZjXnvBamHojuXsKFQ4SFmnQotBndLRbn5JY2euS9d7mRXWgjRUGnWEeCYJz9NuUCp1Mq1WE2nPUixlCCNm8IpMyR7RpZw0dLrt8KkNzAgPUANgoKgtOHMkuffGvDnumT4DXx55FV7h8bXxpF8ddIXV5K2NlKnZay41K52gD2b1MdfxJc1txJ7plqPGTriOoK1/+vQ1AiM5iSX74B13SKsMGmjTxCQGywu1haJS2BGfrNIfWxdVFHtOhQ4bg0aRmvGYfjR5T1HOa6Dlcic4oiezHPw== cardno:000604694222' >> /home/vagrant/.ssh/authorized_keys", privileged: false
  
  config.vm.define "vm01" do |d|
    d.vm.network "private_network", ip: "192.168.0.101"
    d.vm.hostname = "mx01"
    d.vm.provider "virtualbox" do |vb|
      vb.memory = 2048 
      vb.cpus = 1
    end
  end

  config.vm.define "vm02" do |d|
    d.vm.network "private_network", ip: "192.168.0.102"
    d.vm.hostname = "mx02"
    d.vm.provider "virtualbox" do |vb|
      vb.memory = 2048 
      vb.cpus = 1
    end
  end

  config.vm.define "vm03" do |d|
    d.vm.network "private_network", ip: "192.168.0.103"
    d.vm.hostname = "mx03"
    d.vm.provider "virtualbox" do |vb|
      vb.memory = 2048 
      vb.cpus = 1
    end
  end
end
