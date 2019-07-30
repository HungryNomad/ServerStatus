# ServerStatus
Work in progress  - A collection of tools to allow admins to query info about a system.

Main
	- Ask if want to do a standard scan
		○ Yes, proceed with the defaults
		○ No, change settings > Settings menu
	- Discovery
		○ DHCP Scan
			§ DHCP AD Lookup
			§ DHCP Scopes ( exempt tag )
			§ Leased IPs
		○ DNS Lookup
			§ Grab all A addresses
		○ AD Lookup
			§ Scan for Server OS
	- Display list
		○ Allow toggle of systems not to scan
	- Scan the systems
		○ Get-StatusAlive (Use NMAP instead?)
			§ Ping? Ports? NMAP? WMI? RPC? RDP Ping!)
		○ Get-StatusHDD
		○ Get-StatusServices
		○ Get-StatusReboot
		○ Get-StatusPatches
		

Deliverables
	- Name
	- IP
	- Status
		○ Good
		○ Low hard drive space
		○ Offline
	- Free HDD space GB
	- Free HDD space %
	- Stopped Auto Services
	- Reboot pending

Main
	- Default settings? 
		○ No, configure settings
	- Get-ADServerList (DC?)
		○ (DC?)
			§ Look up DC
		○ Query 
	
Functions
	- Set-SSSettings (obj settings) return (obj settings)
		○ Display settings
		○ Allow modify
	- Get-StatusDHCPDump
	- Get-StatusDNSDump
	- Get-StatusHDD
	- Get-StatusServices
	
		
Variables


User defined (stored in .xml)
	- Settings
		○ .useAD (bool)
		○ .useDHCP (bool)
		○ .useDNS (bool)
		○ .DNSServer (IP/Name)
		○ .ADServer (IP/Name)
		○ .DHCPServer (IP/Name)
		○ .UseRDPPing(bool) Mandatory?
		○ .OUPath (DN)
