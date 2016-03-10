# 02-elk

This second example is a bit more complex than the first example, for three reasons: 1. we're now adding configuration files for the containers; 2. we're actually building one of the containers locally; and 3. we're adding an assert statement at the end of the role so the playbook can test its own results.

Because the containers require local config files, we're relying upon the Vagrant sync process to make those files available in the Ansible role, so the config files live in the default /vagrant directory.

This example also requires SELinux to be set properly for Atomic, so the Ansible role puts SELinux into permissive mode. It's a great example of how Ansible can manage non-container tasks during the container launch process, which is often necessary to set up the environment properly.

Note in particular the value of having the assert statement at the end of the role. It tells you, unambiguously, that the role does what is expected. If the result of the playbook isn't a functioning Kibana server, validated by fetching the URL, then you know something broke. This use of assert makes the Ansible role a perfect component of a CI/CD pipeline.

Compare:
* docker-elk/docker-compose.yml
* atomic-elk/ansible-dockerized-elk/tasks/main.yml

