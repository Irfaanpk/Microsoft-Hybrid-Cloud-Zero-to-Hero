# On-Premises Infrastructure

On-premises infrastructure refers to IT systems and resources that are physically deployed, owned, or directly managed by an organization within its own facilities or data centers.

Before organizations widely adopted cloud computing, most enterprise workloads were hosted on-premises. Even today, many organizations continue to operate on-premises infrastructure because of legacy applications, regulatory requirements, security requirements, performance requirements, or business needs.

Understanding on-premises infrastructure is important for anyone working with Windows Server, Active Directory, Microsoft 365, hybrid identity, and hybrid cloud environments.

---

## 1. What is On-Premises Infrastructure?

On-premises infrastructure is an organization's internally managed IT environment.

It can include:

- Physical servers
- Virtual machines
- Network devices
- Storage systems
- Firewalls
- Load balancers
- Active Directory
- DNS
- DHCP
- File servers
- Application servers
- Database servers
- Backup systems
- Monitoring systems
- Physical facilities

A simplified environment looks like:

```text
                    Organization
                         │
                         ↓
                   Data Center
                         │
        ┌────────────────┼────────────────┐
        ↓                ↓                ↓
     Servers          Storage          Network
        │                │                │
        ├── AD DS        │                ├── Switches
        ├── DNS          │                ├── Routers
        ├── DHCP         │                ├── Firewalls
        ├── Files        │                └── Load Balancers
        └── Applications │
                         ↓
                    Backup System
````

The organization is responsible for managing the infrastructure and the services running on it.

---

## 2. Components of On-Premises Infrastructure

An enterprise on-premises environment consists of multiple infrastructure layers.

```text
┌──────────────────────────────────────┐
│          Business Applications       │
├──────────────────────────────────────┤
│          Operating Systems           │
├──────────────────────────────────────┤
│       Virtual Machines / Servers     │
├──────────────────────────────────────┤
│          Storage Infrastructure      │
├──────────────────────────────────────┤
│          Network Infrastructure      │
├──────────────────────────────────────┤
│       Physical Data Center           │
└──────────────────────────────────────┘
```

Each layer depends on the layers below it.

---

## 3. Physical Infrastructure

Physical infrastructure represents the hardware and facilities required to operate IT systems.

Common components include:

* Server hardware
* Network switches
* Routers
* Firewalls
* Storage systems
* Rack cabinets
* Power systems
* Cooling systems
* Cabling
* Backup power
* Physical security

A simplified data-center environment may look like:

```text
                 Data Center
                      │
        ┌─────────────┼─────────────┐
        ↓             ↓             ↓
     Servers       Networking     Storage
        │             │             │
        ↓             ↓             ↓
       VMs         Switches        SAN
                    Routers        NAS
                   Firewalls
```

Physical infrastructure provides the foundation for all higher-level services.

---

## 4. Data Center

A data center is a facility designed to host IT infrastructure.

An enterprise data center may contain:

```text
┌──────────────────────────────────────┐
│              Data Center             │
│                                      │
│  ┌─────────┐  ┌─────────┐            │
│  │ Rack 01  │  │ Rack 02 │   ...      │
│  └─────────┘  └─────────┘            │
│                                      │
│  Power                                │
│  Cooling                              │
│  Networking                           │
│  Physical Security                    │
│  Monitoring                           │
└──────────────────────────────────────┘
```

### 4.1 Data Center Requirements

A data center generally requires:

* Reliable electricity
* Backup power
* Cooling
* Network connectivity
* Fire detection and suppression
* Physical access controls
* Environmental monitoring
* Hardware monitoring
* Redundant infrastructure

Organizations may also operate multiple data centers for disaster recovery and business continuity.

---

## 5. Server Hardware

A physical server is a computer specifically designed to provide services and resources to other systems.

Typical server components include:

| Component             | Purpose                            |
| --------------------- | ---------------------------------- |
| CPU                   | Processes instructions             |
| RAM                   | Provides temporary working memory  |
| Storage               | Stores operating systems and data  |
| NIC                   | Provides network connectivity      |
| RAID Controller       | Manages disk redundancy            |
| Power Supply          | Provides electrical power          |
| Management Controller | Enables remote hardware management |
| Cooling               | Maintains operating temperature    |

A typical enterprise server can be represented as:

```text
┌─────────────────────────────────┐
│        Physical Server          │
│                                 │
│  CPU                            │
│  RAM                            │
│  Storage                        │
│  Network Interfaces             │
│  RAID Controller                │
│  Power Supplies                 │
│  Hardware Management            │
└─────────────────────────────────┘
```

---

## 6. Server Types

Organizations may use different server configurations depending on their requirements.

### 6.1 Tower Servers

Tower servers resemble traditional desktop towers.

They are commonly used in:

* Small businesses
* Branch offices
* Small deployments

### 6.2 Rack Servers

Rack servers are designed to be installed in server racks.

```text
┌─────────────────────────┐
│       Server Rack       │
├─────────────────────────┤
│       Server 01         │
├─────────────────────────┤
│       Server 02         │
├─────────────────────────┤
│       Server 03         │
├─────────────────────────┤
│       Network Switch    │
├─────────────────────────┤
│       Storage           │
└─────────────────────────┘
```

Rack servers are common in enterprise data centers.

### 6.3 Blade Servers

Blade servers use a shared chassis containing multiple server blades.

```text
┌─────────────────────────────┐
│       Blade Chassis         │
│                             │
│ ┌────┐ ┌────┐ ┌────┐       │
│ │ B1 │ │ B2 │ │ B3 │  ...  │
│ └────┘ └────┘ └────┘       │
│                             │
│ Shared Power / Networking   │
└─────────────────────────────┘
```

Blade infrastructure can provide high-density server deployments.

---

## 7. Network Infrastructure

Network infrastructure connects clients, servers, storage, and external networks.

Common components include:

* Switches
* Routers
* Firewalls
* Load balancers
* Wireless infrastructure
* Network cables
* Network interfaces

A simplified enterprise network looks like:

```text
                         Internet
                            │
                            ↓
                       ┌─────────┐
                       │Firewall │
                       └────┬────┘
                            │
                       ┌────▼────┐
                       │ Router  │
                       └────┬────┘
                            │
                       ┌────▼────┐
                       │ Switch  │
                       └────┬────┘
             ┌──────────────┼──────────────┐
             ↓              ↓              ↓
          Servers        Storage        Clients
```

Networking fundamentals such as IP addressing, subnetting, routing, TCP/IP, ports, and firewalls are covered in the **Networking Fundamentals** section.

---

## 8. Storage Infrastructure

Enterprise environments require storage for operating systems, applications, databases, user files, backups, and other data.

Common storage technologies include:

* Local storage
* Direct-Attached Storage (DAS)
* Network-Attached Storage (NAS)
* Storage Area Network (SAN)

### 8.1 DAS

Direct-Attached Storage is directly connected to a server.

```text
Server
  │
  │ Direct Connection
  ↓
Storage
```

### 8.2 NAS

Network-Attached Storage provides file-based storage over a network.

```text
Clients
   │
   ↓
Network
   │
   ↓
NAS
   │
   ↓
Files
```

### 8.3 SAN

A Storage Area Network provides block-level storage to servers over a dedicated storage network.

```text
        ┌───────────┐
        │  Server   │
        └─────┬─────┘
              │
              ↓
        Storage Network
              │
              ↓
        ┌───────────┐
        │    SAN    │
        └───────────┘
```

Storage becomes especially important when designing virtualization, file servers, databases, and backup infrastructure.

---

## 9. Operating Systems

Servers require operating systems to manage hardware and provide services.

Common enterprise operating systems include:

* Windows Server
* Linux distributions
* VMware ESXi and other virtualization platforms

In a Microsoft-focused enterprise environment, Windows Server provides many important capabilities.

Examples include:

```text
Windows Server
     │
     ├── Active Directory Domain Services
     ├── DNS
     ├── DHCP
     ├── File Services
     ├── IIS
     ├── Hyper-V
     └── Windows Server Security
```

The Windows Server section of this repository will provide hands-on administration starting from server installation.

---

## 10. Virtualization

Virtualization allows multiple virtual machines to run on a physical server.

Without virtualization:

```text
┌───────────────────┐
│ Physical Server   │
│                   │
│ Application       │
└───────────────────┘
```

With virtualization:

```text
┌─────────────────────────────────┐
│       Physical Server           │
│                                 │
│          Hypervisor              │
│               │                 │
│     ┌─────────┼─────────┐       │
│     ↓         ↓         ↓       │
│   VM01      VM02      VM03      │
│   DC01      FILE01    WEB01     │
└─────────────────────────────────┘
```

Each virtual machine can run its own operating system and applications.

Virtualization provides:

* Better hardware utilization
* Isolation
* Easier provisioning
* Flexible resource allocation
* Snapshot/checkpoint capabilities
* Simplified testing
* Easier disaster recovery

Hyper-V and virtualization will be covered later in the repository.

---

## 11. Hypervisor

A hypervisor is software or firmware that creates and manages virtual machines.

There are two common categories.

### 11.1 Type 1 Hypervisor

A Type 1 hypervisor runs directly on physical hardware.

```text
┌──────────────────────────┐
│     Physical Hardware   │
├──────────────────────────┤
│      Hypervisor         │
├─────────┬──────┬─────────┤
│   VM01  │ VM02 │  VM03   │
└─────────┴──────┴─────────┘
```

Examples include:

* Microsoft Hyper-V
* VMware ESXi

### 11.2 Type 2 Hypervisor

A Type 2 hypervisor runs on top of a host operating system.

```text
┌──────────────────────────┐
│     Physical Hardware   │
├──────────────────────────┤
│      Host OS             │
├──────────────────────────┤
│      Hypervisor          │
├─────────┬──────┬─────────┤
│   VM01  │ VM02 │  VM03   │
└─────────┴──────┴─────────┘
```

Type 2 virtualization is commonly used for desktop development and learning environments.

---

## 12. Enterprise Services

On-premises infrastructure hosts many services required by an organization.

A typical Microsoft environment may include:

```text
                    Enterprise
                        │
        ┌───────────────┼────────────────┐
        ↓               ↓                ↓
    Identity         Network          Storage
        │               │                │
     AD DS             DNS             Files
     Users             DHCP            Shares
     Groups            Routing         Backup
     GPO               Firewall        Recovery
```

These services work together.

For example:

```text
User
 │
 ↓
Client Computer
 │
 │ Authentication
 ↓
Active Directory
 │
 │ DNS Resolution
 ↓
DNS
 │
 │ Network Access
 ↓
File Server
```

---

## 13. Active Directory in On-Premises Infrastructure

Active Directory Domain Services is a central component of many traditional Microsoft enterprise environments.

A simplified architecture is:

```text
                 Active Directory
                       │
          ┌────────────┼────────────┐
          ↓            ↓            ↓
        Users        Groups      Computers
          │            │            │
          └────────────┼────────────┘
                       ↓
                    Policies
                       │
                       ↓
                   Clients
```

Active Directory can provide centralized:

* Identity management
* Authentication
* Authorization
* Computer management
* Group management
* Policy management

Detailed Active Directory concepts will be covered in a later section.

---

## 14. Infrastructure Redundancy

Enterprise infrastructure should avoid unnecessary single points of failure.

For example, instead of using one domain controller:

```text
Clients
   │
   ↓
  DC01
```

an enterprise may deploy multiple domain controllers:

```text
              Clients
                 │
          ┌──────┴──────┐
          ↓             ↓
        DC01           DC02
          │             │
          └──────┬──────┘
                 │
           Active Directory
```

Similarly, organizations may use redundancy for:

* Network switches
* Firewalls
* Power supplies
* Storage
* Servers
* Internet connections
* Data centers

Redundancy improves availability and reduces the impact of individual component failures.

---

## 15. High Availability

High availability aims to keep services operational even when individual components fail.

A simple example:

```text
             Application
                  │
             ┌────┴────┐
             ↓         ↓
           Server01  Server02
             │         │
             └────┬────┘
                  ↓
               Storage
```

If one server becomes unavailable, another server may continue providing the service depending on the architecture.

High availability is different from backup.

**High availability** focuses on maintaining service availability.

**Backup** focuses on recovering data or systems after loss or corruption.

---

## 16. Backup Infrastructure

On-premises environments require backup systems to protect data and workloads.

A simplified backup architecture is:

```text
Production Servers
       │
       │ Backup
       ↓
Backup Server
       │
       ↓
Backup Storage
       │
       ↓
Offsite / Secondary Copy
```

Backups may protect:

* Files
* Databases
* Virtual machines
* Operating systems
* Active Directory
* Application data
* Configuration data

Backup and recovery will be covered in detail later in this repository.

---

## 17. Monitoring and Management

Enterprise infrastructure must be monitored continuously.

Organizations monitor:

* CPU usage
* Memory usage
* Disk space
* Network traffic
* Server health
* Application health
* Security events
* Hardware failures
* Service availability

A simplified monitoring architecture:

```text
Servers
   │
   ├──────────────┐
   ↓              ↓
Applications    Systems
   │              │
   └──────┬───────┘
          ↓
     Monitoring
       System
          │
          ↓
       Alerts
```

Monitoring helps administrators identify problems before they become major incidents.

---

## 18. Security in On-Premises Infrastructure

Security must be implemented across every infrastructure layer.

```text
┌───────────────────────────────┐
│          Applications         │
├───────────────────────────────┤
│          Identity             │
├───────────────────────────────┤
│          Servers              │
├───────────────────────────────┤
│          Network              │
├───────────────────────────────┤
│          Storage              │
├───────────────────────────────┤
│          Physical             │
└───────────────────────────────┘
```

Security controls may include:

* Physical access control
* Network firewalls
* Endpoint protection
* Server hardening
* Least privilege
* Authentication
* Authorization
* Encryption
* Security monitoring
* Auditing
* Backup protection

Security will be explored in greater detail in the Windows Server Security, Microsoft Defender, Microsoft Purview, and Zero Trust sections.

---

## 19. On-Premises Infrastructure Management

Managing an enterprise environment involves many responsibilities.

Administrators may manage:

| Area           | Examples                                 |
| -------------- | ---------------------------------------- |
| Servers        | Installation, configuration, maintenance |
| Networking     | Switches, routers, firewalls             |
| Storage        | Capacity, performance, availability      |
| Identity       | Users, groups, authentication            |
| Applications   | Deployment and maintenance               |
| Security       | Hardening, monitoring, auditing          |
| Backup         | Backup policies and recovery             |
| Virtualization | VMs, hosts, virtual networks             |
| Monitoring     | Logs, alerts, health                     |
| Automation     | PowerShell and scripts                   |

This requires administrators to understand how infrastructure components depend on one another.

---

## 20. Infrastructure Dependencies

Enterprise infrastructure is highly interconnected.

For example, a Windows client joining an Active Directory domain may depend on:

```text
Client
  │
  ├── Network Connectivity
  │
  ↓
IP Configuration
  │
  ├── IP Address
  ├── Subnet Mask
  ├── Default Gateway
  └── DNS Server
          │
          ↓
        DNS
          │
          ↓
    Domain Controller
          │
          ↓
    Active Directory
```

If DNS is incorrectly configured, domain operations may fail even when the network itself is reachable.

This is why infrastructure administrators need to understand dependencies between services.

---

## 21. On-Premises Infrastructure vs Cloud Infrastructure

On-premises and cloud environments both provide computing resources, but their operational responsibilities differ.

| Area                    | On-Premises                      | Cloud                                        |
| ----------------------- | -------------------------------- | -------------------------------------------- |
| Physical hardware       | Organization                     | Cloud provider                               |
| Data center             | Organization                     | Cloud provider                               |
| Hardware maintenance    | Organization                     | Cloud provider                               |
| Network infrastructure  | Organization                     | Shared/provider-managed depending on service |
| Server OS               | Organization                     | Varies by service model                      |
| Applications            | Organization                     | Customer/provider depending on service       |
| Scaling                 | Requires infrastructure planning | Often more flexible                          |
| Capital expenditure     | Usually higher                   | Often shifted toward operational consumption |
| Physical security       | Organization                     | Cloud provider                               |
| Infrastructure location | Organization facilities          | Cloud provider facilities                    |

The exact division of responsibilities depends on the cloud service model.

---

## 22. On-Premises and Hybrid Cloud

Organizations do not always move everything to the cloud.

Many enterprises operate hybrid environments.

```text
                 Organization
                       │
          ┌────────────┴────────────┐
          ↓                         ↓
     On-Premises                  Cloud
          │                         │
   ┌──────┼──────┐           ┌──────┼──────┐
   ↓      ↓      ↓           ↓      ↓      ↓
   AD    Files  Apps        M365   Intune Defender
          │                         │
          └──────────┬──────────────┘
                     ↓
              Hybrid Environment
```

A hybrid environment can allow organizations to retain existing infrastructure while adopting cloud services.

This is particularly relevant to Microsoft environments where organizations may have:

```text
On-Premises
   │
   ├── Windows Server
   ├── Active Directory
   ├── DNS
   ├── File Services
   └── Group Policy
          │
          ↓
    Hybrid Identity
          │
          ↓
Microsoft Cloud
   │
   ├── Microsoft 365
   ├── Intune
   ├── Defender
   └── Purview
```

The detailed hybrid identity architecture will be covered later in this repository.

---

## 23. Infrastructure Lifecycle

On-premises infrastructure follows a lifecycle.

```text
Plan
  ↓
Design
  ↓
Purchase
  ↓
Deploy
  ↓
Configure
  ↓
Operate
  ↓
Monitor
  ↓
Maintain
  ↓
Upgrade
  ↓
Retire
```

Each stage requires planning and documentation.

For example, before deploying a new server, administrators should consider:

* Business requirements
* Hardware requirements
* Network requirements
* Storage requirements
* Security requirements
* Backup requirements
* Availability requirements
* Monitoring requirements
* Licensing
* Future scalability

---

## 24. Why On-Premises Infrastructure Matters for Hybrid Cloud

Understanding on-premises infrastructure is especially important when working with hybrid cloud environments.

Cloud technologies do not eliminate the need to understand traditional infrastructure.

For example:

```text
On-Premises Knowledge
        │
        ├── Networking
        ├── Windows Server
        ├── Active Directory
        ├── DNS
        ├── Group Policy
        ├── File Services
        └── PowerShell
                │
                ↓
          Hybrid Identity
                │
                ↓
          Cloud Services
```

An administrator working with hybrid environments needs to understand both sides.

For example, a synchronization problem may involve:

```text
On-Premises AD
      │
      ↓
Entra Connect
      │
      ↓
Microsoft Entra ID
      │
      ↓
Microsoft 365
```

Without understanding the on-premises side, troubleshooting the complete hybrid environment becomes more difficult.

---

## 25. Summary

On-premises infrastructure is the foundation of traditional enterprise IT.

The key concepts introduced in this section are:

* **On-premises infrastructure** consists of IT systems operated within an organization's controlled environment.
* Physical infrastructure includes servers, networking, storage, power, cooling, and data-center facilities.
* Servers can be physical or virtual.
* Virtualization allows multiple virtual machines to run on physical hardware.
* Network infrastructure connects clients, servers, storage, and external networks.
* Storage can use technologies such as DAS, NAS, and SAN.
* Windows Server provides many enterprise services including Active Directory, DNS, DHCP, file services, and application services.
* Enterprise environments commonly use redundancy and high availability to reduce service disruption.
* Backup protects data and enables recovery after failures.
* Monitoring provides visibility into infrastructure health and security.
* Security must be implemented across physical, network, server, identity, application, and data layers.
* Enterprise infrastructure contains many dependencies between services.
* On-premises infrastructure and cloud infrastructure have different management responsibilities.
* Hybrid cloud environments combine on-premises infrastructure with cloud services.
* Understanding on-premises infrastructure is essential for effectively designing and troubleshooting hybrid environments.

These concepts provide the foundation for the Windows Server and enterprise infrastructure sections that follow.

---
