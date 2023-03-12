# YAML-Ansible-Server-Configuration
This is a script that automatically configures a server based on a desired configuration utilizing configuration management tools - Ansible.


In this script, we use Ansible to define a desired server configuration in the desired_configuration variable. This includes a list of tasks to install packages, start and enable services, and configure firewall rules.

We then use Ansible tasks to configure the server based on the desired configuration. The loop parameter is used to iterate over the list of tasks in desired_configuration. We also use when conditions to only run tasks that are relevant to the current item in the loop.

To use this script, you'll need to install Ansible on your server and ensure that it can connect to the target host. You can then save the script as a YAML file and run it with the ansible-playbook command. For example:

css
Copy code
$ ansible-playbook configure_server.yaml -i inventory.ini
