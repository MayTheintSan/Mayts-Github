# Networking Note (May)

www.youtube.com/@LoopAvoidance



### Communication

* unicast
* multicast
* broadcast



### Numbering System

* Binary => base2 => 0,1
* Decimal => base10 => 0,1,2,3,4,5,6,7,8,9 => IP Address (32bits)
* Hexadecimal => base16 => 0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F => MAC Address (48bits)



##### Signal => Digital / Analog



MB(byte) is not the same as mb(bit)

0 = 1 bit

1 = 1 bit

8 bits = 1 byte

1024 bytes = 1 kB (kilo = 10\*3)

1024 kB = 1 MB (mega = 10\*6)

1024 MB = 1 GB (gega = 10\*9)

1024 GB = 1 TB (tera = 10\*12)



|**Hexadecimal**|**Binary**|
|-|-|
|0|0000|
|1|0001|
|2|0010|
|3|0011|
|4|0100|
|5|0101|
|6|0110|
|7|0111|
|8|1000|
|9|1001|
|A|1010|
|B|1011|
|C|1100|
|D|1101|
|E|1110|
|F|1111|



### Network Type

* telecommunication network
* computer network



### Network Elements

* PAN => Personal Area Network => use Bluetooth
* LAN => Local Area Network => Intranet
* CAN => Campus Area Network => set area
* MAN => Metropolian Area Network => Extranet (connect the countries)
* WAN => Wide Area Network => Internet (connect the world)
* SAN => Storage Area Network => server/storage devices



### Network Topologies

* Logical infrastructure
* Physical infrastructure
* bus, ring, star, mesh, tree, mesh, hybrid



### Switch = network switch

* managed switch => allow to change operating system setting
* unmanaged switch => plug and play (SOHO)



Network Card = Ethernet Card ( RJ-45, SFP, SFP+, QSFP+, QSFP28 )



Network = 8 wires => 4 work (2 transmitter and 2 receiver)



### Network Medium

* Guided => wire cable ( UTP, fiber Optic) cable
* Unguided => wireless (RF) (wireless ethernet card)



### Bandwidth

network Speed = depend on card not wire

|**Ethernet Standard**|**Bandwidth**|**Connector**|
|-|-|-|
|ethernet|10 mbps|RJ-45 / BNC|
|Fastethernet|100 mbps|RJ-45|
|Gigabitethernet|1000 mbps / 1 gbps|RJ-45 / SPF|
|Tengigabitethernet|10 gbps|SFP+|
|40gigabitethernet|40 gbps|QSFP+|
|100gigabitethernet|100 gbps|QSFP28|



\# UTP = 100 meters = 4pairs-8wires

\# Fiber Optic Cable needs SFP transceiver (transmitter + receiver)

### 

### MAC address (Physical Address)

in all ROM chipset

#### Notation

|colon hexadecimal notation|eg: 00:0a:83:b1:c0:8e|
|-|-|
|hyphen hexadecimal notation|eg: 00-0a-83-b1-c0-8e|
|period-separate hexadecimal notation|eg: 000.a83.b1c.08e|



MAC = Media Access Control

\#first 3 periods (24bits) => Organizationally Unique Identifier

\#last 3 periods (24bits) => Network Interface Controller Specific (can assign up to 2 to the power 24)

### 

### Traffic Type

* Unicast MAC => all computer network card
* Multicast MAC => 01-00-5e-xx-xx-xx
* Broadcast MAC => all f
* Any MAC => all 0



### Ethernet Switch

* forward ethernet frame
* use MAC address table / CAM table
* switch port table => each port (listening, learning = record SMAC address on table, forwarding = based on DMAC address)



### Router

* forward IP packet
* use IP routing table

\*connect different networks

### 

### PDU term (protocol data unit)

|application|data|
|-|-|
|presentation|data|
|session|data|
|transport|segment (Dport\|Sport\|...\|data)|
|network|packet (DIP\|SIP\|protocol\|...\|segment)|
|data-link|frame (DMAC\|SMAC\|ET\|packet\|fcs)|
|physical|bits (01.....)|



Ethernet frame

|DMAC|SMAC|ET|PACKET|FCS|
|-|-|-|-|-|
|48 bits = 6 bytes|48 bits = 6 bytes|16 bits = 2 bytes|1500B (MTU = maximum transmition unit)<br />#Jumbo packet = 9000B|frame check sequence/ checksum|

### 

### Fiber Optic Cable (glass core)

* single-mode (long distance) 1310 wavelength
* multi-mode (no more than 800 meters0 850 wavelength) => step-index/graded-index



### ARP Protocol

* mapping (IP+MAC) address
* ARP request packet ( to know DMAC address) => ethernet frame (broadcast/any MAC)
* ARP reply packet (unicast)
* ARP cache

