<div align="center">

<img src="./assets/hybrid.png" alt="Microsoft Hybrid Cloud Zero to Hero Banner">

<br><br>

<img src="https://img.shields.io/badge/Microsoft-5E5E5E?style=for-the-badge&logo=microsoft&logoColor=white">
<img src="https://img.shields.io/badge/Level-Beginner%20to%20Advanced-purple?style=for-the-badge">
<img src="https://img.shields.io/badge/Windows%20Server-0078D4?style=for-the-badge&logo=windows&logoColor=white">
<img src="https://img.shields.io/badge/Active%20Directory-0078D4?style=for-the-badge&logo=microsoft&logoColor=white">
<img src="https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white">
<img src="https://img.shields.io/badge/Entra%20ID-Identity-blue?style=for-the-badge&logo=microsoft&logoColor=white">
<img src="https://img.shields.io/badge/Microsoft%20365-Cloud-blue?style=for-the-badge&logo=microsoft&logoColor=white">

<br>

<img src="https://img.shields.io/badge/Contributions-Welcome-brightgreen?style=for-the-badge">

</div>

<div align="center">

# Microsoft Hybrid Cloud — Zero to Hero

### ☁️ From on-premises infrastructure to modern Microsoft hybrid cloud — comprehensive explanations, hands-on labs, troubleshooting, automation, and real-world architecture.

</div>

---

## 📖 About This Repository

**Microsoft Hybrid Cloud Zero to Hero** is a structured, project-based learning repository designed to take you from the fundamentals of IT infrastructure all the way through building, managing, securing, and automating modern Microsoft hybrid cloud environments.

The learning journey starts with **networking and Windows Server fundamentals**, progresses through **DNS, DHCP, Active Directory, Group Policy, file and storage services, Hyper-V, PowerShell, and advanced Active Directory administration**, and then connects these on-premises technologies with **Microsoft Azure, Microsoft Entra ID, and Microsoft 365**.

The repository also covers modern Microsoft security and endpoint technologies including **Microsoft Intune, Microsoft Defender, Microsoft Purview, Zero Trust, and Microsoft Graph**.

Every section is organized into its own folder with a dedicated `README.md` containing detailed explanations, architecture diagrams, configuration walkthroughs, verification steps, troubleshooting scenarios, and hands-on labs.

The content progresses logically from **on-premises infrastructure → hybrid identity → cloud administration → Microsoft 365 → security → automation**.

By the end of this course, you will be able to:

- ✅ Understand core IT infrastructure, networking, virtualization, and server concepts
- ✅ Deploy and administer Windows Server environments
- ✅ Configure and troubleshoot DNS and DHCP services
- ✅ Build and manage Active Directory Domain Services environments
- ✅ Create and manage users, groups, computers, OUs, and domain controllers
- ✅ Implement centralized administration using Group Policy
- ✅ Configure and manage file servers, NTFS permissions, SMB shares, and storage
- ✅ Build virtualization environments using Hyper-V
- ✅ Understand AD replication, Sites and Services, Global Catalog, FSMO roles, and SYSVOL
- ✅ Implement Windows Server security, certificates, auditing, backup, and recovery
- ✅ Automate infrastructure administration using PowerShell
- ✅ Deploy and manage Azure resources and networking
- ✅ Implement identity and access management using Microsoft Entra ID
- ✅ Configure MFA, SSPR, Conditional Access, Enterprise Applications, SSO, PIM, and Identity Governance
- ✅ Connect on-premises Active Directory with Microsoft Entra ID using hybrid identity technologies
- ✅ Administer Microsoft 365 users, groups, licensing, and tenant settings
- ✅ Manage Exchange Online, SharePoint Online, OneDrive, and Microsoft Teams
- ✅ Manage devices and applications using Microsoft Intune
- ✅ Protect identities, endpoints, email, and cloud workloads using Microsoft Defender
- ✅ Implement data protection and compliance using Microsoft Purview
- ✅ Apply Zero Trust security principles across hybrid environments
- ✅ Automate Microsoft 365 and Entra administration using Microsoft Graph and PowerShell
- ✅ Design and troubleshoot real-world Microsoft hybrid cloud architectures

---

## 📚 Table of Contents

---

## 1. IT Infrastructure Fundamentals

This section introduces the foundations of enterprise IT infrastructure, including client-server architecture, on-premises environments, virtualization, storage, and the core components used in traditional enterprise environments.

📂 **[Explore → IT Infrastructure Fundamentals](./IT%20Infrastructure%20Fundamentals/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 1.1 | [Client-Server Architecture](./IT%20Infrastructure%20Fundamentals/Client-Server%20Architecture/) | Understanding clients, servers, services, and enterprise applications |
| 1.2 | [On-Premises Infrastructure](./IT%20Infrastructure%20Fundamentals/On-Premises%20Infrastructure/) | Understanding traditional enterprise infrastructure and data centers |
| 1.3 | [Enterprise Infrastructure Components](./IT%20Infrastructure%20Fundamentals/Enterprise%20Infrastructure%20Components/) | Servers, storage, networking, applications, and infrastructure services |
| 1.4 | [Virtualization Fundamentals](./IT%20Infrastructure%20Fundamentals/Virtualization%20Fundamentals/) | Understanding virtual machines and virtualization concepts |
| 1.5 | [Storage Fundamentals](./IT%20Infrastructure%20Fundamentals/Storage%20Fundamentals/) | Disks, partitions, volumes, RAID, and storage concepts |
| 1.6 | [Infrastructure Management](./IT%20Infrastructure%20Fundamentals/Infrastructure%20Management/) | Monitoring, administration, documentation, and maintenance |

---

## 2. Networking Fundamentals

This section builds the networking foundation required for Windows Server, Active Directory, Microsoft cloud services, and hybrid cloud environments.

📂 **[Explore → Networking Fundamentals](./Networking%20Fundamentals/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 2.1 | [OSI Model](./Networking%20Fundamentals/OSI%20Model/) | Understanding the seven layers of networking |
| 2.2 | [TCP/IP Model](./Networking%20Fundamentals/TCP%20IP%20Model/) | Understanding the TCP/IP networking architecture |
| 2.3 | [IPv4 Addressing](./Networking%20Fundamentals/IPv4%20Addressing/) | Public, private, network, host, and broadcast addresses |
| 2.4 | [Subnetting](./Networking%20Fundamentals/Subnetting/) | CIDR, subnet masks, network ranges, and subnet calculations |
| 2.5 | [TCP and UDP](./Networking%20Fundamentals/TCP%20and%20UDP/) | Understanding transport protocols and communication |
| 2.6 | [Ports and Protocols](./Networking%20Fundamentals/Ports%20and%20Protocols/) | Common enterprise networking ports and protocols |
| 2.7 | [Routing Fundamentals](./Networking%20Fundamentals/Routing%20Fundamentals/) | Static routing, default gateways, and routing concepts |
| 2.8 | [NAT](./Networking%20Fundamentals/NAT/) | Network Address Translation and its use cases |
| 2.9 | [Firewalls](./Networking%20Fundamentals/Firewalls/) | Network traffic filtering and access control |
| 2.10 | [Network Troubleshooting](./Networking%20Fundamentals/Network%20Troubleshooting/) | Ping, tracert, ipconfig, nslookup, Test-NetConnection, and troubleshooting |

---

## 3. Windows Server

This section introduces Windows Server administration and the tools required to deploy, configure, manage, and troubleshoot enterprise Windows servers.

📂 **[Explore → Windows Server](./Windows%20Server/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 3.1 | [Windows Server Fundamentals](./Windows%20Server/Windows%20Server%20Fundamentals/) | Windows Server architecture, editions, and core concepts |
| 3.2 | [Windows Server Installation](./Windows%20Server/Windows%20Server%20Installation/) | Installing and performing initial server configuration |
| 3.3 | [Server Manager](./Windows%20Server/Server%20Manager/) | Managing server roles, features, and administration |
| 3.4 | [Server Core](./Windows%20Server/Server%20Core/) | Deploying and managing Windows Server without a GUI |
| 3.5 | [Windows Services](./Windows%20Server/Windows%20Services/) | Managing and troubleshooting Windows services |
| 3.6 | [Event Viewer](./Windows%20Server/Event%20Viewer/) | Monitoring and analyzing Windows event logs |
| 3.7 | [Windows Firewall](./Windows%20Server/Windows%20Firewall/) | Configuring Windows Defender Firewall |
| 3.8 | [Local Users and Groups](./Windows%20Server/Local%20Users%20and%20Groups/) | Managing local accounts and groups |
| 3.9 | [Windows Server Administration](./Windows%20Server/Windows%20Server%20Administration/) | Common administration, monitoring, and troubleshooting tasks |

---

## 4. DNS and DHCP

This section covers the essential network services required for Windows Server and Active Directory environments.

📂 **[Explore → DNS and DHCP](./DNS%20and%20DHCP/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 4.1 | [DNS Fundamentals](./DNS%20and%20DHCP/DNS%20Fundamentals/) | Understanding DNS and name resolution |
| 4.2 | [DNS Zones](./DNS%20and%20DHCP/DNS%20Zones/) | Forward and reverse lookup zones |
| 4.3 | [DNS Records](./DNS%20and%20DHCP/DNS%20Records/) | A, AAAA, CNAME, MX, PTR, and SRV records |
| 4.4 | [DNS Forwarders](./DNS%20and%20DHCP/DNS%20Forwarders/) | Configuring external DNS resolution |
| 4.5 | [Dynamic DNS](./DNS%20and%20DHCP/Dynamic%20DNS/) | Understanding and configuring DDNS |
| 4.6 | [DHCP Fundamentals](./DNS%20and%20DHCP/DHCP%20Fundamentals/) | Understanding automatic IP configuration |
| 4.7 | [DHCP Scopes](./DNS%20and%20DHCP/DHCP%20Scopes/) | Creating and managing DHCP scopes |
| 4.8 | [DHCP Reservations](./DNS%20and%20DHCP/DHCP%20Reservations/) | Assigning predictable IP addresses |
| 4.9 | [DHCP Options](./DNS%20and%20DHCP/DHCP%20Options/) | Gateway, DNS, domain, and other DHCP options |
| 4.10 | [DNS and DHCP Troubleshooting](./DNS%20and%20DHCP/DNS%20and%20DHCP%20Troubleshooting/) | Diagnosing common DNS and DHCP problems |

---

## 5. Active Directory Domain Services

This section provides a practical understanding of Active Directory Domain Services and the identity infrastructure used in enterprise Windows environments.

📂 **[Explore → Active Directory Domain Services](./Active%20Directory%20Domain%20Services/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 5.1 | [AD DS Fundamentals](./Active%20Directory%20Domain%20Services/AD%20DS%20Fundamentals/) | Understanding Active Directory and directory services |
| 5.2 | [Domains](./Active%20Directory%20Domain%20Services/Domains/) | Understanding Windows domains |
| 5.3 | [Trees and Forests](./Active%20Directory%20Domain%20Services/Trees%20and%20Forests/) | Understanding AD forest architecture |
| 5.4 | [Domain Controllers](./Active%20Directory%20Domain%20Services/Domain%20Controllers/) | Deploying and managing Domain Controllers |
| 5.5 | [Organizational Units](./Active%20Directory%20Domain%20Services/Organizational%20Units/) | Designing and managing OUs |
| 5.6 | [Users](./Active%20Directory%20Domain%20Services/Users/) | Creating and managing domain users |
| 5.7 | [Groups](./Active%20Directory%20Domain%20Services/Groups/) | Security groups, distribution groups, and group membership |
| 5.8 | [Computers](./Active%20Directory%20Domain%20Services/Computers/) | Managing domain-joined computers |
| 5.9 | [Domain Join](./Active%20Directory%20Domain%20Services/Domain%20Join/) | Joining Windows clients and servers to a domain |
| 5.10 | [Authentication](./Active%20Directory%20Domain%20Services/Authentication/) | Windows authentication fundamentals |
| 5.11 | [LDAP and Global Catalog](./Active%20Directory%20Domain%20Services/LDAP%20and%20Global%20Catalog/) | Directory queries and Global Catalog |
| 5.12 | [Service Accounts](./Active%20Directory%20Domain%20Services/Service%20Accounts/) | Managing accounts used by applications and services |
| 5.13 | [Delegation](./Active%20Directory%20Domain%20Services/Delegation/) | Delegating administrative permissions |
| 5.14 | [AD Recycle Bin](./Active%20Directory%20Domain%20Services/AD%20Recycle%20Bin/) | Recovering deleted Active Directory objects |

---

## 6. Group Policy

This section covers centralized configuration, security, and management of Windows users and computers through Group Policy.

📂 **[Explore → Group Policy](./Group%20Policy/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 6.1 | [Group Policy Fundamentals](./Group%20Policy/Group%20Policy%20Fundamentals/) | Understanding GPO architecture |
| 6.2 | [Creating GPOs](./Group%20Policy/Creating%20GPOs/) | Creating and managing Group Policy Objects |
| 6.3 | [GPO Linking](./Group%20Policy/GPO%20Linking/) | Linking policies to domains and OUs |
| 6.4 | [User Configuration](./Group%20Policy/User%20Configuration/) | Managing user settings |
| 6.5 | [Computer Configuration](./Group%20Policy/Computer%20Configuration/) | Managing computer settings |
| 6.6 | [GPO Inheritance](./Group%20Policy/GPO%20Inheritance/) | Understanding policy inheritance and precedence |
| 6.7 | [Security Filtering](./Group%20Policy/Security%20Filtering/) | Controlling which users and computers receive policies |
| 6.8 | [Enterprise Policies](./Group%20Policy/Enterprise%20Policies/) | Password, firewall, update, and security policies |
| 6.9 | [Drive Mapping](./Group%20Policy/Drive%20Mapping/) | Deploying network drives using Group Policy |
| 6.10 | [GPO Troubleshooting](./Group%20Policy/GPO%20Troubleshooting/) | gpupdate, gpresult, RSOP, and troubleshooting |

---

## 7. File and Storage Services

This section covers Windows file servers, SMB, NTFS permissions, shares, storage management, and enterprise file services.

📂 **[Explore → File and Storage Services](./File%20and%20Storage%20Services/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 7.1 | [File Server Fundamentals](./File%20and%20Storage%20Services/File%20Server%20Fundamentals/) | Understanding Windows file servers |
| 7.2 | [SMB](./File%20and%20Storage%20Services/SMB/) | Understanding Server Message Block |
| 7.3 | [File Shares](./File%20and%20Storage%20Services/File%20Shares/) | Creating and managing network shares |
| 7.4 | [NTFS Permissions](./File%20and%20Storage%20Services/NTFS%20Permissions/) | Managing file and folder permissions |
| 7.5 | [Share Permissions](./File%20and%20Storage%20Services/Share%20Permissions/) | Configuring share-level permissions |
| 7.6 | [Effective Permissions](./File%20and%20Storage%20Services/Effective%20Permissions/) | Understanding combined permissions |
| 7.7 | [Storage Management](./File%20and%20Storage%20Services/Storage%20Management/) | Managing disks, volumes, and storage |
| 7.8 | [File Server Security](./File%20and%20Storage%20Services/File%20Server%20Security/) | Securing enterprise file services |

---

## 8. Hyper-V and Virtualization

This section covers Microsoft Hyper-V and virtualization technologies used to build and operate the hands-on enterprise lab environment.

📂 **[Explore → Hyper-V and Virtualization](./Hyper-V%20and%20Virtualization/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 8.1 | [Virtualization Fundamentals](./Hyper-V%20and%20Virtualization/Virtualization%20Fundamentals/) | Understanding virtualization concepts |
| 8.2 | [Hyper-V](./Hyper-V%20and%20Virtualization/Hyper-V/) | Understanding Microsoft Hyper-V |
| 8.3 | [Virtual Machines](./Hyper-V%20and%20Virtualization/Virtual%20Machines/) | Creating and managing virtual machines |
| 8.4 | [Virtual Switches](./Hyper-V%20and%20Virtualization/Virtual%20Switches/) | External, internal, and private virtual switches |
| 8.5 | [Virtual Disks](./Hyper-V%20and%20Virtualization/Virtual%20Disks/) | VHDX and virtual storage |
| 8.6 | [Checkpoints](./Hyper-V%20and%20Virtualization/Checkpoints/) | Managing VM checkpoints |
| 8.7 | [VM Networking](./Hyper-V%20and%20Virtualization/VM%20Networking/) | Connecting and configuring lab machines |
| 8.8 | [Virtualization Labs](./Hyper-V%20and%20Virtualization/Virtualization%20Labs/) | Hands-on virtualization and lab environment exercises |

---

## 9. PowerShell for Windows Administration

This section teaches PowerShell for Windows Server, Active Directory, DNS, DHCP, automation, and enterprise administration.

📂 **[Explore → PowerShell for Windows Administration](./PowerShell%20for%20Windows%20Administration/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 9.1 | [PowerShell Fundamentals](./PowerShell%20for%20Windows%20Administration/PowerShell%20Fundamentals/) | Commands, cmdlets, objects, and the PowerShell environment |
| 9.2 | [Variables and Data Types](./PowerShell%20for%20Windows%20Administration/Variables%20and%20Data%20Types/) | Managing PowerShell data |
| 9.3 | [Pipeline](./PowerShell%20for%20Windows%20Administration/Pipeline/) | Working with the PowerShell pipeline |
| 9.4 | [Conditions and Loops](./PowerShell%20for%20Windows%20Administration/Conditions%20and%20Loops/) | Automating administrative logic |
| 9.5 | [Functions](./PowerShell%20for%20Windows%20Administration/Functions/) | Creating reusable PowerShell code |
| 9.6 | [Filtering and Formatting](./PowerShell%20for%20Windows%20Administration/Filtering%20and%20Formatting/) | Selecting, filtering, and formatting objects |
| 9.7 | [CSV and Reporting](./PowerShell%20for%20Windows%20Administration/CSV%20and%20Reporting/) | Importing, exporting, and generating reports |
| 9.8 | [Windows Server Administration](./PowerShell%20for%20Windows%20Administration/Windows%20Server%20Administration/) | Managing Windows Server with PowerShell |
| 9.9 | [Active Directory PowerShell](./PowerShell%20for%20Windows%20Administration/Active%20Directory%20PowerShell/) | Managing Active Directory using PowerShell |
| 9.10 | [DNS and DHCP PowerShell](./PowerShell%20for%20Windows%20Administration/DNS%20and%20DHCP%20PowerShell/) | Automating network services |
| 9.11 | [PowerShell Remoting](./PowerShell%20for%20Windows%20Administration/PowerShell%20Remoting/) | Remote administration using PowerShell |
| 9.12 | [Automation Labs](./PowerShell%20for%20Windows%20Administration/Automation%20Labs/) | Practical Windows administration automation |

---

## 10. Active Directory Advanced Concepts

This section covers advanced Active Directory architecture, replication, domain controllers, sites, FSMO roles, SYSVOL, and enterprise troubleshooting.

📂 **[Explore → Active Directory Advanced Concepts](./Active%20Directory%20Advanced%20Concepts/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 10.1 | [AD Replication](./Active%20Directory%20Advanced%20Concepts/AD%20Replication/) | Understanding directory replication |
| 10.2 | [Sites and Services](./Active%20Directory%20Advanced%20Concepts/Sites%20and%20Services/) | Designing and managing AD sites |
| 10.3 | [Global Catalog](./Active%20Directory%20Advanced%20Concepts/Global%20Catalog/) | Understanding Global Catalog servers |
| 10.4 | [FSMO Roles](./Active%20Directory%20Advanced%20Concepts/FSMO%20Roles/) | Understanding and managing FSMO roles |
| 10.5 | [SYSVOL](./Active%20Directory%20Advanced%20Concepts/SYSVOL/) | Understanding SYSVOL |
| 10.6 | [DFSR](./Active%20Directory%20Advanced%20Concepts/DFSR/) | SYSVOL replication using DFSR |
| 10.7 | [Domain Controller Management](./Active%20Directory%20Advanced%20Concepts/Domain%20Controller%20Management/) | Managing multiple Domain Controllers |
| 10.8 | [AD Troubleshooting](./Active%20Directory%20Advanced%20Concepts/AD%20Troubleshooting/) | Diagnosing replication and authentication issues |

---

## 11. Windows Server Security

This section covers Windows Server security, hardening, auditing, firewall configuration, least privilege, and endpoint protection.

📂 **[Explore → Windows Server Security](./Windows%20Server%20Security/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 11.1 | [Windows Security Fundamentals](./Windows%20Server%20Security/Windows%20Security%20Fundamentals/) | Understanding Windows security architecture |
| 11.2 | [Microsoft Defender](./Windows%20Server%20Security/Microsoft%20Defender/) | Endpoint protection fundamentals |
| 11.3 | [Windows Firewall](./Windows%20Server%20Security/Windows%20Firewall/) | Host-based firewall security |
| 11.4 | [Security Policies](./Windows%20Server%20Security/Security%20Policies/) | Local and domain security policies |
| 11.5 | [Auditing](./Windows%20Server%20Security/Auditing/) | Windows security auditing |
| 11.6 | [Least Privilege](./Windows%20Server%20Security/Least%20Privilege/) | Managing administrative privileges |
| 11.7 | [Server Hardening](./Windows%20Server%20Security/Server%20Hardening/) | Enterprise Windows Server hardening |
| 11.8 | [Security Labs](./Windows%20Server%20Security/Security%20Labs/) | Practical Windows security scenarios |

---

## 12. Backup and Recovery

This section covers Windows Server backup, system state protection, Active Directory recovery, file recovery, and disaster recovery.

📂 **[Explore → Backup and Recovery](./Backup%20and%20Recovery/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 12.1 | [Backup Fundamentals](./Backup%20and%20Recovery/Backup%20Fundamentals/) | Backup strategies and concepts |
| 12.2 | [Windows Server Backup](./Backup%20and%20Recovery/Windows%20Server%20Backup/) | Configuring Windows Server Backup |
| 12.3 | [System State Backup](./Backup%20and%20Recovery/System%20State%20Backup/) | Protecting Windows system state |
| 12.4 | [Active Directory Recovery](./Backup%20and%20Recovery/Active%20Directory%20Recovery/) | Recovering Active Directory |
| 12.5 | [File Recovery](./Backup%20and%20Recovery/File%20Recovery/) | Recovering files and folders |
| 12.6 | [Disaster Recovery](./Backup%20and%20Recovery/Disaster%20Recovery/) | Enterprise disaster recovery planning |
| 12.7 | [Recovery Labs](./Backup%20and%20Recovery/Recovery%20Labs/) | Practical backup and recovery scenarios |

---

## 13. Hybrid Identity

This section connects on-premises Active Directory with Microsoft cloud identity services. Detailed Microsoft Entra ID administration is covered separately in the dedicated Entra ID learning path.

📂 **[Explore → Hybrid Identity](./Hybrid%20Identity/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 13.1 | [Hybrid Identity Fundamentals](./Hybrid%20Identity/Hybrid%20Identity%20Fundamentals/) | Understanding hybrid identity architecture |
| 13.2 | [Microsoft Entra Connect](./Hybrid%20Identity/Microsoft%20Entra%20Connect/) | Connecting on-premises AD with cloud identity |
| 13.3 | [Microsoft Entra Cloud Sync](./Hybrid%20Identity/Microsoft%20Entra%20Cloud%20Sync/) | Lightweight directory synchronization |
| 13.4 | [Password Hash Synchronization](./Hybrid%20Identity/Password%20Hash%20Synchronization/) | Understanding PHS |
| 13.5 | [Pass-through Authentication](./Hybrid%20Identity/Pass-through%20Authentication/) | Understanding PTA |
| 13.6 | [Federation Concepts](./Hybrid%20Identity/Federation%20Concepts/) | Understanding federated authentication |
| 13.7 | [User Principal Name](./Hybrid%20Identity/User%20Principal%20Name/) | UPN and identity synchronization |
| 13.8 | [Hybrid Join](./Hybrid%20Identity/Hybrid%20Join/) | Understanding hybrid device identity |
| 13.9 | [Synchronization Troubleshooting](./Hybrid%20Identity/Synchronization%20Troubleshooting/) | Diagnosing synchronization problems |
| 13.10 | [Hybrid Identity Lab](./Hybrid%20Identity/Hybrid%20Identity%20Lab/) | Building an on-premises to cloud identity environment |

---

## 14. Microsoft 365 Administration

This section introduces Microsoft 365 administration and the core management concepts required for enterprise environments.

📂 **[Explore → Microsoft 365 Administration](./Microsoft%20365%20Administration/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 14.1 | [Microsoft 365 Fundamentals](./Microsoft%20365%20Administration/Microsoft%20365%20Fundamentals/) | Understanding Microsoft 365 |
| 14.2 | [Microsoft 365 Admin Center](./Microsoft%20365%20Administration/Microsoft%20365%20Admin%20Center/) | Central Microsoft 365 administration |
| 14.3 | [Users](./Microsoft%20365%20Administration/Users/) | Managing Microsoft 365 users |
| 14.4 | [Groups](./Microsoft%20365%20Administration/Groups/) | Microsoft 365 and security groups |
| 14.5 | [Licensing](./Microsoft%20365%20Administration/Licensing/) | Managing Microsoft 365 licenses |
| 14.6 | [Domains](./Microsoft%20365%20Administration/Domains/) | Adding and managing domains |
| 14.7 | [Service Health](./Microsoft%20365%20Administration/Service%20Health/) | Monitoring Microsoft 365 services |
| 14.8 | [Administration Labs](./Microsoft%20365%20Administration/Administration%20Labs/) | Practical Microsoft 365 administration |

---

## 15. Exchange Online

This section covers Exchange Online administration, mailboxes, mail flow, messaging policies, connectors, security, and troubleshooting.

📂 **[Explore → Exchange Online](./Exchange%20Online/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 15.1 | [Exchange Online Fundamentals](./Exchange%20Online/Exchange%20Online%20Fundamentals/) | Understanding cloud email |
| 15.2 | [Mailboxes](./Exchange%20Online/Mailboxes/) | Creating and managing mailboxes |
| 15.3 | [Distribution Groups](./Exchange%20Online/Distribution%20Groups/) | Managing distribution groups |
| 15.4 | [Mail Flow](./Exchange%20Online/Mail%20Flow/) | Understanding message delivery |
| 15.5 | [Mail Flow Rules](./Exchange%20Online/Mail%20Flow%20Rules/) | Creating transport rules |
| 15.6 | [Connectors](./Exchange%20Online/Connectors/) | Configuring mail connectors |
| 15.7 | [Message Trace](./Exchange%20Online/Message%20Trace/) | Troubleshooting email delivery |
| 15.8 | [Exchange Online Protection](./Exchange%20Online/Exchange%20Online%20Protection/) | Email security fundamentals |
| 15.9 | [Exchange Online Labs](./Exchange%20Online/Exchange%20Online%20Labs/) | Practical messaging administration |

---

## 16. SharePoint Online and OneDrive

This section covers document management, collaboration, permissions, sharing, and OneDrive administration.

📂 **[Explore → SharePoint Online and OneDrive](./SharePoint%20Online%20and%20OneDrive/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 16.1 | [SharePoint Fundamentals](./SharePoint%20Online%20and%20OneDrive/SharePoint%20Fundamentals/) | Understanding SharePoint Online |
| 16.2 | [Sites](./SharePoint%20Online%20and%20OneDrive/Sites/) | Creating and managing SharePoint sites |
| 16.3 | [Permissions](./SharePoint%20Online%20and%20OneDrive/Permissions/) | Managing SharePoint access |
| 16.4 | [Sharing](./SharePoint%20Online%20and%20OneDrive/Sharing/) | Internal and external sharing |
| 16.5 | [OneDrive Fundamentals](./SharePoint%20Online%20and%20OneDrive/OneDrive%20Fundamentals/) | Understanding personal cloud storage |
| 16.6 | [OneDrive Sync](./SharePoint%20Online%20and%20OneDrive/OneDrive%20Sync/) | Configuring synchronization |
| 16.7 | [External Sharing](./SharePoint%20Online%20and%20OneDrive/External%20Sharing/) | Managing external collaboration |
| 16.8 | [SharePoint and OneDrive Labs](./SharePoint%20Online%20and%20OneDrive/SharePoint%20and%20OneDrive%20Labs/) | Practical collaboration scenarios |

---

## 17. Microsoft Teams

This section covers Microsoft Teams administration, collaboration, guest access, policies, meetings, and external communication.

📂 **[Explore → Microsoft Teams](./Microsoft%20Teams/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 17.1 | [Teams Fundamentals](./Microsoft%20Teams/Teams%20Fundamentals/) | Understanding Microsoft Teams |
| 17.2 | [Teams and Channels](./Microsoft%20Teams/Teams%20and%20Channels/) | Creating teams and channels |
| 17.3 | [Team Permissions](./Microsoft%20Teams/Team%20Permissions/) | Managing team membership |
| 17.4 | [Guest Access](./Microsoft%20Teams/Guest%20Access/) | External guest collaboration |
| 17.5 | [External Access](./Microsoft%20Teams/External%20Access/) | External communication |
| 17.6 | [Teams Policies](./Microsoft%20Teams/Teams%20Policies/) | Managing Teams policies |
| 17.7 | [Meetings](./Microsoft%20Teams/Meetings/) | Meeting administration |
| 17.8 | [Teams Labs](./Microsoft%20Teams/Teams%20Labs/) | Practical Teams administration |

---

## 18. Microsoft Intune

This section introduces cloud-based endpoint management, device enrollment, configuration, compliance, applications, endpoint security, and Windows Autopilot.

📂 **[Explore → Microsoft Intune](./Microsoft%20Intune/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 18.1 | [Intune Fundamentals](./Microsoft%20Intune/Intune%20Fundamentals/) | Understanding endpoint management |
| 18.2 | [Device Enrollment](./Microsoft%20Intune/Device%20Enrollment/) | Enrolling devices into Intune |
| 18.3 | [Configuration Profiles](./Microsoft%20Intune/Configuration%20Profiles/) | Managing device configurations |
| 18.4 | [Compliance Policies](./Microsoft%20Intune/Compliance%20Policies/) | Defining device compliance |
| 18.5 | [Application Management](./Microsoft%20Intune/Application%20Management/) | Deploying and managing applications |
| 18.6 | [Windows Autopilot](./Microsoft%20Intune/Windows%20Autopilot/) | Modern Windows deployment |
| 18.7 | [Endpoint Security](./Microsoft%20Intune/Endpoint%20Security/) | Managing endpoint security policies |
| 18.8 | [Intune Labs](./Microsoft%20Intune/Intune%20Labs/) | Practical endpoint management |

---

## 19. Microsoft Defender

This section introduces Microsoft's security ecosystem for identity, endpoints, email, collaboration, and extended detection and response.

📂 **[Explore → Microsoft Defender](./Microsoft%20Defender/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 19.1 | [Microsoft Defender Fundamentals](./Microsoft%20Defender/Microsoft%20Defender%20Fundamentals/) | Understanding the Microsoft Defender ecosystem |
| 19.2 | [Defender for Office 365](./Microsoft%20Defender/Defender%20for%20Office%20365/) | Protecting email and collaboration services |
| 19.3 | [Defender for Endpoint](./Microsoft%20Defender/Defender%20for%20Endpoint/) | Endpoint detection and protection |
| 19.4 | [Defender for Identity](./Microsoft%20Defender/Defender%20for%20Identity/) | Protecting Active Directory identities |
| 19.5 | [Microsoft Defender XDR](./Microsoft%20Defender/Microsoft%20Defender%20XDR/) | Extended detection and response |
| 19.6 | [Incidents and Alerts](./Microsoft%20Defender/Incidents%20and%20Alerts/) | Investigating security incidents |
| 19.7 | [Threat Hunting](./Microsoft%20Defender/Threat%20Hunting/) | Basic threat hunting concepts |
| 19.8 | [Security Operations](./Microsoft%20Defender/Security%20Operations/) | SOC-oriented security workflows |
| 19.9 | [Defender Labs](./Microsoft%20Defender/Defender%20Labs/) | Practical security scenarios |

---

## 20. Microsoft Purview

This section introduces data security, information protection, compliance, retention, DLP, eDiscovery, and insider risk management.

📂 **[Explore → Microsoft Purview](./Microsoft%20Purview/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 20.1 | [Purview Fundamentals](./Microsoft%20Purview/Purview%20Fundamentals/) | Understanding Microsoft Purview |
| 20.2 | [Sensitivity Labels](./Microsoft%20Purview/Sensitivity%20Labels/) | Protecting sensitive information |
| 20.3 | [Data Loss Prevention](./Microsoft%20Purview/Data%20Loss%20Prevention/) | Preventing data leakage |
| 20.4 | [Retention](./Microsoft%20Purview/Retention/) | Managing organizational data retention |
| 20.5 | [eDiscovery](./Microsoft%20Purview/eDiscovery/) | Discovering organizational data |
| 20.6 | [Insider Risk](./Microsoft%20Purview/Insider%20Risk/) | Understanding insider risk management |
| 20.7 | [Compliance Management](./Microsoft%20Purview/Compliance%20Management/) | Managing Microsoft 365 compliance |
| 20.8 | [Purview Labs](./Microsoft%20Purview/Purview%20Labs/) | Practical compliance scenarios |

---

## 21. Zero Trust

This section introduces the Zero Trust security model and how identity, devices, applications, networks, and data are protected in modern hybrid environments.

📂 **[Explore → Zero Trust](./Zero%20Trust/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 21.1 | [Zero Trust Fundamentals](./Zero%20Trust/Zero%20Trust%20Fundamentals/) | Understanding the Zero Trust security model |
| 21.2 | [Verify Explicitly](./Zero%20Trust/Verify%20Explicitly/) | Identity and access verification |
| 21.3 | [Least Privilege](./Zero%20Trust/Least%20Privilege/) | Limiting access to required resources |
| 21.4 | [Assume Breach](./Zero%20Trust/Assume%20Breach/) | Designing for compromised environments |
| 21.5 | [Identity Security](./Zero%20Trust/Identity%20Security/) | Protecting organizational identities |
| 21.6 | [Device Security](./Zero%20Trust/Device%20Security/) | Protecting endpoints and devices |
| 21.7 | [Application Security](./Zero%20Trust/Application%20Security/) | Securing applications and workloads |
| 21.8 | [Data Security](./Zero%20Trust/Data%20Security/) | Protecting organizational data |
| 21.9 | [Zero Trust Architecture](./Zero%20Trust/Zero%20Trust%20Architecture/) | Designing a Zero Trust environment |
| 21.10 | [Zero Trust Labs](./Zero%20Trust/Zero%20Trust%20Labs/) | Practical Zero Trust security scenarios |

---

## 22. Microsoft Graph and Automation

This section introduces Microsoft Graph and automation techniques for managing Microsoft cloud services programmatically.

📂 **[Explore → Microsoft Graph and Automation](./Microsoft%20Graph%20and%20Automation/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 22.1 | [Microsoft Graph Fundamentals](./Microsoft%20Graph%20and%20Automation/Microsoft%20Graph%20Fundamentals/) | Understanding Microsoft Graph |
| 22.2 | [Graph Explorer](./Microsoft%20Graph%20and%20Automation/Graph%20Explorer/) | Exploring Microsoft Graph APIs |
| 22.3 | [Graph PowerShell](./Microsoft%20Graph%20and%20Automation/Graph%20PowerShell/) | Managing Microsoft services with PowerShell |
| 22.4 | [API Authentication](./Microsoft%20Graph%20and%20Automation/API%20Authentication/) | Understanding application authentication |
| 22.5 | [User Automation](./Microsoft%20Graph%20and%20Automation/User%20Automation/) | Automating user administration |
| 22.6 | [Group Automation](./Microsoft%20Graph%20and%20Automation/Group%20Automation/) | Automating group management |
| 22.7 | [Bulk Administration](./Microsoft%20Graph%20and%20Automation/Bulk%20Administration/) | Managing large environments |
| 22.8 | [Automation Projects](./Microsoft%20Graph%20and%20Automation/Automation%20Projects/) | Building practical automation solutions |

---

## 23. Troubleshooting

This section provides practical troubleshooting scenarios across networking, Windows Server, Active Directory, Group Policy, hybrid identity, and Microsoft 365.

📂 **[Explore → Troubleshooting](./Troubleshooting/)**

| # | Sub-Topic | Description |
|---|-----------|-------------|
| 23.1 | [Network Troubleshooting](./Troubleshooting/Network%20Troubleshooting/) | Diagnosing connectivity and routing issues |
| 23.2 | [DNS Troubleshooting](./Troubleshooting/DNS%20Troubleshooting/) | Diagnosing name resolution problems |
| 23.3 | [DHCP Troubleshooting](./Troubleshooting/DHCP%20Troubleshooting/) | Diagnosing IP assignment problems |
| 23.4 | [Windows Server Troubleshooting](./Troubleshooting/Windows%20Server%20Troubleshooting/) | Services, events, firewall, and system issues |
| 23.5 | [Active Directory Troubleshooting](./Troubleshooting/Active%20Directory%20Troubleshooting/) | Diagnosing authentication and domain issues |
| 23.6 | [Replication Troubleshooting](./Troubleshooting/Replication%20Troubleshooting/) | Diagnosing AD replication failures |
| 23.7 | [Group Policy Troubleshooting](./Troubleshooting/Group%20Policy%20Troubleshooting/) | Diagnosing GPO application issues |
| 23.8 | [File Server Troubleshooting](./Troubleshooting/File%20Server%20Troubleshooting/) | Diagnosing permissions and SMB problems |
| 23.9 | [Hybrid Identity Troubleshooting](./Troubleshooting/Hybrid%20Identity%20Troubleshooting/) | Diagnosing synchronization problems |
| 23.10 | [Microsoft 365 Troubleshooting](./Troubleshooting/Microsoft%20365%20Troubleshooting/) | Common Microsoft 365 administration issues |
| 23.11 | [Enterprise Troubleshooting Scenarios](./Troubleshooting/Enterprise%20Troubleshooting%20Scenarios/) | Real-world infrastructure troubleshooting scenarios |

---

## 24. Enterprise Projects

This final section combines the technologies learned throughout the repository into realistic enterprise infrastructure projects, progressing from traditional on-premises infrastructure to a complete hybrid Microsoft environment.

📂 **[Explore → Enterprise Projects](./Enterprise%20Projects/)**

| # | Project | Description |
|---|---------|-------------|
| 24.1 | [On-Premises Enterprise](./Enterprise%20Projects/On-Premises%20Enterprise/) | Build a complete Windows Server enterprise environment |
| 24.2 | [Secure Enterprise Environment](./Enterprise%20Projects/Secure%20Enterprise%20Environment/) | Implement enterprise security and server hardening |
| 24.3 | [Multi-Site Active Directory](./Enterprise%20Projects/Multi-Site%20Active%20Directory/) | Design and deploy a multi-site AD environment |
| 24.4 | [Enterprise PowerShell Automation](./Enterprise%20Projects/Enterprise%20PowerShell%20Automation/) | Automate Windows Server and Active Directory administration |
| 24.5 | [Hybrid Identity Environment](./Enterprise%20Projects/Hybrid%20Identity%20Environment/) | Connect on-premises Active Directory with Microsoft cloud identity |
| 24.6 | [Microsoft 365 Enterprise](./Enterprise%20Projects/Microsoft%20365%20Enterprise/) | Deploy and administer Microsoft 365 services |
| 24.7 | [Modern Endpoint Management](./Enterprise%20Projects/Modern%20Endpoint%20Management/) | Manage Windows devices using Microsoft Intune |
| 24.8 | [Microsoft Security Environment](./Enterprise%20Projects/Microsoft%20Security%20Environment/) | Implement Microsoft Defender security capabilities |
| 24.9 | [Data Protection and Compliance](./Enterprise%20Projects/Data%20Protection%20and%20Compliance/) | Implement Microsoft Purview security and compliance |
| 24.10 | [Complete Hybrid Cloud](./Enterprise%20Projects/Complete%20Hybrid%20Cloud/) | Build an end-to-end hybrid Microsoft environment |
| 24.11 | [Final Capstone Project](./Enterprise%20Projects/Final%20Capstone%20Project/) | Integrate infrastructure, identity, management, security, and automation |

---

## 🤝 Contributing

Contributions are welcome!

If you have suggestions for improvements, new examples, better explanations, or find any issues, feel free to:

- Open an issue
- Submit a pull request
- Improve existing documentation
- Add useful examples or diagrams

Please keep contributions beginner-friendly, accurate, and consistent with the structure of this repository.

---

<div align="center">

**Happy Hybrid Infra Building! ☁️**

*If this repo helped you, please consider giving it a ⭐*

</div>

