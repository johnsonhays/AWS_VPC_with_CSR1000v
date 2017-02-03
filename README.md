# AWS_VPC_with_CSR1000v
Use Terraform to create VPC with Cisco CSR1000v

Edit terraform.tfvars in the Common Folder to apply your AWS account credentials and CSR1000v key. 
Edit FULLTEMPLATE.j2 and add your DMVPN hub public address
Edit FULLTEMPLATE.yml and DMVPN crypto preshared key

Copy full projects folder to your home directory as the shell script references ~/projects/DMVPN...

Perpare linux host:
sudo apt-get update
sudo apt-get install python-setuptools python-pip git ack-grep jq
sudo pip install PyYAML jinja2 httplib2 six bracket-expansion pysnmp netaddr
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
sudo apt-get install tree
sudo pip install pyping
sudo apt-get install unzip

Install Terraform and Ansible on linux
Follow Terraform installation instructions here:
https://www.terraform.io/intro/getting-started/install.html
Remember to add terraform directory PATH
eg., in ~/.profile, add "export PATH=$PATH:/home/vagrant/terraform"

Add Private key
Add openssh version of private key to ~/.ssh
rename to id_rsa
chmod 600 id_rsa
