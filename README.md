# Mac Development Ansible Playbook

[![Build Status](https://travis-ci.org/ekka21/mac-dev-playbook.svg?branch=master)](https://travis-ci.org/ekka21/mac-dev-playbook)

This playbook installs and configures most of the software I use on my Mac for web and software development. Some things in macOS are difficult to automate (notably, the Mac App Store and certain tools from Apple), so I still have some manual installation steps, but at least it's all documented here.

This is a work in progress, and is mostly a means for me to document my current Mac's setup. I'll be adding settings and packages to this set of playbooks over time.

*See also*:

  - [Battleschool](http://spencer.gibb.us/blog/2014/02/03/introducing-battleschool)
  - [osxc](https://github.com/osxc)
  - [MWGriffin/ansible-playbooks](https://github.com/MWGriffin/ansible-playbooks) (the original inspiration for this project)

## Installation

  1. [Install Ansible](http://docs.ansible.com/intro_installation.html).
  2. Ensure Apple's command line tools are installed (`xcode-select --install` to launch the installer).
  3. Clone this repository to your local drive.
  4. Run `$ ansible-galaxy install -r requirements.yml` inside this directory to install required Ansible roles.
  5. Run `ansible-playbook main.yml -i inventory -u [username] -K` inside this directory (substitute `[username]` for your macOS account username). Enter your account password when prompted.

> Note: If some Homebrew commands fail, you might need to agree to XCode's license or fix some other Brew issue. Run `brew doctor` to see if this is the case.

## Included Applications / Configuration

Applications (installed with Homebrew Cask):

  - google-chrome
  - sequel-pro
  - vagrant
  - virtualbox
  - slack
  - iterm2
  - lastpass
  - sizeup
  - flycut
  - spotify
  - docker

Packages (installed with Homebrew):

  - pv
  - openssl
  - git
  - git-flow
  - go
  - gpg
  - python
  - sqlite
  - zsh
  - vim
  - tmux
  - nvm
  - npm
  - tig
  - ssh-copy-id
  - htop
  - php70
  - php70
  - php70-mcrypt

My [dotfiles](https://github.com/ekka21/dotfiles) are also installed into the current user's home directory.

Finally, there are a few other preferences and settings added on for various apps and services.

## Ansible for DevOps

Check out [Ansible for DevOps](https://www.ansiblefordevops.com/), which will teach you how to do some other amazing things with Ansible.

## Author
[Ekkachai Danwanichakul](http://www.ekkachai.net), 2016 (originally inspired by [Jeff Geerling](http://www.jeffgeerling.com/), 2014 (also originally inspired by [MWGriffin/ansible-playbooks](https://github.com/MWGriffin/ansible-playbooks))).

