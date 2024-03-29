# IMPORTANT
The offical open sourced GitHub repo for **nodectl** has moved
https://github.com/StardustCollective/nodectl

*Thank you for all your support*

---

## MAINNET 2.0
### NODECT - RELEASE v1.12.0

TestNet 2.0 Node Operators please refer to the **TestNet** section at the end of this readme.
> https://github.com/netmet1/constellation_testnet_nodectl

```
@netmet72
----------------------
usage:  sudo nodectl [ help [-h], [-p] <profile_name>, status [-s], start, stop,
                       leave, join, health, sec, price, show_node_states [-sns],
                       count, find, peers, whoami, list, change-ssh-port <port>
                       check_connection [-cc], check_source_connection [-csc],
                       reboot, send_logs [-sl], version [-v], check_versions [-cv],
                       clear_logs [-cls], clear_uploads [-cul],
                       install, upgrade, upgrade-nodectl, auto_restart [<disable> <check_pid> ]

        sudo nodectl status -p <profile_name>
        sudo nodectl start -p <profile_name>
        sudo nodectl stop -p <profile_name>
        sudo nodectl leave -p <profile_name>
        sudo nodectl restart -p <profile_name>
        sudo nodectl count -p <profile_name>
        sudo nodectl find -p <profile_name> [self | -s <source>] [ -d <destination>]
        sudo nodectl check_source_connection -p <profile_name> | help
        sudo nodectl check_connection -p <profile_name> [source] [destination]
        sudo nodectl clear_files -t [ logs | backups | uploads ]



Options:

    Mobile friendly CLI options:

    upgrade    | upgrade Tessellation version
    install    | install Tessellation - Turn your bare metal or
                 VPS into a Validator Node

    -h help    | show this menu

    -v version         | show version of nodectl
    -cv check_versions | show versions current and latest
                        versions of nodectl and Tessellation
                        and whether they match

    -s status  | - show the state of the Node's service
              - show if the node has properly joined
                the Constellation Tessellation TestNet
              - show the current TestNet Tessellation
                version running on your system
              - show latest version of Tessellation
                detected on the network.
              - show the current nodectl version
              - show the current cluster session verses node session
              - if the sessions do not match, the node is not connected
                properly.  Even if the Node is in Ready State, this does
                NOT mean the Node is connected to the network.

              States: Initial, ReadyToJoin, StartingSession,SessionStarted,
                      ReadyToDownload,WaitingForDownload,DownloadInProgress,
                      Observing,Ready,Leaving,Offline,ApiNotReady

    -p | - required parameter for several commands
           issue the -p with the name of the profile
           following the -p flag
                Requires -p:
                    - status
                    - start
                    - stop
                    - restart
                    - slow_restart
                    - restart_only
                    - join
                    - leave
                    - count
                    - find
                    - peers
                    - check_connection
                    - check_source_connection

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

    list    | - show a list of all the profiles
                currently available on this version
                of nodectl.

    log <type> <grep> -f  | - show logs for requested log type
                              types =  - nodectl
                                       - app
                                       - http
                           grep = grep on word

                           -f follow  (ctrl-c to break out)
                           example)
                           To show the nodectl log and grep out the "join" with
                           a follow
                           nodectl log nodectl join -f


    whoami  | - show your system's external ip

    id                  | - show your system's node id address
    nodeid              | - show your system's node id address
    export_private_key  | - show your p12's private key

    restart | - restart node services on Node and join

    restart_only | - restart node services on Node but don't join.

    -csl check_seedlist | - check the seed list access to see if
                             your nodeid is present on the seed list

    -usl update_seedlist | - update the local copy of the seed list

    -sr slow_restart | - restart the node with a 600 second delay to
                         make sure it is fully off the network in the
                         event you are seeing connection issues or other

    reboot | - acts exactly same as a distribution reboot; however, this command
               will make sure the Node software does a clean 'leave' to leave
               the network prior to rebooting the system.

    -rc reset_cache | - clear out the snapshot cache directory
                        * this should only be done by advanced users during
                          troubleshooting or genesis block creation! *

    -cls clear_logs    | - clear logs older than 7 or 30 days, or all logs
    -cul clear_uploads | - clear uploads directory older than 7 or 30 days, or all logs

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

    -sns show_node_state  | - show a list of known Node states

    upgrade_nodectl | - upgrade nodectl to latest version

    disable_root_ssh | - have nodectl restrict access to your root user

    enable_root_ssh  | - have nodectl re-enable access to your root user

    change_ssh_port <port> | - change the port number used to access your
                               Node via the SSH protocol.  The port number
                               should be between 1024 and 65535.  Please be
                               careful not to use a port already in use or
                               that might be used by the Node for various
                               API access.  Default well known port = 22

    -sl send_logs   |  - create a tarball of your log files for diagnosis
                         will offer option to upload for the developers
                         to access va transfer.sh
                         file name = <your-node-ip-address>_logs.tar.gz

    auto_restart <disable> <check_pid>   |  Starts a background nodectl service that will
                                            keep an eye on the network and restart your
                                            services if they go offline.

                                            auto_restart disable - turns this service off
                                            auto_restart check_pid - checks if it is running


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
                          
    market  | Do a lookup on the top 10 market
              makers in the Crypto industry and
              print out brief report.  Note: If
              Constellation Network is not in the
              top 10 at the current moment in time
              it will be added to the report in its
              current position.
```
