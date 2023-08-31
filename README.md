# Set up nextcloud
## Installation
This [Ansible playbook](https://docs.ansible.com/ansible/latest/getting_started/index.html) configures a Linux box from scratch to host a swag+nextcloud instance behind a domain. Point the DNS to the IP of the box and set the domain/subdomain accordingly in the playbook. Ensure port 443+80 are open. You can use [this bash script](https://gist.github.com/KasperSkytte/d184d3d163d1e1cfa9b482b2c009a6c0) to install and run everything.

## Requirements
 - ansible (eg from pip3)

## Usage
Add the host entry to the inventory in the `hosts` file or refer to one in you SSH config. Set the `swag_URL` to the correct site URL.

```
# install required galaxy roles
ansible-galaxy install -r roles/requirements.yml

# run the playbook
ansible-playbook playbook.yml
```

## Configuration
Read the comments here and do that https://github.com/linuxserver/reverse-proxy-confs/blob/master/nextcloud.subfolder.conf.sample. 