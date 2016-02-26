# Ansible Docker Examples

Wiki: https://github.com/ftl-toolbox/ansible-docker-examples/wiki

Each of the directories here contain side-by-side examples of multi-container applications installed by docker-compose and by ansible+atomic.

These examples were written on a Mac, and assume that docker-toolkit, ansible, and vagrant are all installed.  (Also, upon running "vagrant up" on an Atomic image for the first time, you'll be asked to install a Vagrant plug-in.)

docker-compose examples are generally invoked by going into the directory and running "docker-compose up".  docker-machine creates its own IP for its VM, which you can determine by running "docker-machine ip default" and then bringing up that IP address in your browser.

ansible+atomic examples are generally invoked by going into the directory and running "vagrant up". vagrant needs to be set up to do its own port forwarding, and the examples are viewed by visiting localhost:port in your browser.

Caveat #1: does not work on Windows because you can't run the Ansible client from Windows natively. Can be solved by running Ansible from the Vagrant box directly; this is one of the reasons to include Ansible in the Atomic image (or at least as a post-install step in the Vagrantfile.)

Caveat #2: no idea if these are the "canonical" Vagrant files for Atomic; currently using a version of the ADB vagrantfile that was grabbed from the internet somewhere.  Most notable modification is the injection of the Ansible provisioning step into the Vagrantfile.
