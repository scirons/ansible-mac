# Ansible Playbook

Playbook that automates the installation of software,general OS configuration and optimization of macOS for *Scirons*.

# Local Installation

1. Go through the initial setup.
2. Ensure Apple's developer tools are installed:

```bash
xcode-select --install
```

3. [Install Ansible with pip](https://docs.ansible.com/ansible/2.9/installation_guide/intro_installation.html#from-pip):
   1.Install pip: `curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py`
   2. Setup virtual environemnt: `sudo pip3 install --upgrade pip`

   ```bash
    python -m virtualenv ansible  # Create a virtualenv if one does not already exist
    source ansible/bin/activate
    ```

   3. Install Ansible: `pip3 install ansible`
   4. Set host target on `main.yml` and run `ansible-playbook main.yml -K` inside the cloned directory. Enter your macOS account password when prompted for the 'BECOME' password.

# Remote Installation

This playbook can be used to manage Macs remotely, without the need of an agent to be installed in the target machine. For that, Remote Login has to be enabled:

From the CLI:

```bash
sudo systemsetup -setremotelogin on
```

# Todos

- Wireguard
- Avatar Picture
