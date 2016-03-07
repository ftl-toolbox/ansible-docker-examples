# 01-wordpress

This is one of the simplest scenarios of multi-container usage: a Wordpress container linked to a separate database container. 

The ansible version is a little bit more heavyweight, because it carries the entire structure of an Ansible role, for reasons that will become clear in subsequent examples. But the examples are nearly identical in both scope and syntax. 

Compare the two key files to see the comparison: 

* docker-wordpress/docker-compose.yml 
* atomic-wordpress/ansible-dockerized-wordpress/tasks/main.yml
