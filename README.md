# ProvisioningVM

This is Ansible playbook to install and run a Centos 7 , Virtual Machine on Your MacOS

# Tools Used

# Python3
# Ansible

# VirtualBox

# Vagrant


Install Python & Ansible on your system to make this work


Details :- 


	host

		This file contains the Inventory details i.e the list of host where you need to execute the Ansible playbook.

	Main.yml
		
		This is the main playbook which includes the role that need to be called and passing the host name as 
		variable during the exeuction of the playbook.


	roles/VMautomation
		
		This is ansible role created using the command 
				
				$ ansible-galaxy init roles/VMautomation
				
				roles/VMautomation/tasks/main.yml
				
						This file consist of the tasks that needs to be executed on the server.
						
						Step 1 to 5 - is used for creating a directory 
						"/Desktop/Automation/downloadsfile" 
						(Needs to be changed as per your server)
                        
                        Downloading the Vagrant and Virtual BOX dmg files , and installing it on MacOs

                        step 6 - is used to bring the Vagrant centos 7 Virtual Machines up and running.

                        step 7 - is used to bring down the Vagrant centos 7 Virtual Machines.
							
						Note :- This step will take time as the IOS image is a 
						huge file to be downloaded.
				
				
				roles/VMautomation/vars/main.yml
					
					This file contains variables used by task main.yml such as 
					
							i) The Path that you want to create and download your files to 
							(should use the path where your ansible playbook is placed ).
							
							ii) The web url to downlad the Virtual Box and Vagrant.
							
					NOte:- this needs to be changed as per your requirement. 
						
	ansible.cfg
		
		This file is used to add the inventory file path so that we can avoid passing the same while 
		running the ansible playbook
	
	
	Vagrantfile
	
		It contains the details of VM that needs to be created.
		
		
		
		
# Commands

To run the ansible-playbook to install Virtualbox , Vagrant run as below

	ansible-playbook Main.yml -e "server=localhost" --ask-become-pass -t MacnewInstall
	
	
To stop the running Vagrant Virtual Machines

	ansible-playbook Main.yml -e "server=localhost" --ask-become-pass -t stopVm
	
To see the Running Virtual Machine status you can run the below command on your local Machine

	vagrant status
	


				
