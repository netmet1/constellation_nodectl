# Node Garage - Nodectl 
#### Version 0.4.2

Constellation Network Node Administration Utility

```
Node Garage / Constellation Network
NODECTL v0.4.2
TESSELLATION v0.1.0
TESSELLATION Latest v0.1.0
by netmet
----------------------
usage:  sudo nodectl [ help, status, health, sec, price, count, whoami, upgrade-nodectl ]

Options:

    If run without an optional variable
    you will be able to install and upgrade
    your Node through a CLI_GUI type experience
    (all CLI commands options can be accessed through
    this access method) from your computer.

    Above execution with no option is NOT designed for mobile.

    Mobile friendly CLI options:

    help    | show this menu

    status  | - show the state of the Node's service
              - show if the node has properly joined
                the Constellation Tessellation TestNet
              - show the current TestNet Tessellation
                version running on your system
              - show latest version of Tessellation
                detected on the network.
              - show the current nodectl version

    start   | - start node services on Node

    count   | - count number of peers seen on the network
                and if your system is seen (true/false)
                
    find    | - Is my IP address found on the network
                if an ip address <x.x.x.x> is supplied
                the system will lookup that IP address
                entered to determine if it is found on
                the network
    
    peers   | - show a list of all IP addresses found
                on the network.
                
    whoami  | - show your system's external ip

    stop    | - stop node services on Node

    restart | - restart node services on Node and join

    restart_only | - restart node services on Node but don't join.

    upgrade-nodectl | - upgrade nodectl to latest version

    disable-root-ssh | - have nodectl restrict access to your root user

    enable-root-ssh  | - have ndoectl re-enable access to your root user

    join    | - join the testnet 2.0 network

    health  | - show basic health elements of your Node
              - show the current 15 minute CPU load and
                if WARNING or LOW
              - show the disk usage of your system's
                main storage volume
              - show the uptime in days with
                WARNING or LOW
              - show Memory of your system and if
                WARNING or LOW
              - show the Swap Drive or your system and
                if WARNING or LOW

    sec     | - show basic security statistics
              - show how many log errors were identified
                through all the logs
              - show a count of access attempts
                that were denied
              - show how many times an entity attempted
                to access your system multiple times
                before being blocked via system default
                timers
              - show the TCP port range that the entity
                attempted access between

    price   | Do a quick lookup for Crypto prices
              currently:  Constellation Network,
                          Lattice Exchange,
                          BitCoin,
                          Ethereum,
                          Quant Network


```

