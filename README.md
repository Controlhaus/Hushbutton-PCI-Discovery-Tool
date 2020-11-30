# Hushbutton-PCI-Discovery-Tool  

## Network Setup  
If DHCP is available, the PCI will automatically use DHCP to obtain an IP Address.  
If DHCP is not available, the PCI will assign itself an address in the 169.254.x.x range. Multiple PCI's on the same network will dynamically assign themselves unique IP Addresses in this range. Adjusting a PC with the following network settings will allow the Device Discovery Tool to communicate with PCI's in this address range.  
• IP Address: 169.254.0.1  
• Subnet Mask: 255.255.0.0  

## Laptop Setup  
Windows 10 users need to add `Hushbutton_PCI_Discovery_Tool.exe` to the list of allowed apps in the Windows Defender firewall. Without this setting, PCI's with a different IP Address from the laptop will not be visible in the Discovery Tool.  

## Using the PCI Discovery Tool  
Once a PCI is installed on the same network as a PC, the PCI Discovery Tool can be used to assign the PCI a static IP Address.  
To install the PCI Discovery Tool, unzip the Hushbutton_PCI_Discovery_Tool.zip folder and open the file setup.exe  

Clicking `Scan for Devices` will populate the `Devices found:` box with the MAC Addresses of all the PCI boards on the local network.  

Clicking `ID Selected Device` will turn the LED's of the selected PCI MAC address on.  

Entering `IP-Address`, `Network Mask`, `Default Gateway` and clicking `ID Selected Device` will set the entered information on the selected PCI MAC address.  

Entering `0.0.0.0` for the `IP-Address` and `Network Mask` and clicking ID Selected Device will enable DHCP.  

## PCI Network Reset  
To force the PCI to rescan for DHCP servers, either:  
- reboot the PCI's power  
- or use a paper clip to press the `RESET` button.  
