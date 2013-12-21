# Hosts role

This role will manage the hosts file on a server, providing IPs for every host
ansible manages. This is useful when you don't have DNS set up for each host
and you want to be able to connect from one host to another by name.

It uses the template module and completely takes over the hosts file, so don't
use this if you want to manage the hosts file with another tool also.
