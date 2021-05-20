# packer-express-recipe

Packer recipe to create openstack Laniakea Galaxy 20.05 image based on Centos7

## Dependencies:

- [packer](https://learn.hashicorp.com/tutorials/packer/get-started-install-cli) 
- Ansible 2.9.6 can be installed on centos using this [ULS](https://github.com/pmandreoli/ULS/blob/main/m_ans_script.sh)
- information in openstack RC v2 or v3 files needed to fill `packer_ga_recipe.json` fields

### Min flavor that image support:

- vcpu: 4
- RAM: 8 GB 
- Storage: 80 GB


