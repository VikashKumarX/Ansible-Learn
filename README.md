# Ansible-Learn
Ansible is Configuration Management Tool.
Configuration management tools make changes and deployments faster, remove the potential for human error, while making system management predictable and scalable. They also help you to keep track of the state of your resources, and keep you from repeating tasks, like installing the same package twice.
# Configuration Management Tool r of 2 type i.e. Pull-Based & Push-Based
In this type of configuration management tool, the nodes pull the configuration information from the server (hence, the name).
# PULL BASED CONFIGURATION TOOL
A small software (called agent or client) is installed on every node. This agent/client will at regular intervals, get the configuration from the server
compare the configuration received from the server with the current configuration of the node if there is any mis-match, take the steps required to match the configuration of the node with the configuration received from the server.This means that, its always the agent/client that initiates communication, not the main server.
Chef & Puppet are good examples of such configuration management tools.
# PUSH BASED CONFIGURATION TOOL
In this type of configuration management tool, the main server (where the configuration data is stored) pushes the configuration to the node (hence, the name). So, it is the main server that initiates communication, not the nodes. Which means that an agent/client may or may not be installed on each node.
Ansible is an example of a push based configuration management tool that doesn’t need an agent to be installed on the nodes. SaltStack is an example of a push based configuration management tool that needs an agent (minion) to be installed on the nodes. In both cases, its the main server that starts the communication and sends the configuration data to the nodes without the nodes asking for it.
# Push vs Pull — Which one to choose?
Remember, both types of configuration management tools can do it all. So, the following comparison is based on the default features. I am not highlighting the disadvantages since, it should be pretty clear from the list of advantages and, frankly speaking, most of these “disadvantages” can be worked around.
Advantages of Push based Configuration Management
Control over the entire system: Since the main server (where you store the configuration information) pushes the configuration to the nodes, you have more control over what nodes need to be configured, the actions are more synchronous and error handling becomes much easier since you can immediately see & correct the issues.
Simpler to use: Push configuration management tools, like Ansible, are generally much easier to setup and get started. Also, since nodes do not pull any information from the main server, development is more straight forward as you can easily test your scripts without worrying about any node picking it up accidentally or changing any settings on the agents.
Advantages of Pull based Configuration Management
Easier to bootstrap new nodes: As soon as a node is ready, agent/client that runs on the node can start pulling configuration from the main server. This means that a new machine configured automatically, when the server is ready to be configured (unlike push method where you have to check if the node is ready to be configured).
Easier scalability: Since the nodes can be bootstrapped automatically and independent of other nodes, it means that scaling such a configuration is much easier.

In summary, which tool should you use? The answer depends on what your fundamental need is and how much customisation are you willing to do.
A largely static infrastructure will benefit more from Push Based Configuration Management, while an extremely dynamic infrastructure will find Pull Based Configuration more suitable.
You could also use a combination of the two — use Pull for initial configuration setup and Push for application deployment.
