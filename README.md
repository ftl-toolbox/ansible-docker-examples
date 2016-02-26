# Ansible Docker Examples

Wiki: https://github.com/ftl-toolbox/ansible-docker-examples/wiki

Each of the directories here contain side-by-side examples of multi-container applications installed by docker-compose and by ansible+atomic.

These examples were written on a Mac, and assume that docker-toolkit, ansible, and vagrant are all installed.

docker-compose examples are generally invoked by going into the directory and running "docker-compose up".  docker-machine creates its own IP for its VM, which you can determine by running "docker-machine ip default" and then bringing up that IP address in your browser.

ansible+atomic examples are generally invoked by going into the directory and running "vagrant up". vagrant needs to be set up to do its own port forwarding, and the examples are viewed by visiting localhost:port in your browser.


