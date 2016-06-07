Demo/Test Project for Passware Kit Agent deployment using Ansible
=================================================================

Requirements
------------

* ansible
* vagrant (optional, to run Passware Kit Agent in VM)


Usage
-----

Prepare ansible playbook:

```shell
$ git clone git@github.com:passware/demo-ansible-passware-kit-agent.git
$ cd demo-ansible-passware-kit-agent
$ mkdir roles
$ ansible-galaxy install -r requirements.yml -p ./roles/

```

Prepare inventory file:

```
# inventory

[agents]
agent01.company.com ansible_ssh_host=1.2.3.4 ansible_ssh_port=2222
agent02.company.com ansible_ssh_host=1.2.3.5 ansible_ssh_port=2222
agent03.company.com

```

Run playbook:

```shell
$ ansible-playbook -i inventory deploy.yml

```

Run playbook in VM:

```shell
$ vagrant up

```

License
-------

MIT
