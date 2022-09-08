Reading Notes <br>
Class 08<br>
Re: Virtualbox Network Settings<br>

*This document is a summary of information in the article linked within.*<br><br>

## VirtualBox Network Settings: Complete Guide
https://www.nakivo.com/blog/virtualbox-network-setting-guide/<br><br>

**Virtualbox Network Modes:** 

- Not Attached<br>
- NAT<br>
- NAT Network<br>
- Bridged Adapter<br>
- Internal Network<br>
- Host-Only Adapter<br>
- Generic Driver

In virtualbox, the virtual network adapters = (NIC) Network Interface Controller

**VBoxManage modifyvm** command = <br>
- to configure any of the virtual network adapters in the GUI of virtualbox<br>
- VBoxManage = command line tool for vbox
    - configures all vbox settings, incl network settings
    - or use the vm's network settings<br><br>


### Types of Virtual Network Adapters in VirtualBox<br><br>

***AMD PCnet-PCI II (Am79C970A).*** 
- based on AMD chip <br>
- can be used for older Windows versions (newer Windows versions such as Windows 7, 8, 10 do not contain a built-in driver for it. 
- supports AMD’s Magic Packet technology for remote wake-up.<br><br>

***AMD PCnet-FAST III (Am79C973).*** <br>
- supported by almost all guest operating systems 
- GRUB (the boot loader) can use it for network boot. 
based AMD chip.
- works with newer Windows versions ,most Linux distributions <br><br>

***Intel PRO/1000 T Server (82543GC).*** 
- useful for importing OVF templates from other platforms 

***Paravirtualized Network Adapter*** 
- (virtio-net) is a special case. 
- guest operating system must provide a special software interface for virtualized environments 
- avoids complexity of networking hardware emulating 
- can improve network performance.
