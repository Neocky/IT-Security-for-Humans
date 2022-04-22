# :left_right_arrow: Network switches

Network switches are essential to provide your building/office with network access to your clients and hosts. Most of
the time the network switch is somewhere in a server rack and is connected to a patch panel, where ethernet cables from
different lan sockets in your building/office go to. Of course every building is wired differently but this is just
an abstraction of the patch panel/switch concept.

So what happens when an attacker goes inside the building and finds an open ethernet port and connects to it?  
If there is no port security configured on the access switch, then the attacker is already inside your network and
can connect to where he pleases.


## :no_entry: Port security
Port security on a network switch means, that hosts need to authenticate themself to be able to access the 
network. The authentication can happen in many different ways, like certificates or mac based authentication.
This guide will show you the setup of mac based authentication for a port on a dell N1500 networking switch.
```diff
- Attackers can spoof their MAC address so this isn't a failesafe method. 
- Look into 802.1x authentication if you want a different authentication method!
```

First I connected to the network switch and then configured the first port to be in vlan 2 and to enable the
mac based port security so only the device with the MAC address `0011:2233:4455` cann connect to vlan 2:
```
Switch01(config)#interface Gi1/0/1
Switch01(config-if)#description "Client"
Switch01(config-if)#switchport mode access
Switch01(config-if)#switchport access vlan 2
Switch01(config-if)#switchport port-security                                      // to enable port security
Switch01(config-if)#switchport port-security mac-address 0011:2233:4455 vlan 2    // set allowed MAC address so only 0011:2233:4455 can connect to vlan 2
Switch01(config-if)#exit
```
With this configuration an attacker will be stopped and won't get network access if he wants to connect on the port 
`Gi1/0/1`, unless he spoofs his MAC address to be `0011:2233:4455`. This will slow the attacker down if he doesn't know beforehand the MAC addres which is allowed on the port.

This is just an example of a mac based port security on a Dell N1500 networking switch. Every manufacturer has 
different commands so look into their guides.


## Source
- https://www.dell.com/support/kbdoc/en-en/000121383/how-to-configure-mac-based-port-security-on-the-dell-n1500-switch
- https://www.dell.com/support/kbdoc/en-en/000121440/how-to-configure-mac-based-port-security-on-dell-n2000-n3000-and-n4000-series-switches
