# Hosts role

This role will manage the hosts file on a server, providing IPs for every host
ansible manages. This is useful when you don't have DNS set up for each host
and you want to be able to connect from one host to another by name.

It uses the template module and completely takes over the hosts file, so don't
use this if you want to manage the hosts file with another tool also.

Note that ansible needs to collect facts for all hosts that need to be
included in the host file in the first play of the playbook.

## Example usage

This role doesn't take any configuration, as it just adds IPs for every host
managed. To use it, just add the role to your role list in a playbook:

    ---
    - hosts: all
      roles:
        - hosts
