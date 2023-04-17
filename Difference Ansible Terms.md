# ABOUT ANSIBLE TERMS
First, we understand its basic terminologies which are as follws:-
Playbooks: A Playbook is an expression of Ansible’s configuration, deployment, and orchestration language. They can describe a policy you want your remote systems to enforce or a set of steps in a general IT process.
Server: Remote servers that you manage with Ansible are called Managed Hosts. Once you install Ansible on a management machine, you will use SSH to connect to remote servers.
Target Machine: The machine where Ansible is run is called the Control Node. The target machines can be virtualized or physical systems.
Task: A task is a unit of work Ansible performs. Tasks are organized into plays, which are then executed on target machines.
Machine: A machine is a physical or virtual server that Ansible can manage.
Modules: Modules are small codes Ansible uses to perform tasks on target machines.
Roles: Roles are collections of related tasks and supporting files that can be used to easily provision complex environments.
Variables: Variables are used to store values that can be referenced in plays and tasks. Variables can be defined in playbooks, inventory files, and variable files.
# About Ansible Playbooks
Ansible Playbooks are a set of instructions that define what actions should be taken on a remote server or group of servers. They can configure, deploy, and manage systems and applications. Playbooks are written in YAML format and are very easy to read and understand.
Playbooks can be used to perform various tasks, such as installing software, configuring services, or even rolling out entire application stacks. Playbooks are typically run from the command line using the ansible-playbook command.Ansible playbooks are very flexible and can be used to automate many different types of tasks. Here are some use-cases for Ansible playbooks:Configuration Management,Software Deployment,Continuous Integration and Delivery,Application Orchestration,Security and Compliance .
# Types of Ansible Machines
Ansible machines are classified into several types depending on their functionality. The most common types are Control, Remote, and Target machines.
Control machine: A control machine is the central node in an Ansible infrastructure. It is used to manage all the other machines in the network. The control machine must have a copy of the Ansible project code and playbooks.
Remote machine: A remote machine is any machine that is not the control machine. Remote machines are managed by the control machine using SSH.
Target machine: A target machine is a remote machine being provisioned or configured by Ansible. Target machines can be of any type, including physical servers, virtual machines, containers, etc.
# Ansible Tasks
Ansible tasks are small pieces of code that can be used to automate workflows and processes.
# Handlers
A handler is an Ansible keyword that triggers a particular action on a remote server. Handlers are usually associated with notify directives, which tell Ansible to run a handler when a task changes state.For example, if you have a task that restarts a service, you may want to use a handler to restart the service only if the task has changed state. This way, you can avoid unnecessary restarts and keep your remote servers running smoothly.
To create a handler, you need to use the Ansible handler module. This module allows you to specify the name of the handler, the action to be taken, and the remote server on which the handler should run.
# Ansible Commands
Ansible commands are the basic building blocks for automating infrastructure management with Ansible. By running simple Ansible commands or playbooks (YAML files that define groups of hosts and tasks to be run), entire server deployments can be set up or torn down in moments.
  # Ad-hoc commands we could use Ansible commands for some common tasks.
Example 1: Start and Stop a Service
If you need to start or stop a service on a remote server, you can use the following command:ansible -m service -a “name= state=” 
For example, if you need to start the Apache service on a remote server, you would use the following command: ansible server1 -m service -a “name=httpd state=started” 
## Example 2: Install a Package
If you need to install a package on a remote server, you can use the following command:ansible -m yum -a “name= state=present”
For example, if you need to install the Apache HTTP Server on a remote server, you would use the following command:ansible server1 -m yum -a “name=httpd state=present”
# Function/Commands list
Ansible commands are very powerful and can help you automate many tasks. Below we will discuss the most commonly used Ansible commands.
ansible-playbook: This is the most important Ansible command used to run playbooks. 
ansible-doc: This command is used to view documentation for Ansible modules.
ansible-galaxy: This command is used to install roles from Galaxy, a repository of community-contributed roles.
ansible-vault: This command is used to encrypt and decrypt sensitive data.
ansible-console: This command is used to launch an interactive Ansible session.
ansible-pull: This command is used to pull playbooks from a remote Git repository.
ansible-inventory: This command is used to generate an inventory file.
# Ansible Variables
Ansible variables help you define values that you can reference in your playbooks. Variables can be used to store values that you want to reuse throughout your playbooks, and they can be used in conditionals and loops to dynamically change the behavior of your playbooks.
In Ansible, there are two types of variables: facts and vars. Facts are variables automatically populated by Ansible from the information it gathers about the managed system. Vars are user-defined variables that can be used to store any value, including strings, numbers, lists, and dictionaries.
