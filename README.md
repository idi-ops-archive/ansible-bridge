Ansible Role: bridge
====================

Creates a network bridge on Linux

Requirements
------------

None.

Role Variables
--------------

    bridge_name
    bridge_ip_addr   # optional
    bridge_netmask   # optional
    bridge_ports     # list of network interface to be enslaved to bridge
    bridge_onboot    # default: yes
    bridge_protocol  # default: none
    bridge_delay     # default: 0


Dependencies
------------

None.

Example Playbook
----------------


    - hosts: localhost
      roles:
         - role: bridge
           bridge_name: "br-public"
           bridge_ports: ["eth0"]
