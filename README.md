# ansible-vagrant
A Vagrant profile used to setup a test environment. (This has been tested on Ansible 2.0 or later.)

[![Build Status](https://travis-ci.org/webdavis/ansible-vagrant.svg?branch=master)](https://travis-ci.org/webdavis/ansible-vagrant)

## Requirements

Download and install the following for your system.

* [VirtualBox][1]
* [Vagrant][2]
* [Ansible][3]

_Note: If you are using an Arch system consult the Arch wiki for installing [VirtualBox][4] and
[Vagrant][5]._

## Installation

In a terminal, inside of a project directory, download this project by running the following
command.

    $ git clone https://github.com/webdavis/ansible-vagrant.git

Now access the directory containing the `Vagrantfile` by running

    $ cd ansible-vagrant

Next install the needed Ansible roles for this profile by running

    $ ansible-galaxy install -r requirements.yml

Finally we are ready to provision our Vagrant VM. Just make sure your working directory is
`ansible-vagrant` and run `vagrant up`, followed by `vagrant ssh`.

## Credits

This project is maintained by [Stephen A. Davis][7].

## License

[![license](https://img.shields.io/github/license/webdavis/ansible-vagrant.svg)]()

[1]: https://www.virtualbox.org/wiki/Downloads
[2]: https://www.vagrantup.com/downloads.html
[3]: http://docs.ansible.com/ansible/intro_installation.html
[4]: https://wiki.archlinux.org/index.php/VirtualBox
[5]: https://wiki.archlinux.org/index.php/Vagrant
[7]: https://github.com/webdavis
