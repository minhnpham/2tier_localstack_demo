# 2 Tier local VM stack Demo
## Overview
A quick self contained demo of a 2 tier (web/data) application utilising the following components:
+ Centos 7
+ Docker
+ NodeJS
+ Angular
+ MongoDB


Environment and Configuration management tools used:
+ Vagrant
+ Ansible


## Prerequisites
+ [VirtualBox](https://www.virtualbox.org)
+ [Vagrant](https://www.vagrantup.com)


## Description
This is demo project used for local development purposes of a standard 2 tier web application (web/DB), it will:
1. Provision a single local virtual machine running Centos 7
2. Make sure all Centos 7 packages are up to date (this might take a while depending on your internet connection)


The following automation steps will be performed on the VM:
1. Install Ansible
2. Install/configure Docker engine
3. Provision a MongoDB docker container
4. Install GIT and NodeJS build tools
5. Clone/Pull web application source code
6. Configure/Update web application runtime environment configuration variables
7. Build/Bundle Angular frontend code
8. Provision a NodeJS docker container and deploy/start the web application inside the container


NOTE: For demonstration purposes, one of my bootstrap NodeJS web application will be used for the web application source.
[MEAN Stack User Authentication Boostrap App](https://github.com/minhnpham/meanauthapp)

## Usage
Clone this repo, then from a CLI: 

`$ vagrant up`


## Testing
Open up a browser and point to the address:  
[http://localhost:8080](http://localhost:8080)

Using the links on the page:
1. Click *"Register"*, to register a new user account.
2. Click *"Login"*, to login with the newly created account details.
3. After logged in, Click *"Profile"* to verify the user details entered in step #1. 

> Notes: User credentials are stored and retrieved from the MongoDB instance created during the provisioning stages.


## TODO
-