IANA (Internet Assigned Number Authority)  is responsible for global coordination of the IP addressing systems, as well as the Autonomous System Numbers (ASN) which are unique identifier for each network that cross-connects with other networks used for routing Internet traffic. An IP address uniquely identifies a device on an IP network. There are 2 versions of IP addresses : IPv4 and IPv6
IPV4 - 32 bit address divided into 4 octets which is further divided into a network portion and host portion. The value in each octet ranges from 0 to 255 decimal 
IPV6 - 128 bit address

Users are assigned IP addresses by Internet service providers (ISPs). ISPs obtain allocations of IP addresses from a local Internet registry (LIR) or National Internet Registry (NIR), or from their appropriate Regional Internet Registry (RIR).
![[rir-map.svg]]
American, Africa, European, Asian, Latin-American Regions
IANA allocates pools of unallocated IP addresses and ASN to the RIRs according to their needs as described by global policy and documents protocol assignments made by the IETF. When an RIR requires more IP addresses for allocation or assignment within its region, they allocates additional addresses to the RIR and does not make allocations directly to ISPs or end users except in specific circumstances, such as allocations of multicast addresses or other protocol specific needs.
## IP Address Allocations :

### Internet Protocol Version 4 (IPv4)
- [IPv4 Address Space](https://www.iana.org/assignments/ipv4-address-space)
- [IPv4 Multicast Address Assignments](https://www.iana.org/assignments/multicast-addresses)
- [IPv4 Special Purpose Address Registry](https://www.iana.org/assignments/iana-ipv4-special-registry)
- [IPv4 Recovered Address Space Registry](https://www.iana.org/assignments/ipv4-recovered-address-space)
- [Bootstrap Service Registry for IPv4 Address Space](https://www.iana.org/assignments/rdap-ipv4)
### Internet Protocol Version 6 (IPv6)
- [IPv6 Address Space](https://www.iana.org/assignments/ipv6-address-space)
- [IPv6 Global Unicast Allocations](https://www.iana.org/assignments/ipv6-unicast-address-assignments)
- [IPv6 Parameters](https://www.iana.org/assignments/ipv6-parameters) (Parameters described for IPv6, including header types, action codes, etc.)
- [IPv6 Anycast Address Allocations](https://www.iana.org/assignments/ipv6-anycast-addresses)
- [IPv6 Multicast Address Allocations](https://www.iana.org/assignments/ipv6-multicast-addresses
- [IANA IPv6 Special Registry](https://www.iana.org/assignments/iana-ipv6-special-registry)
- [Bootstrap Service Registry for IPv6 Address Space](https://www.iana.org/assignments/rdap-ipv6
- [RIR Comparative Policy Overview](http://www.nro.net/documents/)
## Autonomous System Number Allocations

- [Autonomous System Numbers](https://www.iana.org/assignments/as-numbers)
- [Special-Purpose AS Number Assignments](https://www.iana.org/assignments/iana-as-numbers-special-registry)
- [Bootstrap Service Registry for AS Number Space](https://www.iana.org/assignments/rdap-asn)

ASNs are used to uniquely identify a routing domain controlled by a single administration. In order for traffic to flow from a source Internet address to a destination, network operators need to “announce” the addresses for which they provide connectivity to other network operators. 

Protocols are sets of agreed forms of communication. Domain names and Internet number resources are specialized forms of protocol parameters, there are many more Internet protocols that require coordination. All Internet protocols have values or parameters that must be globally unique.

![[Screenshot 2025-03-19 182804.png]]

## IP Address Classes:

IP addresses are split up into several different categories, including Class A, B, C, D (Multicast), and E (Reserved). Address classes are defined, in part, based on the number of bits that make up the network portion of the address, and in turn, on how many are left for the definition of individual host addresses. 
	• In Class A addresses, the first octet is the network portion.
	• In Class B, the first two octets are the network portion. 
	• In Class C, the first 3 octets are the network portion.
	
![[Screenshot 2025-03-19 183855.png]]

## Private IP Addressing:

IANA has reserved a number of IPv4 network ranges as private. These network ranges are reserved for organizations that want to build an internal network infrastructure based on TCP/IP without using public IP space. By universally recognizing these ranges as private and non-routable in the Internet, multiple organizations can use these ranges internally without causing a conflict with public Internet addresses. To allow traffic from hosts that are using private addresses to access Internet Network Address Translation (NAT) is required. 
	• 10.0.0.0 – 10.255.255.255 (10.0.0.0/8)
	• 172.16.0.0 – 172.31.255.255 (172.16.0.0/12)
	• 192.168.0.0 – 192.168.255.255 (192.168.0.0/16)

## Subnetting:

Subnetting allows you to create multiple logical networks that exist within a single Class A, B, or C network. Each data link on a network must have a unique network address, with every host on that link being a member of the same network. If you break a major network (Class A, B, or C) into smaller subnetworks, you can create a network of interconnecting subnetworks. Each data link on this network would then have a unique network/subnetwork ID.

## Variable Length Subnet Masks (VLSMs) :

VLSMs allow you to use different masks for each subnet, and thereby use address space efficiently. With private address space, it is rarely necessary to shrink below a /24 subnet mask as space is plentiful.

## IP Addressing example  in the Small Business Administration:

Most midsize agencies will likely deploy private addresses internally and use public addresses from a service provider when connecting to a public network such as the Internet.
For example the SBA IP addressing ranges assigned from the 192.168.0.0/16 range of private addresses for covering the following main sections of the network: 
• Headquarters 
• WAN 
• Remote Sites 
• Data Center 
• DMZ 
• Disaster Recovery Site 
• Security 
• Voice
The chosen address space is allocated in contiguous IP address blocks to each of these areas to promote IP summarization. Summarization ensures that there are no entries for child routes, which are routes thar are created for any combination of individual IP addresses contained within summary address in routing table. Summarization reduces the size of the table and allows routers to handle more routes. Be sure to turn off auto-summarization in the Enhanced Interior Gateway Routing Protocol (EIGRP) if there are noncontiguous IP spaces.

![[Screenshot 2025-03-19 191116.png]]
![[Screenshot 2025-03-19 191249.png]]
![[Screenshot 2025-03-19 191635.png]]


