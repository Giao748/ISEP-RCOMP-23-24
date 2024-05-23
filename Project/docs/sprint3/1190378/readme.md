## RCOMP 2023-2024 Project - Sprint 3 - Member 1190378 folder

# Building 2


### Document Organization:

- Schematic Campus Overview

- Packet Tracer Simulation
  - OSPF dynamic routing
  - HTTP Server
  - DHCPv4 service
  - Voip Service
  - DNS
  - Nat
  - ACLS

- Startup and Configuration Router Files




## OSPF dynamic routing

- Static routing is no longer utilized, thus in each router, the existing static routing tables have been cleared, except for the default route that connects to the ISP (as without this route there would be no internet distribution on the campus).
- The overall infrastructure is now an OSPF domain, divided into OSPF areas, one for each building and the backbone area (area 0).



### Router_Building4 Configuration.
```
router ospf 2
network 172.25.0.0 0.0.0.255 area 0   (Submask /24)
network 172.25.4.0 0.0.0.255 area 2 (Submask /24)  
```


### BackBone router Configuration
```
router ospf 5
network 172.25.0.0 0.0.0.255 area 0   (Submask /24)
default-information originate
```

### HTTP Service:

### DHCPv4 service
- The router in each building provides DHCPv4 service to all local networks (within the building), except for the DMZ and backbone networks, where IPv4 addresses are static and manually defined.
- For the VoIP VLAN, the DHCP server configuration includes option 150, which represents the IP address of the TFTP (Trivial File Transfer Protocol) server to be used by the phones.
- All computers and laptops have started to receive network configuration via DHCP.




- All Computers and Laptops  are now receiving *DHCP* network configuration.


### Ground Floor

```
ip dhcp pool 1
network 172.25.4.0 255.255.255.128
default-router 172.25.4.0
dns-server 172.25.6.2
domain-name rcomp-22-23-di-g3
```

### Floor One
```
ip dhcp pool 2
network 172.25.4.128 255.255.255.128
default-router 172.25.4.129
dns-server 172.25.6.2
domain-name rcomp-23-24-di-g3
```

### *Wi-Fi*
```
ip dhcp pool 3
network 172.25.5.0 255.255.255.0
default-router 172.25.5.1
dns-server 172.25.6.2
domain-name rcomp-22-23-di-g2
```

### *VoIP*
```
ip dhcp pool 4
network 172.25.6.128 255.255.255.128
default-router 172.25.6.129
option 150 ip 172.25.6.129
dns-server 172.25.6.2
domain-name rcomp-23-24-di-g2
```

## *VoIP service*

In each conntected to each VoipPhone ,it was added telephony Service.

```
telephony-service
auto-reg-ephone
ip source-address 172.25.6.128 port 2000
max-ephones 30
max-dn 30
auto assign 1 to 2

ephone-dn 1
number 2001

ephone-dn 2
number 2002
```


## *DNS*


**DNS Table ** configured on Server 4(Server4_DNS):**

| No. | Name                            | Type     | Detail                          |
|-----|---------------------------------|----------|---------------------------------|
| 0   | building-2.rcomp-23-24-dj-g2    | NS       | ns.building-2.rcomp-23-24-dj-g2 |
| 1   | dns.rcomp-23-24-dj-g2           | CNAME    | ns.rcomp-23-24-dj-g2            |
| 2   | ns.building-2.rcomp-23-24-dj-g2 | A Record | 172.25.4.0                      |
| 3   | ns.rcomp-22-23-dj-g2            | A Record | 172.25.4.0                      |
| 4   | rcomp-22-23-dj-g2               | NS       | ns.rcomp-22-23-dj-g2            |
| 5   | server1.rcomp-22-23-dj-g2       | A Record | 172.25.1.0                      |
| 6   | web.rcomp-23-24-dj-g2           | CNAME    | server1.rcomp-23-24-dj-g2       |
| 7   | www.rcomp-23-24-dj-g2           | CNAME    | server1.rcomp-23-24-dj-g2       |



As we can see , here The web was successevely created.As it can be accessed through any pc or laptop through its link:



### NAT (Network Address Translation)
- Static NAT was used to redirect traffic, therefore, the necessary configurations were applied on the router of the building.
- HTTP and HTTPS requests received on the backbone interface of the router are redirected to the HTTP server in the local DMZ. Both HTTP and HTTPS use TCP connections and assume that the standard service port numbers are used, 80 and 443.


```
ip nat inside source static tcp 172.25.4.0 80 172.25.4.0 80
ip nat inside source static tcp 172.25.4.0 443 172.25.4.0 443
```

```
ip nat inside source static tcp 172.25.4.0 53 172.25.4.0 53
ip nat inside source static udp 172.25.4.0 53 172.25.4.0 53
```


```
interface FastEthernet1/0.1
ip nat inside

interface FastEthernet1/0.2
ip nat inside

interface FastEthernet1/0.3
ip nat inside

interface FastEthernet1/0.4
ip nat inside

interface FastEthernet1/0.5
ip nat inside

interface FastEthernet1/0.6
ip nat outside
```

### Static Firewall (ACLs)
- ACLs will be implemented on the router of each building. They will be particularly restrictive to traffic exchanged with the local DMZ and traffic destined for the router itself.


### Backbone
```
access-list 100 deny ip 10.81.146.0 0.0.1.255 any
access-list 100 permit ospf any host 10.81.151.5
access-list 100 permit udp any host 10.81.151.5 eq 53
access-list 100 permit tcp any host 10.81.151.5 eq 53
access-list 100 permit tcp any host 10.81.151.5 eq 80
access-list 100 permit tcp any host 10.81.151.5 eq 443
access-list 100 permit tcp any host 10.81.151.5 eq 2000
access-list 100 deny ip any host 10.81.151.5
access-list 100 permit ip any any
```

### Floor 0
```
access-list 101 permit ip host 0.0.0.0 host 255.255.255.255					
access-list 101 permit ip 10.81.146.192 0.0.0.63 any
```

### Floor 1
```
access-list 102 permit ip host 0.0.0.0 host 255.255.255.255
access-list 102 permit ip 10.81.146.128 0.0.0.63 any
```

### Wi-fi
```
access-list 103 permit ip host 0.0.0.0 host 255.255.255.255
access-list 103 permit ip 10.81.146.0 0.0.0.127 any
```

### DMZ
```
access-list 104 deny ip 10.81.147.32 0.0.0.31 any
access-list 104 permit udp any host 10.81.147.34 eq 53
access-list 104 permit tcp any host 10.81.147.34 eq 53
access-list 104 permit tcp any host 10.81.147.35 eq 80
access-list 104 permit tcp any host 10.81.147.35 eq 443
```

### VoIP
```
access-list 105 permit ip host 0.0.0.0 host 255.255.255.255
access-list 105 permit udp 10.81.147.0 0.0.0.31 host 10.81.151.5 eq 69
access-list 105 permit tcp 10.81.147.0 0.0.0.31 host 10.81.151.5 eq 2000
access-list 105 permit ip 10.81.147.0 0.0.0.31 any
```


### Static Firewall (ACLs)
- ACLs will be implemented on the router of each building. They will be particularly restrictive to traffic exchanged with the local DMZ and traffic destined for the router itself:


```
interface FastEthernet1/0.550
ip access-group 100 in

interface FastEthernet1/0.571
ip access-group 101 in

interface FastEthernet1/0.572
ip access-group 102 in

interface FastEthernet1/0.573
ip access-group 103 in

interface FastEthernet1/0.574
ip access-group 104 out

interface FastEthernet1/0.575
ip access-group 105 in
```



# Startup and Configuration Router Files
For this sprint, our group needed to access the configuration files for all routers in each building, which are essential for the proper functioning of the DHCPv4 service on the campus. The Campus **Startup and Configuration files** can be found at this link: [Configuration Files](config-files)







