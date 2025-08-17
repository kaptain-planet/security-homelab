# Security Home Lab for Training 
Documenting the process for setting up a home lab for security training for myself and those looking to get into Information Security/Cybersecurity. 

## Overview 
This project will mainly provide resources I used during my initial setup to create a virtualized segmented environment within my home network. Virtualization will be a big part of this lab but it will be locally hosted. 

## Network Diagram (Mine) created via [draw.io](https://github.com/jgraph/drawio-desktop)
This is the visual representation of my security lab environment. It is not completely finished so I will continue to make updates to this image and the documentation.

![security lab diagram](https://github.com/kaptain-planet/security-homelab/blob/27631ed60d00d1ed8ae13edb5f432a609366c8e2/HomeLab_2025.png)

| VLAN ID               | Purpose             | Devices |
| --------------------- | ------------------- | ------- |
| **1**                 | Mgmt Network        | PfSense <br> EVE-NG <br> Ubuntu Server <br> IDS: Security Onion | 
| **10 (vtnet1.10)**    | Attack Network      | Kali Linux (Red Team) / Metasploit |
| **20 (vtnet1.20)**    | Victim Network      | Vulnerable machines: WIN 10 Machine and Linux <br> Active Directory (WIN Server 2019) <br> DVWA (done) <br> VULNHUB (done) <br> bWAPP (done) |
| **30 (vtnet1.30)**    | SOC Network         | Incident Response: TheHive <br> Internal Vulnerability Scanner: OpenVAS <br> SIEM: The ELK Stack or Wazuh <br> MISP Threat Sharing  <br> Kali Purple (done) |

## Foundation: Components of the Lab
It is essential to have the right hardware and software in place to make sure the lab has the capacity to function as expected with differnt tasks. 

### Hardware & Software Requirements 
When it comes to hardware it all comes down to what type of environment you want and what tasks you will be running/performing. <br> 
I am currently using the below hardware to run the [Proxmox](https://www.proxmox.com/en/) virtualization software on. 

+ Device: Intel NUC12WSHi7
+ CPU: 12-Core i7-1260P
+ RAM: 32GB DDR4
+ Storage: 1TB SSD M/2 NVME + 500GB WD SATA SSD

> [!NOTE]
> You can find various intel nuc models on ebay for a very resonable price for your lab hardware.

| Software Tools        | Role                             | Status  |
| --------------------- | -------------------------------- | ------- |
| **PfSense**           | Open-source Firewall (gateway)   | ✅ Done |
| **TheHive**           | Incident Response Platform       | Planned |
| **Wazuh**             | SIEM Solution                    | Planned |
| **OpenVAS**           | Vulnerability Scanner            | Planned |
| **Security Onion**    | Intrusion Detection System (IDS) | Planned |
| **MISP**              | Threat Intelligence Sharing      | Planned |
| **Kali Purple**       | Security Operations OS           | ✅ Done |
| **EVE-NG**            | Network Simulation               | ✅ Done |

### ✅ Current Status Summary

+ Management and Attack networks are set up.
+ Victim and SOC networks partially complete.
+ Next steps: Focus on SIEM and Incident Response components.

### 🔗 Helpful Resources
📺 Video Tutorials

+ [Building a Home SOC Lab - Part 1 (Gerard O'Brien)(Best Resource)](https://www.youtube.com/watch?v=gTCZ-g-cbbE)
+ [Building a Home SOC Lab - Part 2 (Gerard O'Brien)](https://www.youtube.com/watch?v=XIvn0ZDSmKA)
+ [Building the Ultimate Cybersecurity Lab - Episode 1 (7-Part Series) (Gerard O'Brien) (Best Resource)](https://youtu.be/XIvn0ZDSmKA?si=h53nOC22MWdXaaV0)
+ [Nessus Vulnerability Scan Tuturial (Gerard O'Brien)](https://youtu.be/FANQcjzVfzg?si=uAiAcSUjo-q7Kp0F)
+ [Windows Server 2022 - Active Directory - Proxmox Install](https://www.youtube.com/watch?v=bEoGu50G09E)
+ [Terraform 2-Part Series (Gerard O'Brien) ](https://youtu.be/roCHue3uPD4?si=gLfEyy46Mlv0ioon)

📘 Blog Posts & Articles

+ [Building a Home SOC Lab (ELK Stack SIEM) – Khalid Chbail](https://medium.com/@khalid.chbail4/building-a-home-soc-lab-part-1-elk-stack-siem-solution-b82dd396836f)
+ [SOC Lab – Threat Detection & Defense – iritt.medium9](https://iritt.medium.com/soc-lab-building-a-cybersecurity-environment-for-threat-detection-and-defense-7785ef70c75e)
+ [Understanding Wazuh – OSINTph](https://osintph.medium.com/understanding-wazuh-the-free-open-source-security-platform-for-xdr-siem-48b3c3dfba9d)
+ [Homelab Hardware & Topology Overview – emhedge.medium](https://medium.com/@emhedge/homelab-learning-a-general-overview-of-my-homelab-hardware-and-topology-d4ef3a7336b1)
+ [Installing pfSense on Proxmox – ZenArmor Docs](https://www.zenarmor.com/docs/network-security-tutorials/how-to-install-pfsense-software-on-proxmox)
+ [David Varghese - Building a Virtual Security Home Lab](https://blog.davidvarghese.net/posts/building-home-lab-part-1/)

🌐 Networking Resources

+ [Proxmox VE 8.1 Network Configuration – BDRSuite](https://www.bdrsuite.com/blog/understanding-network-configuration-in-proxmox-ve-8-1/)
+ [pfSense User Management – Netgate Docs](https://docs.netgate.com/pfsense/en/latest/usermanager/defaults.html)
+ [Linux Routing with ip command – CyberCiti.biz](https://www.cyberciti.biz/faq/howto-linux-configuring-default-route-with-ipcommand/)
+ [Kali Purple Documentation – GitLab](https://gitlab.com/kalilinux/kali-purple/documentation/-/wikis/home)
+ [Proxmox Beginner Tutorial – Proxmox Forum](https://forum.proxmox.com/threads/proxmox-beginner-tutorial-how-to-set-up-your-first-virtual-machine-on-a-secondary-hard-disk.59559/)

## About Me 
LinkedIn: [Christopher Armon](https://www.linkedin.com/in/chrisarmon) 









