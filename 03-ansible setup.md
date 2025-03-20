# Hands-on

1. update ubuntu apt
2. install ansible
3. create inventory file
4. test connection : ansible all --key-file ~/.ssh/ansible -i inventory -m ping
5. create ansible.cfg file
6. test infos : ansible all -m gather_facts