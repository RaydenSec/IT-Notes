VirtualBox Guest Additions: installed iinside vm after guest OS has installed, 
consists of device drivers etc to optimmise guest OS performance
eg. smoother mouse speed 

Ctrl+Alt+Delete to get in Windows Server 2019, in a VM, can be done via Input bar

Windows Server allows manual error entry and category into event viewer whenever there's a restart etc

VM network connections, w/ 1 being connected to internet, ipv4 assigned by DHCP, whilst second adapter looking for DHCP, but couldn't find it so was assigned APIPA address 169.xx
- So manually assign IP, and don't need to specify Default Gateway as this is for devices to access this server, and the other NIC (w/ DHCP IP) is for accessing the internet
- Windows Server automatically installs DNS server, so it can be its own DNS server (127.0.0.1)

Install AD DS on this server, there are many services you can install for this, then specify server from pool (only one in this case)
Create a new forest since first DC, specify domain 


Turn Server to AD server -> NAT (can forward traffic from devices in this private network devices to internet) -> DHCP on DC, so devices connected can be auto assigned IP

Can manage users and computers through AD domain controller: computers allow users to log in through them, deleting it will prevent users from logging into AD using it. 


Why add additional DCs to domain? For redundancy and load balancing

If client manually configures their IP (requires admin perms if connected with AD account), DHCP leases will not show for that IP
If Defautl Gateway for IP missing, add the default gateway in the AD server (should be itself since its redirecting traffic to internet) in DHCP. THen ipconfig /renew in client and see if there now is defautl gateway

Client WIndows Machines can directly connect to AD as default gateway because the network is set to internal network (For Virtualbox, it is an internal virtual netowrk avaialbe to any vm running on the host)
