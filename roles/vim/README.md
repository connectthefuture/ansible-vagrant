Role Name
=========

An [Ansible][1] role used to install [Vim][2].

Requirements
------------

This role requires Ansible 2.0 or later.

Role Variables
--------------

Override the following variable to change how Vim's `runtimepath` variable is set. This variable is
used for installing and managing a Vim plugin manager such as [Vundle][3].

```yaml
vim_runtimepath: ''
```

Dependencies
------------

This role does not have any dependencies.

Example Playbook
----------------

This role can be installed from [Galaxy][3] by running the following command:

    $ ansible-galaxy install webdavis.vim

or this role can be applied as follows:

```yaml
- hosts: home_nodes
  roles:
    - { role: webdavis.vim }
```


License
-------

[![license](https://img.shields.io/github/license/webdavis/ansible-vagrant.svg)]()

Author Information
------------------

This project is maintained by [Stephen A. Davis][4].

[1]: http://docs.ansible.com/ansible/intro_installation.html
[2]: http://www.vim.org/download.php
[3]: https://github.com/VundleVim/Vundle.vim
[4]: https://galaxy.ansible.com/
[5]: https://github.com/webdavis
