Faucet
======

Installs the openflow controller Faucet.

Supporting python modules are installed with `pip`, and `faucet` itself from Github.

Creates systemd startup scripts.



Requirements
------------

Verified on Ubuntu 16.04 LTS.


Role Variables
--------------

    faucet_user: faucet
    faucet_group: faucet
    
The username and group of the system account that faucet should run as.

    faucet_listen_host: 192.168.55.55
    faucet_listen_port: 6636
    
Socket that faucet should listen on.

    faucet_logdir: /var/log/faucet
    faucet_logfile: faucet.log
    faucet_exceptionlogfile: exception.log
    

Dependencies
------------

Example Playbook
----------------


    - name: Install faucet

      hosts: sdn-controllers

      roles:
      - { role: faucet, faucet_listen_host: 192.168.55.55 }

License
-------

MIT

Author Information
------------------

Dick Visser <dick.visser@geant.org>
