# Ansible-stage

Workflow to configure satellite with stage environment.


Pre-requisites:

1. Have a account on Redhat Ethel 

 - Create account on stage cloud. (Go to http://account-manager-stage.app.eng.rdu2.redhat.com/#create)
 - You can view your subscription pool id by attaching subscription from https://access.stage.redhat.com/


Installation:

The playbooks in this directory make heavy use of a collection from Automation Hub. Before
executing the playbooks, install the collection by doing the following:

1. Install dependencies:
 
   `ansible-galaxy collection install community.general`

   `ansible-galaxy collection install git+https://github.com/theforeman/foreman-ansible-modules.git`
2. Update inventory.yaml
 
Usage:

That done, you can configure the Satellites.

   `ansible-playbook playbooks/configure/stage.yml -e ansible_fqdn=sat_hostname`







