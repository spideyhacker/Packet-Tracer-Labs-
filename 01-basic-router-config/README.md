Packet Tracer Lab 01: Basic Router Configuration 

**Goal:** Practice configuring a Cisco router with hostnames, interfaces, IP addresses, and basic security. 
---
## Topology 
- 1 Router
- 1 Switch
- 2 PCs
  ## Tasks performed for Router Configuration
  - Set router
  - Configured GigabitEthernet interfaces
  - Assigned IP addresses
  - Set console and VTY passwords
  - Configured service password-encryption
  - saved the running config
  ## Commands 
Router #conf term

Enter configuration commands, one per line.  End with CNTL/Z.

Router(config)#hostname R1 

R1(config)#interface g0/0/0

R1(config-if)#ip address 192.167.1.1 255.255.255.0

R1(config-if)#no shutdown

R1(config-if)#

%LINK-5-CHANGED: Interface GigabitEthernet0/0/0, changed state to up

R1(config-if)#line console 0

R1(config-line)#password cisco

R1(config-line)#login

R1(config-line)#service password-encryption

R1(config) #end

## PC1
- IP: 192.168.1.1
- Subnet: 255.255.255.0
- Gateway: 192.168.1.1
## PC2 
- IP: 192.164.1.1
- Subnet: 255.255.255.0
- Gateway: 192.168.1.1

  ### Switch config (S1)
  - en
  - conf term
  - hostname S1
  - interface range fa0/1-3
  - switchport mode access
  - no shutdown
  - end
  - write memory
 
    ## TESTING VERIFICATION COMMANDS
    - Pinging IP addresses from both PCs
    - Verified switch port status with:
    - show ip interface brief
    - Show interface status
    
## Key Takeaways
- Understanding how to navigate basic router modes
- Remembering to use 'no shutdown'
- Importance of encrypting passwords
- Saving configs with 'write memory'
  ## Future improvements
  - Add DHCp config
  - Add a second router for routing practice
 
    # LINK
  [PACKET TRACER PRACTICE CONFIGURING A LAN.zip](https://github.com/user-attachments/files/23686164/PACKET.TRACER.PRACTICE.CONFIGURING.A.LAN.zip) 
