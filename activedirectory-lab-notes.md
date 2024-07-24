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


Turn Server to AD server -> NAT (so private network devices can talk to outside through DC) -> DHCP on DC, so devices connected can be auto assigned IP
