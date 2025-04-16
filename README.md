# OSPFv2-Multi-Area-
This Activity Is Aimed At Configuring OSPFv2 For Multi-Area

# REQUIREMENTS
Routers(4)(2911)
Switches(4)
PCs(16)

# SKILLS TESTED
Configuring OSPF(Multi-Area)
Subnetting
Configuring Secure Remote Access(SSH)
Vlans(Router On a Stick) and Inter-Vlan Routing
Basic Configuration

# PASSWORDS
Privilege Exec mode: cisco123
Line VTY & Console: cisco

# REMOTE ACCESS VIA SSH
Username: James
Secret: james123

# SUBNETTING
# Network Used: 172.16.10.0/24
It was subnetted to have 8 Networks that accommodate at least 4 Usable IP Addresses(Hosts) that were used for the none Point to Point network(Connecting Router to Switches)
4hosts >= 2^n - 2  Where n = number of host bits
by collecting like terms
6 >= 2^n
Choose the smallest value of n that gives the answer of 2^n greater or equal to 6
n = 3 => 2^3 = 8
Therefore, the host bits are 3
New network bits will be 32-3 = 29  Where 32 is the default number of bits of an IPv4 address
Block size/ Magic number: This helps to determine the next network/subnet
Block size = 2^m Where m = the host bits in the octet boundary
Since our network is /24 which is a class C network, the octet boundary is the last octet hence m = n
Block size = 2^3
Block size = 8

SUBNETS
New subnet mask: We use the new network bits = /29
To get the subnets, add the block size to the network given
1. 172.16.10.0/29
2. 172.16.10.8/29
3. 172.16.10.16/29
4. 172.16.10.24/29
5. 172.16.10.32/29
6. 172.16.10.40/29
7. 172.16.10.48/29
8. 172.16.10.56/29

It was subnetted to have 4 Networks that accommodate a maximum of 2 Usable IP Addresses that were used for the Point to Point network (Connecting Router to Router)
2hosts = 2^n - 2
4 = 2^n
2^2 = 2^n
n = 2 host bits
The host bits will be 2
New network bits: 32-2 = 30

Block size = 2^m
Block size = 2^2
Block size = 4

New subnet mask = /30
After completing the 8 networks, the nineth network becomes the first network for the second group with 2 usable IP.
1. 172.16.10.64/30
2. 172.16.10.68/30
3. 172.16.10.72/30
4. 172.16.10.76/30
