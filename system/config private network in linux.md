# Configuring a private network in Linux
## Table of Content
1. [Centos](##Centos)
2. [Ubuntu]()
3. [Debian]()

 Show all network interface and determining the private network interface
```# ip addr```
In this example, the name of the unconfigured network interface for the private network is **eth0**
## Centos
Use vi to create the configuration file for unconfigured interface. The path file name of this interface wil have the following format:
```/etc/sysconfig/network-scripts/ifcfg-[name of interface]```
**Example**:

To configure the private network, enter the following information:
```
NAME="Private [NAME_OF_THE_PRIVATE_NETWORK_INTERFACE]"  
DEVICE="[NAME_OF_THE_PRIVATE_NETWORK_INTERFACE]"  
IPADDR="[IP_ADDRESS_OF_THE_SERVER_IN_THE_PRIVATE_NETWORK]"  
NETMASK="[SUBNET_MASK_OF_THE_PRIVATE_NETWORK]"  
HWADDR="[MAC_ADDRESS]"  
BOOTPROTO="none"  
ONBOOT="yes"  
USERCTL="no"```

**Example**

Restart network interface:
```ifup [name of interface]```