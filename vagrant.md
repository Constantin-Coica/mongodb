# Provisioning project

What did you need to do to provision a vm to run mongo db?

What did you need to do to provision a vm to:

- Run the node.js application?
    1. Download node.
    2. Install node.
    3. Install the dependencies in the folder where the main app is located.
    4. Run the node.js 
- Use the `nology.training` alias?
    1. Create a nology-proxy.conf file, where we define the server name and its alias.
    2. Replace it in the environment, in the sites-avaiable folder.
- Use apache server to direct traffic to a given port?
    1. Editing/creating a new 000-default.conf and change the IP to allow access from every adress (Binding ip: 0.0.0.0)
- How are you able to pass in the DB connection string?
    1. By adding the DB_Path to myvars.sh in the etc/profile.d folder.
---

## General Environment Questions

- What are development environments?
    A virtual space where implementations and changes can be made ensuring the original project data is protected
        and changes that would make it not work are not made.
- How do they relate to an application?
    Application can be run without making possible damaging changes to the physical/original machine.


### Virtual machines

- What is a virtual machine?
    A computer system created using software on one physical computer.
- What does it allow you to do?
    Emulate the functionality of another separate physical computer.
- How have you used one?
    Using virtual box to configure the Ubuntu virtual machine and then uploaded the project files to it so that the project can be run inside it.

### Vagrant

- What is vagrant?
    Vagrant is a software that configures and maintains a virtual environment
- What is a `VagrantFile`?
    VagrantFile is the file where the information used for configuring and defining the virtual machine is stored and used at creation.

#### CLI commands

| Command   | What does it do? | When did you use it? |
| --------- | ---------------- | -------------------- |
| reload    | Reload configuration | When the VagrantFile is changed/edited|
| up        | Initialising the virtual machines | To start/initialise the machines |
| provision | Takes a shell commands script that will be automatically dony by the virtual machine | Used it after initialisation or when the shell scripts are edited |
| destroy   | Shuts down the virtual machines | When the virtual machines need to be stopped from running |
| suspend   | Saves the exact point in time of the vagrant machine rather than completely shutting it off | When further work is required to be done on the virtual machines however you don't want to have them run in the background until that work is done |
| ssh       | Allows entering the virtual environment of the the virtual machines | When needing to edit/create/run files that were specific to the virtual machine |

#### Provisioning

- What is Provisioning in relation to Vagrant?
    Provisioners in Vagrant allow you to automatically install software, alter configurations, and more on the machine as part of the vagrant up process
---
