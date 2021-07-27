# Cisco Data Center Automation

### Why automate my data center?

By automating the provisioning and configuration of data center, you can save time when provisioning new network devices 
and prevent the human errors that often are a byproduct of manual configuration.

### Automating NXOS configuration and management

NXOS is designed to support third party tool integration. The guest shell enables the users to run custom programs and
containers and the NXAPI makes it easy to build new tools for NXOS or integrate with existing configuraion and management 
tools. Configuration management tools like Chef and Puppet need an agent running on the device and the guest shell on NXOS
provides that capability.

### Popular Open Source automation tools

Ansible, Chef and Puppet are three of the most popular open source automation tools for configuring and managing
infrastructure efficiently ([NetDevOps Fall 2016 Survey](https://interestingtraffic.nl/2017/03/27/insights-from-the-netdevops-fall-2016-survey/)).

##### Ansible

##### Puppet

##### Chef

### What are these lab exercises about?

These lab exercises attempt to teach the learners how to automate and orchestrate their data center Cisco devices. Real 
world use cases are used for the exercises. Each lab exercise extends on the previous one by increasing the complexity
of the operation that is being automated. The same operation in each lab is automated using different popular tools.
This helps the user understand the advantages and disadvantages of each tool, thus enabling him to choose a tool best
suited for him. The following tools are used in these lab exercises:

* Rest APIs
* Python SDK
* Ansible
* Puppet
* Chef

##### Lab1
In this lab exercise we'll be automating configuration of a simple setting. We'll focus on learning the basics of each 
tool. The automation script itself will contain the actual configuration the we want to apply on the device.

##### Lab2
In this lab exercise we'll learn how to make the automation scripts that we created in the previous exercise reusable
with different devices/configuration values. In order to do this, we need to move the actual configuration values out of 
the automation script. By storing the configuration values in an external file, we'll be able to easily change the 
values when needed without having to worry about inadvertently changing the script. 

##### Lab3
Jinja Templates for creation of reports.

##### Lab4
In this lab exercise we'll learn how to use conditional statements and loops. Conditional statements will help in having 
more control on which tasks get executed or how they get executed. Loops will improve the reusability of the automation
script by programmatically repeating the execution of tasks over a set of devices or configuration values.

##### Lab5
In the previous exercise we looked at how to reduce the rewriting of automation code by moving the configuration values
to an external file. In this lab exercise we'll learn how to reduce the rewriting of the configuration values themselves,
wherever they are common across many devices. Within a datacenter, some of the configuration values will be common for 
many devices. Hence, by grouping the devices according to suitable criteria (functionality, geographical etc.,) the
automation becomes more logically organized and efficient.

##### Lab6
In this lab exercise we improve upon the logical grouping of devices and code reusability that we achieved in the 
previous exercise.

##### Advanced Lab
In this lab exercise we will implement all the concepts we learnt in the previous exercises and automate the
configuration of VXLAN BGP EVPN on a spine-leaf NXOS architecture. Note that, the virtual NXOS image does not support 
VXLAN data plane yet (release: 7.0.3.I6.1). Though these lab exercises can be executed on the VIRL topology, the data
flow cannot be verified. You'll need a physical setup to verify the data flow.  
 
### What are these lab exercises not about?

These lab exercises do not cover the networking aspect of the devices. Please refer to official Cisco documentation for
this purpose.

### How do I use these lab exercises?

The lab exercises are designed such that the user is introduced to the basic concepts of the tool first and then the
complexity increases as the user proceeds to further lab exercises.

##### With Cisco dCloud setup

##### With your own setup

Pre requisites on the Ansible control VM:
```
Install pip
Install gcc libffi-dev python-dev libssl-dev
Install ansible
Install requests pip package
```

Copy the ansible.cfg file from the ansible directory in this repository to /etc/


Append hosts file:

```
198.18.1.51	nxosv1
198.18.1.52	nxosv2
198.18.1.61	server1
198.18.1.62	server2
198.18.1.91	VXLAN-Spine-1
198.18.1.92	VXLAN-Leaf-1
198.18.1.93	VXLAN-Leaf-2
198.18.1.94	VXLAN-Leaf-3
```

### Need help? Or have suggestions about improving these lab exercises?

Reach out to APJ Infrastructure Programmability team:

Richard Wade (ricwade@cisco.com) - Team Lead  
Vinay B S (vinbs@cisco.com) - Software Systems Engineer  