# code-ansible
Ansible Playbook to install all necessary packages on dev environment

1. Install Fedora:
Choose a Fedora minimal ISO image and use it for the netinstall / everything
2. Install Git and Ansible:
After the initial installation, log in and use the command `sudo dnf install git ansible-core` to install Git and Ansible. 
3. Clone this Repository:`git clone https://github.com/drowsyrobotboy/code-ansible.git`
4. Go to the newly cloned repository and create an ansible.log file `touch ansible.log`. Now tail it `tail -f ansible.log`
5. In a parallel session, run Ansible Playbooks: `ansible-playbook fedora.yml -vvv -K >> ./ansible.log 2>&1` vvv is for more logging K is for root password prompt

Since `hosts: localhost` and `connection: local` are used, Ansible will apply the changes directly to the machine where you run the command.
Most tasks require root privileges, so become: yes is used, and Ansible will likely prompt for your user's sudo password.
