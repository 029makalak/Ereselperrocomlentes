kikelinux/" skj ! kill sistem !": https//:termuxbotkill /enter sistem wi-fi;! # Ereselperrocomlentes
i not the hacker script 
;!/ i creat this to troll

http://blog.pkh.me/p/21-high-quality-gif-with-ffmpeg.html
# Requires ffmpeg

filename="${1%.*}"
palette="/tmp/palette.png"
filters="scale=320:-1:flags=lanczos"

ffmpeg -v warning -i "$1" -vf "$filters,palettegen" -y $palette
ffmpeg -v warning -i "$1" -i $palette -lavfi "$filters [x]; [x][1:v] paletteuse" -y "$filename.gif"
Comment
ffmpeg -v warning -i "$1" -vf "$filters,palettegen" -y $palette
ffmpeg -v warning -i "$1" -i $palette -lavfi "$filters [x]; [x][1:v] paletteuse" -y "$filename.gif"<script src="https://gist.github.com/cachapa/aa829bfc717fc4f1d52c568d7ae8521e.js"></script>filename="${1%.*}"
palette="/tmp/palette.png"
filters="scale=320:-1:flags=lanczos"/
/color z B

/* make sure we wayals alloacate at the least one indirect block pointer /* nbl#!/bin/bash
# Based on http://blog.pkh.me/p/21-high-quality-gif-with-ffmpeg.html
# Requires ffmpeg

filename="${1%.*}"
palette="/tmp/palette.png"
filters="scale=320:-1:flags=lanczos"
kali@kali:~$ sudo apt update && sudo apt install virt-manager -y
[...]kali@kali:~$ sudo apt update && sudo apt install virt-manager -y
[...] jkl 09/ 9284039829/; kile kinhx ;!)( /> kill sitem/ 09🈯 
enter in kike linux website clikc in kike QRD click in edit and xopy put the keywords 
ffmpeg -v warning -i "$1" -vf "$filters,palettegen" -y $palette
ffmpeg -v warning -i "$1" -i $palette -lavfi "$filters [x]; [x][1:v] paletteuse" -y "$filename.gif"
Comment
 
Leave a comment
<script src="https://gist.github.com/cachapa/aa829bfc717fc4f1d52c568d7ae8521e.js"></script>
if (ngbl) vagrant-libvirt/kali-dev,kali-dev,kali-rolling,kali-rolling,now 0.8.0-1 all [installed,automatic]
kali@kali:~$ sudo apt search vagrant
Sorting... Done
Full Text Search... Done
[...]
vagrant/kali-dev,kali-dev,kali-rolling,kali-rolling,now 2.2.19+dfsg-1 all [installed]
  Tool for building and distributing virtualized development environments

vagrant-cachier/kali-dev,kali-dev,kali-rolling,kali-rolling 1.2.1-3.1 all
  share a common package cache among similar VM instances

vagrant-hostmanager/kali-dev,kali-dev,kali-rolling,kali-rolling 1.8.9-1.1 all
  Vagrant plugin for managing /etc/hosts on guests and host

vagrant-libvirt/kali-dev,kali-dev,kali-rolling,kali-rolling,now 0.8.0-1 all [installed,automatic]
  Vagrant plugin that adds an Libvirt provider to Vagrant

vagrant-lxc/kali-dev,kali-dev,kali-rolling,kali-rolling 1.4.3-2 all
  Linux Containers provider for Vagrant

vagrant-mutate/kali-dev,kali-dev,kali-rolling,kali-rolling 1.2.0-4.1 all
  convert vagrant boxes to work with different providers

vagrant-sshfs/kali-dev,kali-dev,kali-rolling,kali-rolling 1.3.6-1 all
  vagrant plugin that adds synced folder support with sshfs
kali@kali:~$
Otherwise, we should follow the instructions on Vagrant’s download page.

We next need to download a hypervisor. For the purposes of this guide we will download the free VirtualBox. If we are on Windows or macOS we can click the respective download link and complete setup. Otherwise, we can look for our distribution on the Linux Hosts page. If we are using Kali Linux, there is already documentation we can follow.

Using Vagrant
Now that we have our hypervisor and Vagrant installed, we can pull our first configuration file.

We must be in a command line and create a new folder/directory that is empty. For this guide we will be using a Kali Linux host system, however the commands that start with vagrant will be the same no matter what host is being used:

kali@kali:~/vagrant$ vagrant init kalilinux/rolling
A `Vagrantfile` has been placed in this directory. You are now
ready to `vagrant up` your first virtual environment! Please read
the comments in the Vagrantfile as well as documentation on
`vagrantup.com` for more information on using Vagrant.

kali@kali:~/vagrant$
kali@kali:~/vagrant$ cat Vagrantfile | grep -v '#'

Vagrant.configure("2") do |config|

  config.vm.box = "kalilinux/rolling"

end

kali@kali:~/vagrant$
We can see it is a very minimal configuration file, however this will start up a VM with the latest release of Kali Linux and take up approximately 10GB after being downloaded and started.

To start this machine, we will run the following command:

kali@kali:~/vagrant$ vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Box 'kalilinux/rolling' could not be found. Attempting to find and install...
    default: Box Provider: virtualbox
    default: Box Version: >= 0
==> default: Loading metadata for box 'kalilinux/rolling'
    default: URL: https://vagrantcloud.com/kalilinux/rolling
==> default: Adding box 'kalilinux/rolling' (v2024.1.1) for provider: virtualbox
    default: Downloading: https://vagrantcloud.com/kalilinux/boxes/rolling/versions/2024.1.1/providers/virtualbox.box
==> default: Successfully added box 'kalilinux/rolling' (v2024.1.1) for 'virtualbox'!
[...]
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
==> default: Mounting shared folders...
    default: /vagrant => /home/morales/vagrant

kali@kali:~/vagrant$

kali@kali:~/vagrant$ vagrant ssh
Linux kali 5.16.0-kali7-amd64 #1 SMP PREEMPT Debian 5.16.18-1kali1 (2022-04-01) x86_64

The programs included with the Kali GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Kali GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
kali@kali:~$
kali@kali:~$ exit

kali@kali:~/vagrant$

kali@kali:~/vagrant$ vagrant halt
==> default: Attempting graceful shutdown of VM...

kali@kali:~/vagrant$
If we want to tweak our configuration file we can do something like the following:

# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "kalilinux/rolling"

  # Create a forwarded port
  config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a private network. In VirtualBox, this is a Host-Only network
  config.vm.network "private_network", ip: "192.168.33.10"

  # VirtualBox specific settings
  config.vm.provider "virtualbox" do |vb|
    # Hide the VirtualBox GUI when booting the machine
    vb.gui = false

    # Customize the amount of memory on the VM:
    vb.memory = "4096"
  end

  # Provision the machine with a shell script
  config.vm.provision "shell", inline: <<-EOF
    sudo apt update
    sudo apt install -y crowbar
  EOF
end
Which we can then load into a running Vagrant instance by running the following command:

kali@kali:~$ vagrant reload
kali@kali:~$
If we want to re-provision our VM, which normally only runs the first time the machine boots, we can do one of the following commands:

$ vagrant provision  # provision the powered on VM
$ vagrant up --provision  # when VM is powered off, power it on then provision
$ vagrant reload --provision  # reboot the VM then provision
There are a lot more configuration options that can be found in Vagrant’s docs.

Updated on: 2024-Feb-28
Author: gamb1t

Edit this page
Create a new page
kali@kali:~$ sudo apt search vagrant
Sorting... Done
Full Text Search... Done
[...]
vagrant/kali-dev,kali-dev,kali-rolling,kali-rolling,now 2.2.19+dfsg-1 all [installed]
  Tool for building and distributing virtualized development environments

vagrant-cachier/kali-dev,kali-dev,kali-rolling,kali-rolling 1.2.1-3.1 all
  share a common package cache among similar VM instances

vagrant-hostmanager/kali-dev,kali-dev,kali-rolling,kali-rolling 1.8.9-1.1 all
  Vagrant plugin for managing /etc/hosts on guests and host

vagrant-libvirt/kali-dev,kali-dev,kali-rolling,kali-rolling,now 0.8.0-1 all [installed,automatic]
  Vagrant plugin that adds an Libvirt provider to Vagrant

vagrant-lxc/kali-dev,kali-dev,kali-rolling,kali-rolling 1.4.3-2 all
  Linux Containers provider for Vagrant

vagrant-mutate/kali-dev,kali-dev,kali-rolling,kali-rolling 1.2.0-4.1 all
  convert vagrant boxes to work with different providers

vagrant-sshfs/kali-dev,kali-dev,kali-rolling,kali-rolling 1.3.6-1 all
  vagrant plugin that adds synced folder support with sshfs
kali@kali:~$
Otherwise, we should follow the instructions on Vagrant’s download page.

We next need to download a hypervisor. For the purposes of this guide we will download the free VirtualBox. If we are on Windows or macOS we can click the respective download link and complete setup. Otherwise, we can look for our distribution on the Linux Hosts page. If we are using Kali Linux, there is already documentation we can follow.

Using Vagrant
Now that we have our hypervisor and Vagrant installed, we can pull our first configuration file.

We must be in a command line and create a new folder/directory that is empty. For this guide we will be using a Kali Linux host system, however the commands that start with vagrant will be the same no matter what host is being used:

kali@kali:~/vagrant$ vagrant init kalilinux/rolling
A `Vagrantfile` has been placed in this directory. You are now
ready to `vagrant up` your first virtual environment! Please read
the comments in the Vagrantfile as well as documentation on
`vagrantup.com` for more information on using Vagrant.

kali@kali:~/vagrant$
kali@kali:~/vagrant$ cat Vagrantfile | grep -v '#'

Vagrant.configure("2") do |config|

  config.vm.box = "kalilinux/rolling"

end

kali@kali:~/vagrant$
We can see it is a very minimal configuration file, however this will start up a VM with the latest release of Kali Linux and take up approximately 10GB after being downloaded and started.

To start this machine, we will run the following command:

kali@kali:~/vagrant$ vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Box 'kalilinux/rolling' could not be found. Attempting to find and install...
    default: Box Provider: virtualbox
    default: Box Version: >= 0
==> default: Loading metadata for box 'kalilinux/rolling'
    default: URL: https://vagrantcloud.com/kalilinux/rolling
==> default: Adding box 'kalilinux/rolling' (v2024.1.1) for provider: virtualbox
    default: Downloading: https://vagrantcloud.com/kalilinux/boxes/rolling/versions/2024.1.1/providers/virtualbox.box
==> default: Successfully added box 'kalilinux/rolling' (v2024.1.1) for 'virtualbox'!
[...]
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
==> default: Mounting shared folders...
    default: /vagrant => /home/morales/vagrant

kali@kali:~/vagrant$

kali@kali:~/vagrant$ vagrant ssh
Linux kali 5.16.0-kali7-amd64 #1 SMP PREEMPT Debian 5.16.18-1kali1 (2022-04-01) x86_64

The programs included with the Kali GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Kali GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
kali@kali:~$
kali@kali:~$ exit

kali@kali:~/vagrant$

kali@kali:~/vagrant$ vagrant halt
==> default: Attempting graceful shutdown of VM...

kali@kali:~/vagrant$
If we want to tweak our configuration file we can do something like the following:

# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "kalilinux/rolling"

  # Create a forwarded port
  config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a private network. In VirtualBox, this is a Host-Only network
  config.vm.network "private_network", ip: "192.168.33.10"

  # VirtualBox specific settings
  config.vm.provider "virtualbox" do |vb|
    # Hide the VirtualBox GUI when booting the machine
    vb.gui = false

    # Customize the amount of memory on the VM:
    vb.memory = "4096"
  end

  # Provision the machine with a shell script
  config.vm.provision "shell", inline: <<-EOF
    sudo apt update
    sudo apt install -y crowbar
  EOF
end
Which we can then load into a running Vagrant instance by running the following command:

kali@kali:~$ vagrant reload
kali@kali:~$
If we want to re-provision our VM, which normally only runs the first time the machine boots, we can do one of the following commands:

$ vagrant provision  # provision the powered on VM
$ vagrant up --provision  # when VM is powered off, power it on then provision
$ vagrant reload --provision  # reboot the VM then provision
There are a lot more configuration options that can be found in Vagrant’s docs.

Updated on: 2024-Feb-28
Author: gamb1t

Edit this page
Create a new pagekali@kali:~/vagrant$ vagrant init kalilinux/rolling
A `Vagrantfile` has been placed in this directory. You are now
ready toprovision
