## HELP FILE

Node Garage / Constellation Network
NODECTL v0.11.0
TESSELLATION vv0.12.0
TESSELLATION Latest vv0.12.0
by netmet
----------------------
usage:  sudo nodectl [ help [-h], status [-s], start, stop, leave, join, health, sec, price,
                       count, find, peers, whoami, check_connection [-cc], check_source_connection [-csc],
                       upgrade-nodectl, reboot, send_logs [-sl], version [-v] ]

        sudo nodectl check_connection [source] [destination]
        sudo nodectl find [self | source] [destination]


Options:

    If run without an optional variable
    you will be able to install and upgrade
    your Node through a CLI_GUI type experience
    (all CLI commands options can be accessed through
    this access method) from your computer.

    WARNING: GUI-CLI currently is NOT designed for mobile.

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

    id      | - show your system's node id address

    restart | - restart node services on Node and join

    restart_only | - restart node services on Node but don't join.

    -sr slow_restart | - restart the node with a 600 second delay to
                         make sure it is fully off the network in the
                         event you are seeing connection issues or other

    reboot | - acts exactly same as a distribution reboot; however, this command
               will make sure the Node software does a clean 'leave' to leave
               the network prior to rebooting the system.

    -csc check_source_connection | - checks the debug api for peer on both the
                                     node that the edge initially joined to
                                     and the edge node and reports back status

    -cc check_connection | - checks the debug api for peer against
                             the entire network (state channel) you are
                             connected to and report back status

                             EN = Edge Node --> Your Node
                             SN = Source Node --> Node you joined to when
                             you created to Join the State Channel.

                             This command will use compare the Nodes (Peers)
                             that the EN sees verses the Nodes (Peers) the
                             SN sees.  Both should see the same Peers.

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
