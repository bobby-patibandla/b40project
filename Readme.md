ssh-keygen
ll .ssh/

ssh-copy-id ansible@172.20.10.131
ssh ansible@172.20.10.131

ssh-copy-id ansible@172.20.10.116
ssh ansible@172.20.10.116

sudo yum install git -y

git clone --branch ansible-playbooks https://github.com/venkat09docs/b40project.git

cd b40project/
git branch

ansible all -m ping

ansible-playbook ansible/01.ping.yml

ansible-playbook ansible/01.ping.yml -l web

ansible-playbook ansible/02.shell.yml

ansible-playbook ansible/01.ping.yml --list-hosts

ansible-playbook ansible/03.variables.yml

vi ansible/03.variables.yml
ansible-playbook ansible/03.variables.yml

ansible-playbook ansible/03.variables.yml -e "variable1='Commandline Variable'"
