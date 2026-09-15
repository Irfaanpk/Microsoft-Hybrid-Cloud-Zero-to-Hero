# Virtualization Fundamentals

Virtualization is a core technology used in modern enterprise IT infrastructure. It allows a physical computing system to provide multiple isolated virtual computing environments called **virtual machines (VMs)**.

Instead of dedicating one physical server to every workload, organizations can use virtualization to run multiple servers on shared physical infrastructure.

Virtualization is fundamental to understanding modern data centers, Windows Server, Hyper-V, cloud computing, disaster recovery, high availability, and hybrid cloud environments.

---

## 1. Introduction to Virtualization

Virtualization is the process of creating a virtual representation of a computing resource.

A virtual machine can have its own:

- CPU resources
- Memory
- Virtual disk
- Network interface
- Operating system
- Applications
- Configuration

From the operating system's perspective, the virtual machine behaves like an independent computer.

A simplified architecture looks like:

```text
┌──────────────────────────────┐
│       Physical Server        │
│                              │
│       CPU / RAM / Storage    │
│                              │
├──────────────────────────────┤
│          Hypervisor          │
├──────────┬─────────┬─────────┤
│   VM01   │  VM02   │  VM03   │
│          │         │         │
│  DC01    │ FILE01  │ WEB01   │
└──────────┴─────────┴─────────┘
````

Each virtual machine can run a different workload while sharing the underlying physical hardware.

---

## 2. Why Virtualization is Important

Before virtualization became widely used, organizations often deployed applications using dedicated physical servers.

For example:

```text
Application 1
     ↓
Physical Server 1

Application 2
     ↓
Physical Server 2

Application 3
     ↓
Physical Server 3
```

This could result in:

* Low hardware utilization
* Higher hardware costs
* Increased power consumption
* More physical space requirements
* More hardware to maintain

Virtualization changes this model:

```text
                  Physical Server
                        │
                    Hypervisor
                        │
          ┌─────────────┼─────────────┐
          ↓             ↓             ↓
        VM01          VM02          VM03
        App 1         App 2         App 3
```

Multiple workloads can therefore share the same physical infrastructure.

---

## 3. Physical Machine vs Virtual Machine

A physical machine runs directly on hardware.

```text
┌──────────────────────────┐
│     Physical Server      │
├──────────────────────────┤
│     Operating System     │
├──────────────────────────┤
│       Application        │
└──────────────────────────┘
```

A virtual machine runs on virtualized hardware provided by a hypervisor.

```text
┌──────────────────────────┐
│     Physical Server      │
├──────────────────────────┤
│       Hypervisor         │
├──────────────────────────┤
│       Virtual Machine    │
├──────────────────────────┤
│     Guest Operating OS   │
├──────────────────────────┤
│       Application        │
└──────────────────────────┘
```

The guest operating system generally does not need to know that it is running on virtualized hardware.

---

## 4. Virtual Machine

A **virtual machine** is an isolated software-defined computer that runs on a physical host through a hypervisor.

A VM normally contains:

* Virtual CPU
* Virtual memory
* Virtual disk
* Virtual network adapter
* Virtual hardware devices
* Guest operating system
* Applications

Example:

```text
┌─────────────────────────────┐
│            VM01             │
│                             │
│   Windows Server            │
│                             │
│   vCPU: 4                   │
│   RAM: 8 GB                 │
│   Disk: 100 GB              │
│   vNIC: Connected           │
│                             │
└─────────────────────────────┘
```

Another VM on the same host can have completely different resources:

```text
┌─────────────────────────────┐
│            VM02             │
│                             │
│   Windows Server            │
│                             │
│   vCPU: 2                   │
│   RAM: 4 GB                 │
│   Disk: 60 GB               │
│                             │
└─────────────────────────────┘
```

Both VMs can run independently while sharing the physical host.

---

## 5. Hypervisor

A **hypervisor** is the software layer responsible for creating and managing virtual machines.

The hypervisor manages access to physical resources such as:

* CPU
* Memory
* Storage
* Network interfaces

```text
┌──────────────────────────────┐
│       Physical Hardware      │
│                              │
│ CPU / RAM / Storage / NIC    │
├──────────────────────────────┤
│          Hypervisor          │
├────────────┬─────────┬───────┤
│    VM01    │  VM02   │ VM03  │
└────────────┴─────────┴───────┘
```

The hypervisor provides isolation between virtual machines while controlling how physical resources are allocated.

---

## 6. Types of Hypervisors

Hypervisors are commonly divided into two categories:

* Type 1
* Type 2

---

## 7. Type 1 Hypervisor

A Type 1 hypervisor runs directly on physical hardware.

It is also commonly called a **bare-metal hypervisor**.

```text
┌──────────────────────────┐
│     Physical Hardware    │
├──────────────────────────┤
│     Type 1 Hypervisor    │
├────────┬────────┬────────┤
│  VM01  │  VM02  │  VM03  │
└────────┴────────┴────────┘
```

Examples include:

* Microsoft Hyper-V
* VMware ESXi

Type 1 hypervisors are commonly used in enterprise data centers.

### 7.1 Characteristics

* Runs directly on hardware
* Designed for server virtualization
* High performance
* Strong isolation
* Suitable for enterprise environments
* Supports centralized management

---

## 8. Type 2 Hypervisor

A Type 2 hypervisor runs on top of a host operating system.

```text
┌──────────────────────────┐
│     Physical Hardware    │
├──────────────────────────┤
│       Host Operating OS  │
├──────────────────────────┤
│     Type 2 Hypervisor    │
├────────┬────────┬────────┤
│  VM01  │  VM02  │  VM03  │
└────────┴────────┴────────┘
```

Examples include desktop virtualization platforms such as:

* Oracle VirtualBox
* VMware Workstation

Type 2 virtualization is commonly used for:

* Development
* Testing
* Training
* Desktop laboratories

---

## 9. Type 1 vs Type 2 Hypervisors

| Feature             | Type 1              | Type 2                |
| ------------------- | ------------------- | --------------------- |
| Runs on             | Physical hardware   | Host operating system |
| Common use          | Enterprise servers  | Desktop/testing       |
| Performance         | Generally higher    | Generally lower       |
| Management          | Enterprise-oriented | Desktop-oriented      |
| Example             | Hyper-V             | VirtualBox            |
| Example             | VMware ESXi         | VMware Workstation    |
| Hardware dependency | Direct              | Through host OS       |

The choice depends on the environment and requirements.

---

## 10. Host and Guest

Virtualization introduces two important terms:

### Host

The **host** is the physical system that provides the hardware resources.

```text
Physical Host
     │
     └── Hypervisor
```

### Guest

The **guest** is the virtual machine running on the host.

```text
Physical Host
     │
     └── Hypervisor
            │
            ├── Guest VM01
            ├── Guest VM02
            └── Guest VM03
```

For example:

```text
Host:
Physical Server

Guest:
Windows Server VM
```

---

## 11. Virtual CPU

A virtual machine receives virtual CPUs, commonly called **vCPUs**.

```text
Physical CPU
     │
     ├── vCPU → VM01
     ├── vCPU → VM02
     └── vCPU → VM03
```

The hypervisor schedules virtual CPU workloads onto physical CPU resources.

For example:

```text
Physical Server
     │
     │ 16 Physical CPU Cores
     │
     ├── VM01 → 4 vCPU
     ├── VM02 → 4 vCPU
     ├── VM03 → 2 vCPU
     └── VM04 → 2 vCPU
```

The number of vCPUs assigned to a VM should be based on workload requirements.

More vCPUs do not automatically mean better performance.

---

## 12. Virtual Memory

Virtual machines are also assigned virtual memory.

For example:

```text
Physical Host
     │
     │ 64 GB RAM
     │
     ├── VM01 → 16 GB
     ├── VM02 → 16 GB
     ├── VM03 → 8 GB
     └── VM04 → 8 GB
```

Memory allocation must be carefully planned.

Over-allocating memory can result in resource contention and degraded performance.

---

## 13. Virtual Storage

Virtual machines typically use virtual disks rather than directly accessing physical disks.

```text
VM01
 │
 │ Virtual Disk
 ↓
VHDX / Virtual Disk File
 │
 ↓
Physical Storage
```

A virtual disk can contain:

* Operating system
* Applications
* Configuration
* Data

In Microsoft Hyper-V environments, **VHDX** is commonly used for virtual hard disks.

---

## 14. Virtual Networking

Virtual machines need network connectivity just like physical computers.

A hypervisor provides virtual networking components.

```text
┌─────────────┐
│     VM01    │
└──────┬──────┘
       │
   Virtual NIC
       │
       ↓
Virtual Switch
       │
       ↓
Physical NIC
       │
       ↓
Physical Network
```

This allows VMs to communicate with:

* Other VMs
* Physical computers
* Servers
* The internet
* Other networks

---

## 15. Virtual Network Adapter

A VM normally has a virtual network interface card.

```text
VM01
 │
 └── vNIC
       │
       ↓
 Virtual Switch
       │
       ↓
 Physical NIC
```

The virtual NIC behaves similarly to a physical network adapter from the guest operating system's perspective.

The guest operating system can configure:

* IP address
* Subnet mask
* Default gateway
* DNS servers

just like a physical machine.

---

## 16. Virtual Switch

A virtual switch connects virtual machines to each other and, depending on configuration, to physical networks.

A simplified architecture:

```text
                 Virtual Switch
                 /      |      \
                /       |       \
              VM01     VM02     VM03
                |
                ↓
          Physical Network
```

In Hyper-V environments, virtual switches can provide different types of connectivity.

Common concepts include:

* External
* Internal
* Private

These concepts will be explored in detail in the Hyper-V section.

---

## 17. VM Isolation

Virtual machines are logically isolated from one another.

For example:

```text
┌───────────────┐
│     VM01      │
│   DC01        │
└───────────────┘

┌───────────────┐
│     VM02      │
│   FILE01      │
└───────────────┘

┌───────────────┐
│     VM03      │
│   WEB01       │
└───────────────┘
```

A problem inside one VM does not normally directly modify the operating system of another VM.

However, virtualization is not an automatic security boundary for every threat.

Organizations still need:

* Network security
* Operating system security
* Access controls
* Patch management
* Monitoring
* Endpoint protection

---

## 18. Resource Allocation

The hypervisor allocates physical resources to virtual machines.

Resources include:

```text
Physical Resources
        │
        ├── CPU
        ├── Memory
        ├── Storage
        └── Network
                │
                ↓
           Hypervisor
                │
        ┌───────┼───────┐
        ↓       ↓       ↓
      VM01    VM02    VM03
```

Administrators must consider:

* CPU requirements
* Memory requirements
* Storage requirements
* Network requirements
* Workload characteristics
* Future growth

Poor resource allocation can result in performance problems.

---

## 19. Overcommitment

Virtualization platforms can sometimes allocate more virtual resources than the physical host has available at one time.

For example:

```text
Physical CPU:
16 cores

Allocated vCPU:
VM01 → 8
VM02 → 8
VM03 → 8
VM04 → 8

Total:
32 vCPU
```

This does not necessarily mean all VMs can continuously consume 32 physical cores.

The hypervisor schedules workloads based on demand.

Overcommitment can improve hardware utilization when workloads have varying usage patterns.

However, excessive overcommitment can cause:

* CPU contention
* Memory pressure
* Poor performance
* Unpredictable application behavior

Resource planning is therefore important.

---

## 20. Virtual Machine Lifecycle

A VM follows a lifecycle similar to a physical server.

```text
Create
  ↓
Configure
  ↓
Install OS
  ↓
Configure Network
  ↓
Install Applications
  ↓
Operate
  ↓
Monitor
  ↓
Backup
  ↓
Maintain
  ↓
Update
  ↓
Retire
```

Administrators may also need to:

* Resize resources
* Add disks
* Modify networking
* Change configuration
* Move workloads
* Restore backups
* Clone systems

---

## 21. VM Snapshots and Checkpoints

Virtualization platforms can provide mechanisms for capturing the state of a virtual machine.

In Hyper-V, this is called a **checkpoint**.

Conceptually:

```text
VM01
 │
 │ Running
 ↓
Checkpoint
 │
 ↓
Saved VM State
```

Checkpoints can be useful for:

* Testing
* Development
* Configuration changes
* Short-term rollback

However, checkpoints should **not be treated as a replacement for backups**.

For production systems, administrators must understand the difference between:

```text
Checkpoint
    ≠
Backup
```

A backup is designed for data and system recovery, while checkpoints are primarily useful for managing VM state during certain operational scenarios.

---

## 22. Virtualization and High Availability

Virtualization can support high-availability architectures.

For example:

```text
             Virtualization Cluster
                     │
          ┌──────────┴──────────┐
          ↓                     ↓
       Host01                Host02
          │                     │
      ┌───┴───┐             ┌───┴───┐
      ↓       ↓             ↓       ↓
    VM01    VM02          VM03    VM04
```

If the architecture is properly designed, workloads may be moved or restarted on another host when a host fails.

High availability requires more than virtualization alone.

It may require:

* Multiple hosts
* Shared or resilient storage
* Redundant networking
* Cluster management
* Monitoring
* Proper application design

---

## 23. Virtualization and Disaster Recovery

Virtual machines can simplify disaster recovery.

A simplified design:

```text
Primary Site
     │
     │ Replication / Backup
     ↓
Secondary Site
     │
     ↓
Recovery Environment
```

Virtual machines can be:

* Backed up
* Replicated
* Restored
* Migrated
* Recreated from templates

This can reduce the time required to recover workloads.

---

## 24. Virtualization and Server Consolidation

Server consolidation is one of the major benefits of virtualization.

Without virtualization:

```text
Server01 → Application A
Server02 → Application B
Server03 → Application C
Server04 → Application D
```

With virtualization:

```text
             Physical Host
                  │
              Hypervisor
                  │
      ┌───────────┼───────────┐
      ↓           ↓           ↓
    VM01        VM02        VM03
    App A       App B       App C
```

Multiple workloads can share the same physical infrastructure.

This can reduce:

* Hardware requirements
* Data-center space
* Power consumption
* Cooling requirements
* Hardware maintenance

---

## 25. Virtualization and Testing

Virtualization is particularly useful for development and testing.

An administrator can create isolated environments:

```text
┌─────────────────────────────┐
│       Test Environment      │
│                             │
│  DC01                       │
│  CLIENT01                   │
│  FILE01                     │
│  WEB01                      │
│                             │
└─────────────────────────────┘
```

Changes can be tested without affecting production systems.

This is one reason virtualization is extremely useful for learning Windows Server and Active Directory.

---

## 26. Virtualization in Enterprise Infrastructure

A typical enterprise virtualization environment may look like:

```text
                         Data Center
                              │
              ┌───────────────┼───────────────┐
              ↓               ↓               ↓
           Host01          Host02          Host03
              │               │               │
          ┌───┴───┐       ┌───┴───┐       ┌───┴───┐
          ↓       ↓       ↓       ↓       ↓       ↓
        DC01    FILE01   WEB01   SQL01   APP01   APP02
              \             |             /
               \            |            /
                └────── Storage ─────────┘
                         │
                         ↓
                    Backup System
```

Enterprise virtualization infrastructure normally includes:

* Physical hosts
* Hypervisors
* Virtual machines
* Virtual networking
* Storage
* Backup
* Monitoring
* Management
* Security

---

## 27. Virtualization Management

Virtualized environments require centralized management.

Administrators may need to manage:

* Virtual machines
* Hosts
* Virtual switches
* Virtual disks
* CPU allocation
* Memory allocation
* VM networking
* Checkpoints
* Templates
* Backup
* Monitoring

Management tools depend on the virtualization platform.

For Microsoft environments, **Hyper-V** is an important virtualization technology.

---

## 28. Virtualization Security

Virtualization introduces additional security considerations.

Security must be applied to:

```text
Physical Hardware
       ↓
Hypervisor
       ↓
Virtual Machines
       ↓
Guest Operating Systems
       ↓
Applications
       ↓
Data
```

Important controls include:

* Hypervisor security
* Administrative access control
* VM isolation
* Network segmentation
* Secure management
* Patch management
* Endpoint protection
* Encryption
* Monitoring
* Backup protection

Compromising virtualization management infrastructure can have a significant impact because multiple workloads may depend on the same platform.

---

## 29. Virtualization vs Cloud Computing

Virtualization and cloud computing are related but they are not the same thing.

### Virtualization

Virtualization is a technology for abstracting physical resources and creating virtual computing environments.

### Cloud Computing

Cloud computing is an operational and service-delivery model that provides computing resources over a network with characteristics such as on-demand access and scalable resource consumption.

A cloud platform may use virtualization internally, but cloud computing includes much more than virtualization.

```text
Virtualization
     │
     ├── Virtual Machines
     ├── Virtual Networks
     └── Virtual Storage

Cloud Computing
     │
     ├── Compute
     ├── Storage
     ├── Networking
     ├── Identity
     ├── Managed Services
     ├── Automation
     └── Consumption Model
```

---

## 30. Virtualization and Hybrid Cloud

Virtualization is important in hybrid environments because many organizations continue to run virtualized workloads on-premises while consuming cloud services.

A simplified architecture:

```text
              ON-PREMISES
        ┌─────────────────────┐
        │                     │
        │ Physical Hosts      │
        │       │             │
        │   Hypervisor        │
        │       │             │
        │   Virtual Machines  │
        │                     │
        └──────────┬──────────┘
                   │
                   │ Hybrid Connectivity
                   ↓
                 CLOUD
        ┌─────────────────────┐
        │                     │
        │ Cloud Compute       │
        │ Cloud Storage       │
        │ Cloud Services      │
        │ Microsoft 365       │
        │ Security Services   │
        │                     │
        └─────────────────────┘
```

This allows organizations to modernize gradually.

---

## 31. Virtualization Technologies

Several virtualization technologies are widely used.

| Technology         | Vendor / Ecosystem | Common Use                            |
| ------------------ | ------------------ | ------------------------------------- |
| Hyper-V            | Microsoft          | Windows and enterprise virtualization |
| VMware ESXi        | Broadcom / VMware  | Enterprise virtualization             |
| VirtualBox         | Oracle             | Desktop virtualization                |
| VMware Workstation | Broadcom / VMware  | Desktop development and testing       |
| KVM                | Linux ecosystem    | Linux and cloud virtualization        |

The choice depends on:

* Organization requirements
* Operating systems
* Existing infrastructure
* Management requirements
* Licensing
* Performance
* Availability
* Budget

---

## 32. Important Virtualization Terminology

| Term           | Meaning                                               |
| -------------- | ----------------------------------------------------- |
| Hypervisor     | Software layer that manages VMs                       |
| Host           | Physical system running the hypervisor                |
| Guest          | Virtual machine running on the host                   |
| VM             | Virtualized computer                                  |
| vCPU           | Virtual CPU assigned to a VM                          |
| vRAM           | Virtual memory assigned to a VM                       |
| vNIC           | Virtual network interface                             |
| Virtual Switch | Provides virtual network connectivity                 |
| Virtual Disk   | Disk presented to a VM                                |
| VHDX           | Hyper-V virtual hard disk format                      |
| Checkpoint     | Captured VM state used for certain rollback scenarios |
| Cluster        | Multiple hosts working together                       |
| Template       | Reusable VM configuration/image                       |
| Migration      | Moving a VM or workload between hosts                 |

---

## 33. Virtualization Architecture

A complete enterprise virtualization architecture can be represented as:

```text
                         Data Center
                              │
                    ┌─────────┴─────────┐
                    ↓                   ↓
                 Host01              Host02
                    │                   │
                Hypervisor          Hypervisor
                    │                   │
             ┌──────┼──────┐     ┌──────┼──────┐
             ↓      ↓      ↓     ↓      ↓      ↓
           DC01   FILE01  WEB01  SQL01  APP01  APP02
             │      │      │      │      │      │
             └──────┴──────┴──────┴──────┴──────┘
                            │
                         Network
                            │
                         Storage
                            │
                         Backup
```

This architecture demonstrates how compute, networking, storage, and management come together.

---

## 34. Virtualization in the Learning Environment

Virtualization will be particularly important for the practical sections of this repository.

The later labs will use virtual machines to build an enterprise-style Microsoft environment.

The environment will progressively evolve:

```text
Virtualization
      ↓
Windows Server
      ↓
DC01
      ↓
DNS / DHCP
      ↓
Active Directory
      ↓
CLIENT01
      ↓
Group Policy
      ↓
FILE01
      ↓
PowerShell
      ↓
Additional Servers
      ↓
Hybrid Identity
```

The actual VM creation and Hyper-V configuration will be covered in the **Hyper-V and Virtualization** section rather than in this fundamentals chapter.

---

## 35. Summary

Virtualization is a foundational technology in modern enterprise infrastructure.

The key concepts introduced in this section are:

* **Virtualization** creates virtual representations of computing resources.
* A **virtual machine** behaves like an independent computer.
* A **hypervisor** manages virtual machines and allocates physical resources.
* **Type 1 hypervisors** run directly on physical hardware.
* **Type 2 hypervisors** run on top of a host operating system.
* The physical system is called the **host**.
* A virtual machine is called the **guest**.
* VMs can have virtual CPUs, memory, storage, and network interfaces.
* Virtual switches provide networking between virtual machines and physical networks.
* Virtualization provides workload isolation and better hardware utilization.
* Resource allocation must be planned carefully to avoid contention.
* Overcommitment can improve utilization but can also cause performance problems when excessive.
* Checkpoints can capture VM state but should not be treated as a replacement for backups.
* Virtualization can support server consolidation, testing, high availability, and disaster recovery.
* Virtualization is a technology, while cloud computing is a broader service-delivery model.
* Modern enterprises commonly combine virtualization with cloud services.
* Virtualization provides the foundation for the practical Windows Server and Hyper-V labs later in this repository.
---

