# packer-express-recipe

Packer recipe to create openstack Laniakea Galaxy 20.05 image based on Centos7 in raw format and then convert it in qcow2.

## Dependencies:

- [packer](https://learn.hashicorp.com/tutorials/packer/get-started-install-cli) 
- Ansible 2.9.6 can be installed on centos using this [ULS](https://github.com/pmandreoli/ULS/blob/main/m_ans_script.sh)
- information in openstack RC v2 or v3 files needed to fill `packer_ga_recipe.json` fields
- [openstack client](https://docs.openstack.org/newton/user-guide/common/cli-install-openstack-command-line-clients.html) 
- [quemu-img converter](https://docs.openstack.org/image-guide/convert-images.html)

### Min flavor that image support:

- vcpu: 4
- RAM: 8 GB 
- Storage: 80 GB

### raw to qcow2 conversion
the image then has to be converted to qcow2 using Quemu immage converter:
- Install quemu  `sudo apt install quemu-utils`
- Download the openstack image using the openstack client
- Convert image from raw to qcow2 cmd: `qemu-img convert -f raw -O qcow2 image.img image.qcow2`
- Upload the image to openstack: `openstack image create`
