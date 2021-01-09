<font face="Dejavu Sans"/>

# ItC Week 13 - Network

###### tags: `Intro_to_Comp`

- ## Network Interface Card
  - Every networked device must have one
    - some motherboards/laptops might have both a wired one and a wireless one
  - Each NIC has an IP address (logical address) and a physical address (MAC address)
    - MAC address is unique, given to a NIC at factory
  - MAC addresses are used within LAN
  - IP addresses are used accross different nerworks

- ## Hub
  - Connects network devices
  - A device sends a message to the hub, and the hub send that message to all the other connected devices
    - unintended recipients should ignore bogus traffic
  - Can only deal with one message at a time

- ## Switch
  - Acts like a hub, but only direct the traffic to intended destination instead of spamming all devices
  - An "Intelligent hub"
  - Avoid "packing sniffing" when message is not encrypted

- ## Routers
  - Different networks connect via routers (NOT switch or hub)
  - Can connect networks with different protocols
  - Gateway router
    - your computer &rarr; gateway router &rarr; a computer on the other network
    - your computer &rarr; gateway router &rarr; ISP's network (Internet)

- ## TCP/IP & Packet
  - Provides the technical foundation for public internet
  - Layers
    - Applications
    - Transport
    - Internet
    - Network Interface
  - ![TCP/IP Layers](https://i.imgur.com/t0xCJsD.png)
  - ![Sending packet](https://i.imgur.com/6XKmdF9.png)

- ## Wireless Networking
  - WiFi : a means of implementing WLAN
  - aka 802.11

- ## Some Scenario
  - ![](https://i.imgur.com/KgrAn3L.png)
  - 



{%hackmd OQo9p0ONRaSb9WIkZQZZ7w %}