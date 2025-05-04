# Ansible Playbook

Playbook that automates the installation of software,general OS configuration and optimization of macOS for *Scirons*.

# Local Installation

1. Go through the initial setup.
2. Ensure Apple's CLI tools are installed:

```bash
xcode-select --install
```

3. [Install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/index.html):
   1. Run the following command to add Python 3 to your $PATH: `export PATH="$HOME/Library/Python/3.8/bin:/opt/homebrew/bin:$PATH"`
   2. Upgrade Pip: `sudo pip3 install --upgrade pip`
   3. Install Ansible: `pip3 install ansible`
4. Run `ansible-playbook main.yml -K` inside the cloned directory. Enter your macOS account password when prompted for the 'BECOME' password.

# Remote Installation

This playbook can be used to manage Macs remotely, without the need of an agent to be installed in the target machine. For that, Remote Login has to be enabled:

From the CLI:

```bash
sudo systemsetup -setremotelogin on
```

# Todos

- Wireguard
- Avatar Picture
