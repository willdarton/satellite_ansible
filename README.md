# Satellite_6_Ansible_Installation_Playbook
Ansible Playbook to Install Red Hat Satellite 6
-----------------------------------------------
-----------------------------------------------

Requirements
------------

You will need ansible and all the required subscriptions for RHEL 7 and Satellite 6.

* Disk Partitioning to support Satellite Directories. Refer to installation guide.
* DNS
* NTP
* satellite_deployment_manifest_path variable defined 
* Satellite Manifest file is hosted on the Ansible Bastion or available via HTTP or FTP somewhere in the environment.

Role Variables
--------------

All variables are in files located in defaults/main.yml


Dependencies
------------

There is no role dependency for this role.

Inventory File
----------

The example of inventory file for this role is in  hosts.target.

Defaults Main YML File
----------------------

Remember to put the correct Admin User and Admin Password
Remember to comment out the RHN user and password if you are performing internal registration (line 18 and line 19)

Answers Template File
---------------------
Remember to Put the correct admin username and admin password Line 98 and 99

How to run the playbook
------------------------

* To run the playbook first you need to create and download the manifest:

Go to <http://rhn.redhat.com>.
- Click "Satellite"
- Click "Register a Satellite"
- Set a Name, select a version and Click "Register"
After this we are going to  attach a subscription.
- Click "Attach Subscription" and select the subscription to attach and click
"Attach Selected"
After this we will download the manifest.
- Click "Download manifest"
After this copy the download file inside the /files directory on the role and
name it "satellite_manifest.zip"

** Then update the variable file in defaults/main.yml in your playbook and
set all mandatory variables for role.:

You can see example of playbook in playbook_example/config.yml
