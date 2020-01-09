Role Name
=========

This role uses a wrapper around GNU stow to back up any existing dotfiles and then symlink the desired folders from the dotfiles repo.

Requirements
------------

This role installs GNU stow. A dotfiles git repo is required with various application dotfiles separated into folders and listed in the dotf_stow_list var.
A dotfiles stow repo example:
```
dotfiles
├── bash
│   ├── .bash_aliases
│   ├── .bash_fedora
│   ├── .bash_osx
│   ├── .bash_profile
│   ├── .bashrc
│   └── .bash_root_aliases
├── dig
│   └── .digrc
├── git
│   ├── .gitconfig
│   └── .gitignore_global
├── mongodb
│   └── .mongorc.js
├── rpmbuild
│   └── .rpmmacros
├── sakura
│   └── .config
│       └── sakura
│           └── sakura.conf
└── vim
    └── .vimrc
```

Role Variables
--------------

This role requires setting a valid git repo URL and vaulted key_vault attribute in the dotf_git_repo dict, as well as the desired folders to stow. The dotf_root_too boolean will also stow the selected folders for root using become.

License
-------

BSD

Author Information
------------------

https://github.com/herd-the-cats
