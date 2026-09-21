## How to check Ip address?

- on routers: `show ip interface br`

- on VPCs: `show ip`

## To show Protocols and the active Routing on a router?

- `show ip protocols`

- `Routing Protocol is "ospf 1"`: the protocol is OSPF and the process ID is 1

- `Router ID 192.168.1.1`: Router ID identifies the router inside the OSPF, like a unique name for the router.

- `Number of areas is 1`: R1 is in one area only [we still don't know which area].

- `Maximum path 4`: means OSPF can reach 4 different paths to a destination with same cost. it is called [ECMP]

- `Routing for Networks`: means these are the networks that are currently in OSPF

- `Passive Interface`: Ethernet0/3 is inside OSPF but OSPF can't send Hello packets from E0/3.. why? because E0/3 going to PC or a LAN that has no other Router.

- `Routing Information Soureces`: Basically saying these are the sources that OSPF learnt from.. Gateway is the Router IDs of other Routers that R1 took OSPF info from.

## whats an area?

Area is like a space in a big network. Many routers can be in a single area. However, the most important Area is [Area 0]. Most areas usually communicate with Area 0.

When you see:

- `10.1.1.0 0.0.0.3 area 0`

- `192.168.1.0 0.0.0.255 area 0`

This means `10.1.1.0/30` AND `192.168.1.0/24` are part of area 0.


\## whats an area?



Area is like a space in a big network. Many routers can be in a single area. However, the most important Area is \[Area 0]. Most areas usually communicate with Area 0.



When you see:



\- `10.1.1.0 0.0.0.3 area 0`

\- `192.168.1.0 0.0.0.255 area 0`



This means `10.1.1.0/30` AND `192.168.1.0/24` are part of area 0.

