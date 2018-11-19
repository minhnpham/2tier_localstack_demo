# 2 Tier local VM stack Demo
## Overview
A quick self contained demo of a 2 tier (web/data) application utilising the following components:
+ Centos 7
+ Docker
+ NodeJS
+ MongoDB

Environment and Configuration management tools:
+ Vagrant
+ Ansible


## Description
This is demo project used for local development purposes of a standard 2 tier web application (web/DB), it will:
1. Provision a single local virtual machine running Centos 7
2. Make sure all Centos 7 packages are up to date (this might take a while depending on your internet connection)


The following automation steps will be performed on the VM:
1. Install Ansible
2. Install/configure Docker engine
3. Provision a MongoDB docker container
4. Install GIT
5. Clone/Pull web application source code
6. Configure/Update web application runtime environment variables
7. Provision a NodeJS docker container and deploy/start the web application inside the container
8. Build/Bundle Angular frontend code
9. Provision a nginx docker container with frontend code

NOTE: For demonstration purposes, one of my bootstrap NodeJS web application will be used for the web application source.
[MEAN Stack User Authentication Boostrap App](https://github.com/minhnpham/meanauthapp)

## Usage
`vagrant up`


## Requirements
+ [VirtualBox](https://www.virtualbox.org)
+ [Vagrant](https://www.vagrantup.com)


## TODO
1. Bundle Angular frontend code
2. Provision nginx and deploy frontend code
