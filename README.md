# devbox

devbox is an Ansible playbook which sets up a relatively disposable virtual environment with my preferred development tools pre-installed.

## Usage

Create a new Ubuntu 18.04 LTS virtual machine using e.g. [Multipass](https://multipass.run/) or [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

Install Ansible:

```
sudo apt-add-repository --update --yes ppa:ansible/ansible
sudo apt install --yes ansible
```

Run the playbook:

```
git clone https://github.com/jheino/devbox.git
cd devbox
ansible-playbook --ask-become-pass --become local.yml
```
