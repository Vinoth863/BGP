# BGP
BORDER GATEWAY POROTOCOL
BGP was configured between the two border routers, each serving a different LAN segment—192.168.0.0/24 and 192.168.1.0/24. Both routers were interconnected through the 192.168.2.0/24 transit network, and BGP peer configuration was applied on this link to enable route exchange between the two LANs.

# BGP - CLI - COMMANDS

Router# config terminal

Router(config) # router BGP 1

Router(config - router) # neighbor 192.168.2.2 remote 2

Router(config - router) # network 192.168.0.1 mask 255.255.255.0

exit

Router(config) # router BGP 2

Router(config - router) # neighbor 192.168.2.1 remote 1

Router(config - router) # network 192.168.1.0 mask 255.255.255.0

exit
