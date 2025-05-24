# code-ansible
Ansible Playbook to install all necessary packages on dev environment

1. Install Fedora:
Choose a Fedora minimal ISO image and use it for the netinstall / everything
2. Install Git and Ansible:
After the initial installation, log in and use the command `sudo dnf install git ansible-core` to install Git and Ansible. 
3. Clone this Repository:`git clone https://github.com/drowsyrobotboy/code-ansible.git`
4. Run Ansible Playbooks: `ansible-playbook fedora.yml`

Since `hosts: localhost` and `connection: local` are used, Ansible will apply the changes directly to the machine where you run the command.
Most tasks require root privileges, so become: yes is used, and Ansible will likely prompt for your user's sudo password.
