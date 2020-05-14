# devbox

devbox is an Ansible playbook which sets up a relatively disposable virtual environment with my preferred development tools pre-installed.

## Supported distributions

- Ubuntu 18.04 LTS
- Ubuntu 20.04 LTS

## Usage

Create a new Ubuntu virtual machine using e.g. [Multipass](https://multipass.run/) or [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

If running Ubuntu 18.04 LTS, enable the PPA repository to install the latest version of Ansible:

```
sudo apt-add-repository --update --yes ppa:ansible/ansible
```

Install Ansible:

```
sudo apt install --yes ansible
```

Run the playbook:

```
git clone https://github.com/jheino/devbox.git
cd devbox
ansible-playbook --ask-become-pass --become local.yml
```
