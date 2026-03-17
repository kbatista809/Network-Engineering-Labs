# Lab Documentation
Step 1 - Create VLANs (Vlan 10 Sales, Vlan 20 Engineeering, Vlan 30 HR, Vlan 40 IT) A VLAN (Virtual LAN) logically separates networks even if they share the same physical switch. This prevents unnecessary broadcast traffic. (show vlan brief - to verify)

Step 2 - Configure VTP (VTP allows one switch to distribute VLANs to other switches.) Core1 is the server, Core2,Dist1,Dist2 are clients.

Step 3 - Configure Trunk Ports (Trunks allow multiple VLANs across a single cable.) Core1 and Core2 Trunks (show interfaces trunk - to verify)

Step 4 - Configure EtherChannel (We bundle links between DIST1 and CORE1. interface range g0/1 - 2 channel-group 1 mode active 
interface port-channel 1 switchport mode trunk ) (show etherchannel summary - to verify) 

Step 5 - Spanning Tree (We want CORE1 to be root bridge.) 

Step 6 - Configure Access Ports (Assign PCs to VLANs. interface fa0/1 switchport mode access switchport access vlan 10 etc..) DIST1 and DIST2

Step 7 - Configure PCs IP Address

communication is Layer 2 only, Same VLAN communication works the switch forwards frames using MAC address table. Different VLAN communication will NOT work, We need a Layer 3 device (router or L3 switch) to route between VLANs.
