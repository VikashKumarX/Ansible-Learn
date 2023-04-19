# About Role
1. default directory
The default directory contains the default variables that will be used or used by a role, and these variables are easily overridden because of the lowest priority it has.
2. files directory
The files directory contains any files that will be used by the role. It also contains files that will be copied to the managed hosts.
3. handlers directory
The handlers directory contains the handlers that are or will be used by the roles
4. meta directory
The meta directory contains the meta data file for the role. It also includes licenses, authors, dependencies, etc.
5. tasks directory
The tasks directory contains the tasks the role will use or rather the tasks you need to execute. If one is using an already created/developed role, and the tasks need to point to variables, it’s best the variables are defined in the defaults directory.
However, role developers/creators will define their variables in the vars directory.
6. vars directory
The vars directory contains the internal variables that are defined for a role. For example, if you are the creator/developer of the role, the variables will be defined in the vars directory.
More so, it is best variables are defined in the defaults directory if you are not the creator. Tampering with the vars directory can break a role if you don’t really understand how the role is developed.
7. templates directory
The templates directory contains the templates file, the Ansible jinja2 template(link) files for the role.
8. tests directory
The test directory contains an example of how a role is used. It contains two files which are the inventory and test.yml file. The inventory file contains an example of inventory, while the test.yml file contains an example of a playbook and task. 
