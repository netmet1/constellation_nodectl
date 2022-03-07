# Node Garage - Nodectl 
#### Version 0.7.6

Constellation Network Node Administration Utility

```
Node Garage / Constellation Network
NODECTL v0.7.6
TESSELLATION v0.5.0
TESSELLATION Latest v0.5.0
by netmet
----------------------
by netmet
----------------------
usage:  sudo nodectl [ help [-h], status [-s], start, stop, leave, join, health, sec, price, count, find, peers, whoami, check_connection [-cc], check_genesis_connection [-cgc], upgrade-nodectl, send_logs [-sl], version [-v] ]

Options:

    If run without an optional variable
    you will be able to install and upgrade
    your Node through a CLI_GUI type experience
    (all CLI commands options can be accessed through
    this access method) from your computer.

    Above execution with no option is NOT designed for mobile.

    Mobile friendly CLI options:

    -h help    | show this menu
    
    -v version | show version of nodectl
    
    -s status  | - show the state of the Node's service
              - show if the node has properly joined 
                the Constellation Tessellation TestNet
              - show the current TestNet Tessellation 
                version running on your system
              - show latest version of Tessellation
                detected on the network.
              - show the current nodectl version
              States: Ready - Joined successfully
                      API Ready - Ready to Join
                      Start Completed - Service is up
                      Shutdown - Service is down
              
    start   | - start node services on Node

    stop    | - stop node services on Node

    join    | - join the testnet 2.0 network
        
    leave   | - force node to leave cluster
            
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
                            
    restart | - restart node services on Node and join
    
    restart_only | - restart node services on Node but don't join.
    
    -cgc check_genesis_connection | - checks the debug api for peer on both the
                                      node performing genesis and the edge node
                                      and reports back status
    
    -cc check_connection | - checks the debug api for peer against
                             the entire network (state channel) you are
                             connected to and report back status
                         
    upgrade-nodectl | - upgrade nodectl to latest version
    
    disable-root-ssh | - have nodectl restrict access to your root user
    
    enable-root-ssh  | - have nodectl re-enable access to your root user    
            
    -sl send_logs   |  - create a tarball of your log files for diagnosis  
                         will offer option to upload for the developers
                         to access va transfer.sh
                         file name = <your-node-ip-address>_logs.tar.gz
                     
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
