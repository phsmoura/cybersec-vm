# cybersec-vm

This repo configures a Kali Linux using **Vagrant** and **Virtual Box**.

## Getting Started

This project was developed on an Ubuntu 20.04 LTS and the commands shown here should work on any linux. Before running any command it's mandatory to have the prerequisites, here I'm using **Virtual Box**, but it's possible to use other virtualization software as well, just check the compatibility of the VM provider with **Vagrant** [here](https://www.vagrantup.com/docs/providers).

### Prerequisites

1. [Install Virtual Box](https://www.virtualbox.org/wiki/Downloads)
2. [Install Vagrant](https://www.vagrantup.com/intro/getting-started/install.html)

## Running the code

Kali virtual machine is configured by Vagrantfile, the name of this vm in the file is *_cybersec_* and once the file is ready, just call vagrant to provision the vm using **ONE** of the commands below:

```bash
$ vagrant up
$ vagrant up cybersec
```

After provisioning it, optionally, you can connect to this vm through *_ssh_*:

```bash
$ vagrant ssh cybersec
```

When the fun is over you can turn off this vm using **ONE** of the commands below:

```bash
$ vagrant halt
$ vagrant halt cybersec
```

## Authors

* **Pedro Moura** - [GitHub](https://github.com/phsmoura)

## License

This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/phsmoura/cybersec-vm/blob/master/LICENSE.md) file for details
