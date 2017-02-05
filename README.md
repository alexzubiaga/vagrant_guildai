# Vagrant Guild AI

This repository sets up a vagrant VM with the [examples](https://guild.ai/examples/) from the [guild ai](https://guild.ai/) project.
The vagrant configuration is based on [https://github.com/lau/vagrant_elixir](https://github.com/lau/vagrant_elixir).

## Prerequisites

In order to run it you will need

  * [Vagrant](https://www.vagrantup.com/downloads.html)
  * [Virtual Box](https://www.virtualbox.org/wiki/Downloads)

For Windows it is also recommended to disable [Hyper-V](https://answers.microsoft.com/en-us/windows/forum/windows_8-windows_install/how-do-i-uninstall-hyper-v/7d268911-47cd-4c52-bfe5-ea41e58067ab?auth=1) and install [Putty](http://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
After installing Putty please run `vagrant plugin install vagrant-multi-putty`

## Quick Start

Clone this repository and run
    vagrant up

You can connect to the machine with
    vagrant ssh
or using putty with
    vagrant putty

Once connected just go into `~/guild-examples/mnist` and train the model with the commands

    guild train
    guild view

The training results are available under [http://localhost:6333](http://localhost:6333)

For more information about the guild ai examples see [https://guild.ai/examples/](https://guild.ai/examples/)