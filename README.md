# 🛡️ SOC Homelab

## 📑 Table of Contents
- [Goals & Intention](#Goals--Intention)
- [Architecture](#architecture)
- [Plan](#Plan)
- [Progress](#Progress)
- [Future Steps](#future-steps)
- [Conclusion](#Conclusion)


## 🎯 Goals & Intention
My Goal is to develop relevant skills associated with security operations, pen-testings, networkings, and more.

I intend to built out my homelab to include many of these tools and technologies I intend to learn and practice, inluding Windows Server, VLANS, Splunk, and more.

## 🧱 Architecture

I wanted to segment and isolate my lab network, as it is for testing and may contain both intentional and unintentional vunerabilities.
It will include one machine running Debain server with Splunk, aggreating logs from the other machines: Windows Server 2022 with AD DS, and a Raspberry Pi 0 W.

![network](https://github.com/user-attachments/assets/4f407214-1e09-47dc-a9a3-a23d8bc456d4)


## Plan
1. Segment my homenetwork to make room for a secure homelab deploment.
2. Setup Windows Server 2022 with Active Directory Domain Services.
3. Setup Debina server with Splunk.
4. Setup legacy pi, and forward logs from all machines to Splunk.
5. Experiment with attacking and defending lab.

## Progress
1. I finished subnetting my network with one small hicup. I had my AP broadcasting multiple networks each with a unique VLAN assigned. However despite the ability to connect to the network(s), devices could not access the internet. It turns out I forgot to enable VLAN trunking on the port on the router, despite enabling it on the switch ports connecting to the router and ap. Enabling this setting corrected the issue.

2. I purchased two Dell optiplex 9020 micro's from Ebay, each with an Intel i5, 16GB DDr3 ram, and a 256GB SSD. This was plently to meet my requirements. I installed Windows Server 2022 on the first machine and began configuring it. My next issue began with configuring wifi on the machine, as I had limited space next to my switch, especially in terms of outlet space. The NIC was visable in BIOS, but not at all in Windows. Thus I worked to install the driver, and Windows refused it. From research I concluded that the Intel(R) Dual Band Wireless-AC 7260 was not compatible. I was able to scrap another NIC from a dell laptop, this one beng Qualcomm instead of Intel, and the drivers successfully installed and wifi operated as intended.

## Future Steps
-Maybe add cloud connection, IPSEC tunnel to Azure VNET
-Some reports including threat models, and en test writups

## Conclusion
