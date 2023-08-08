 ## Ansible Instrumentation
 1. Create a directory for the project mkdir ansible-IP
 2. cd ansible-IP
## Disable SSH host keys checking
 1. Create a hosts file with the IP addresses of the client , backend virtual machines on GCP, file is under inventory.ini
 2. Create ansible.cfg file
    ** Disable host key checking by typing host_key_checking = False in the file
## Provision the servers
 1. Then Create a playbook.yaml that will clone the repo and run the commands that will ignite up the application.
## Create the virtual servers
 1. Create the TF file that provisions the VMs on GCP and use use debian-cloud/debian-10 as the base boot disk
 2. Also create ssh-keys locally and save the public key on the project file on GCP VM to allow access. This is under metadata section.
 3. Run terraform init, plan then apply to automatically provision the VMs and starts the ansbile playbook. 
  Once done, the output will be indicated with the IP that you can access the online app.