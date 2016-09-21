# Galaxy Ansible Playbook for local SANBI Installations
A ready-to-use Ansible playbook for the SANBI Galaxy Installation.

Before you can use this playbook, you need to install [Ansible][ans] (version
2.1.2.0+ is required). Note that for the time being, this playbook might not
work with Python 3.x.

    $ mkvirtualenv ansible_galaxy
    $ git clone --recursive -b stable-2.1 https://github.com/ansible/ansible
    $ pip install ansible/


To use, clone this repo and provide a locally. Then, run the playbook:

    $ git clone git@github.com:SANBI-SA/ansible_cbt_gx_sanbi.git
    $ cd ansible_cbt_gx_sanbi && ansible-galaxy install -f -r requirements_roles.yml -p roles

The default settings will run the playbook for an installation of SANBI Galaxy in http://cbtgx.sanbi.ac.za. To target a different instance of Galaxy, edit `cbtgx.yml` and set host URL to your prefered Galaxy instance. 

Updates
-------
To update the version of the galaxy-tools role, run the following command
`ansible-galaxy install -f -r requirements_roles.yml -p roles`

[ans]: http://www.ansible.com/home
