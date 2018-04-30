# macOS-Bootstrap
### What is this?
This repo contains an ansible playbook that will setup a freshly installed macOS client to my liking.
### Why?
I'm addicted to automation and figured why not automate a long daunting task with my favorite provisioning tool, Ansible. Also, I wanted a way to document my Mac's environment.
### Usage:
* Git clone this repository 
```
$ git clone git@github.com:bpdev97/macOS-Bootstrap.git
```
* Run the `init.sh` script to install homebrew and ansible
```
$ ./init.sh
```
* Run the ssh portion of the playbook to copy my private key into place
```
$ ansible-playbook bootstrap.yml --tags "ssh" --ask-vault-pass
```
* Run playbook normally
```
$ ansible-playbook bootstrap.yml
```
* Run the homeshick portion of the playbook setup my dotfiles via homeshick
```
$ ansible-playbook bootstrap.yml --tags "homeshick"
```
