# Client-Server Architecture

Client-server architecture is a fundamental concept in enterprise IT infrastructure. It describes how computers, applications, and services communicate over a network to provide and consume resources.

In a traditional enterprise environment, users typically work from client devices while centralized servers provide services such as authentication, DNS, DHCP, file storage, applications, databases, and web services.

Understanding the client-server model provides the foundation for learning Windows Server, Active Directory, Group Policy, file services, Microsoft 365, hybrid identity, and cloud infrastructure.

---

## 1. Introduction to Client-Server Architecture

Client-server architecture is a computing model in which a **client requests a service or resource** and a **server provides that service or resource**.

The client and server communicate through a network using defined communication protocols.

```text
┌──────────────┐
│    Client    │
└──────┬───────┘
       │
       │ Request
       ↓
┌──────────────┐
│    Server    │
└──────┬───────┘
       │
       │ Response
       ↓
┌──────────────┐
│    Client    │
└──────────────┘
````

A simple example is accessing a website.

```text
User
 │
 ↓
Web Browser
 │
 │ HTTPS Request
 ↓
Web Server
 │
 │ HTTPS Response
 ↓
Web Browser
 │
 ↓
Web Page
```

The web browser acts as the **client**, while the web server provides the requested content.

---

## 2. Client

A **client** is a device, application, or system that requests services or resources from another system.

A client normally initiates communication with a server.

### 2.1 Client Devices

Common client devices include:

* Desktop computers
* Laptops
* Smartphones
* Tablets
* Thin clients
* Virtual desktops
* Workstations

Example:

```text
┌─────────────────┐
│     CLIENT01    │
│                 │
│ Windows Client  │
│                 │
│ Browser         │
│ Outlook         │
│ Teams           │
│ File Explorer   │
└─────────────────┘
```

### 2.2 Client Applications

Applications can also act as clients.

Examples include:

| Client Application    | Server/Service Accessed |
| --------------------- | ----------------------- |
| Web Browser           | Web Server              |
| Outlook               | Mail Server             |
| File Explorer         | File Server             |
| SQL Client            | Database Server         |
| Remote Desktop Client | Remote Desktop Server   |
| SSH Client            | SSH Server              |
| API Client            | API Server              |

Therefore, the term **client** does not necessarily refer to an entire computer.

An application can independently act as a client.

---

## 3. Server

A **server** is a computer or software service that provides resources or services to clients.

A server waits for requests, processes those requests, and returns appropriate responses.

```text
                    Server
                       │
       ┌───────────────┼───────────────┐
       ↓               ↓               ↓
     DNS             DHCP            File
    Service          Service        Service
       │               │               │
       ↓               ↓               ↓
    Clients         Clients         Clients
```

### 3.1 Physical Server

A physical server is a dedicated hardware system that provides computing resources and services.

```text
┌──────────────────────────────┐
│       Physical Server        │
│                              │
│ CPU                          │
│ Memory                       │
│ Storage                      │
│ Network Interfaces           │
└──────────────────────────────┘
```

### 3.2 Virtual Server

A virtual server is a virtual machine running on physical virtualization infrastructure.

```text
┌──────────────────────────────┐
│       Physical Host          │
│                              │
│      Hypervisor              │
│          │                   │
│    ┌─────┼─────┐             │
│    ↓     ↓     ↓             │
│  VM01   VM02   VM03          │
└──────────────────────────────┘
```

Virtualization allows multiple server workloads to run on the same physical hardware.

### 3.3 Cloud Server

A cloud server is a virtualized computing resource hosted within a cloud provider's infrastructure.

```text
Client
  │
  ↓
Internet / Private Network
  │
  ↓
Cloud Network
  │
  ↓
Virtual Machine
  │
  ↓
Application / Service
```

---

## 4. Client vs Server

The distinction between a client and a server is primarily based on the **role being performed**.

| Characteristic | Client             | Server                          |
| -------------- | ------------------ | ------------------------------- |
| Primary role   | Requests services  | Provides services               |
| Communication  | Initiates requests | Receives and processes requests |
| Resource usage | Consumes resources | Provides resources              |
| Example        | Web Browser        | Web Server                      |
| Example        | File Explorer      | File Server                     |
| Example        | SQL Client         | SQL Server                      |
| Physical       | Yes                | Yes                             |
| Virtual        | Yes                | Yes                             |
| Cloud-based    | Yes                | Yes                             |

A system can act as both a client and a server.

For example:

```text
Computer A
    │
    │ DNS Request
    ↓
Computer B
    │
    └── DNS Server
```

In this communication:

```text
Computer A = Client
Computer B = Server
```

However, Computer B may request another service from another system:

```text
Computer B
    │
    │ Time Request
    ↓
Time Server
```

Now:

```text
Computer B = Client
Time Server = Server
```

Therefore:

> **Client and server describe roles in communication, not necessarily different physical machines.**

---

## 5. Client-Server Communication

Clients and servers communicate through a network.

The basic communication flow is:

```text
Client
  │
  │ Request
  ↓
Network
  │
  ↓
Server
  │
  │ Process Request
  ↓
Server
  │
  │ Response
  ↓
Network
  │
  ↓
Client
```

Successful communication may involve multiple network components.

```text
Client
  │
  ├── IP Address
  ├── DNS
  ├── Routing
  ├── TCP / UDP
  ├── Port
  ├── Firewall
  └── Application Protocol
          │
          ↓
       Server
```

Each component performs a different function.

### 5.1 IP Address

An IP address identifies a device on an IP network.

Example:

```text
SERVER01
192.168.10.10
```

A client can use the server's IP address to establish network communication.

### 5.2 DNS

DNS translates names into IP addresses.

For example:

```text
CLIENT01
    │
    │ "What is the IP of SERVER01?"
    ↓
DNS Server
    │
    │ 192.168.10.10
    ↓
CLIENT01
```

Instead of remembering:

```text
192.168.10.10
```

users and applications can use:

```text
SERVER01
```

### 5.3 Protocol

A protocol defines how systems communicate.

Examples include:

* HTTP
* HTTPS
* DNS
* SMB
* LDAP
* Kerberos
* SSH
* RDP

### 5.4 Port

A port identifies a particular service or application endpoint on a system.

For example:

```text
Client
  │
  │ TCP
  │ Port 443
  ↓
Web Server
```

### 5.5 Firewall

A firewall controls whether network traffic is allowed or blocked.

```text
Client
  │
  │ Network Traffic
  ↓
┌─────────────┐
│  Firewall   │
└──────┬──────┘
       │
       ↓
    Server
```

A firewall may allow:

```text
TCP 443 → Allowed
```

while blocking:

```text
TCP 445 → Blocked
```

depending on the organization's security requirements.

---

## 6. Request and Response Model

The request-response model is one of the most common patterns in client-server communication.

The general process is:

```text
1. Client creates request
          ↓
2. Request travels through network
          ↓
3. Server receives request
          ↓
4. Server processes request
          ↓
5. Server creates response
          ↓
6. Response travels back
          ↓
7. Client receives response
```

### 6.1 Web Request

```text
Browser
   │
   │ HTTPS Request
   ↓
Web Server
   │
   │ Process Request
   ↓
Web Server
   │
   │ HTTPS Response
   ↓
Browser
```

### 6.2 File Request

```text
CLIENT01
   │
   │ "I need Report.xlsx"
   ↓
FILE01
   │
   ├── Locate file
   ├── Authenticate user
   ├── Check permissions
   └── Return file
   │
   ↓
CLIENT01
```

### 6.3 DNS Request

```text
CLIENT01
   │
   │ DNS Query
   ↓
DNS Server
   │
   │ DNS Response
   ↓
CLIENT01
```

---

## 7. Common Enterprise Server Types

Enterprise environments commonly use specialized servers for different workloads.

### 7.1 Web Server

A web server hosts websites and web applications.

Examples:

* Microsoft IIS
* Apache
* NGINX

```text
Browser
   │
   │ HTTP / HTTPS
   ↓
Web Server
   │
   ↓
Web Application
```

---

### 7.2 File Server

A file server provides centralized file storage and sharing.

```text
CLIENT01
    │
    │ SMB
    ↓
FILE01
    │
    ├── Finance
    ├── HR
    ├── Projects
    └── Documents
```

Windows environments commonly use **SMB (Server Message Block)** for network file sharing.

---

### 7.3 DNS Server

A DNS server provides name resolution.

```text
CLIENT01
    │
    │ DNS Query
    ↓
DNS Server
    │
    │ IP Address
    ↓
CLIENT01
```

DNS is especially important for Windows enterprise environments and Active Directory.

---

### 7.4 DHCP Server

A DHCP server automatically provides network configuration to clients.

DHCP can provide:

* IP address
* Subnet mask
* Default gateway
* DNS server
* DNS domain

```text
CLIENT01
    │
    │ DHCP Request
    ↓
DHCP Server
    │
    │ IP Configuration
    ↓
CLIENT01
```

---

### 7.5 Authentication Server

An authentication service verifies the identity of a user or system.

In a Windows enterprise environment, **Active Directory Domain Services (AD DS)** provides centralized identity and authentication capabilities.

```text
User
 │
 │ Credentials
 ↓
CLIENT01
 │
 │ Authentication Request
 ↓
Domain Controller
 │
 │ Authentication Result
 ↓
CLIENT01
```

---

### 7.6 Database Server

A database server stores and manages structured application data.

Examples include:

* Microsoft SQL Server
* PostgreSQL
* MySQL
* Oracle Database

```text
Application Server
       │
       │ Database Query
       ↓
Database Server
       │
       │ Query Result
       ↓
Application Server
```

---

### 7.7 Application Server

An application server hosts business applications and application services.

```text
Client
   │
   ↓
Application Server
   │
   ↓
Database Server
```

---

### 7.8 Email Server

An email server provides messaging services.

Traditional environments may use:

```text
Exchange Server
```

Cloud environments may use:

```text
Exchange Online
```

---

## 8. Server Roles and Services

A server can provide one or multiple services.

For example, a small environment may use a single server:

```text
┌──────────────────────────────┐
│        Windows Server        │
│                              │
│  ├── DNS                     │
│  ├── DHCP                    │
│  ├── File Services           │
│  └── Application Services    │
│                              │
└──────────────────────────────┘
```

This can be appropriate for:

* Small organizations
* Development environments
* Test environments
* Learning environments

Larger organizations generally separate workloads.

```text
┌──────────────┐
│     DC01     │
│ AD DS + DNS  │
└──────────────┘

┌──────────────┐
│    DHCP01    │
│     DHCP     │
└──────────────┘

┌──────────────┐
│    FILE01    │
│ File Server  │
└──────────────┘

┌──────────────┐
│     WEB01    │
│ Web Server   │
└──────────────┘
```

Workload separation can improve:

* Security
* Performance
* Availability
* Scalability
* Maintenance
* Troubleshooting

---

## 9. Centralized Architecture

In a centralized architecture, multiple services are concentrated on a smaller number of systems.

```text
                ┌──────────────┐
                │    SERVER    │
                │              │
                │ DNS          │
                │ DHCP         │
                │ Files        │
                │ Applications │
                └───────┬──────┘
                        │
            ┌───────────┼───────────┐
            ↓           ↓           ↓
        CLIENT01    CLIENT02    CLIENT03
```

### 9.1 Advantages

* Simple management
* Lower infrastructure requirements
* Easier initial deployment
* Suitable for small environments

### 9.2 Disadvantages

* Single point of failure
* Resource contention
* Limited scalability
* Larger impact if the server fails

---

## 10. Distributed Architecture

In a distributed architecture, workloads are distributed across multiple servers.

```text
                    ┌────────────┐
                    │    DC01    │
                    │ AD + DNS   │
                    └─────┬──────┘
                          │
          ┌───────────────┼───────────────┐
          ↓               ↓               ↓
    ┌──────────┐    ┌──────────┐    ┌──────────┐
    │  DHCP01  │    │  FILE01  │    │   WEB01  │
    │   DHCP   │    │   SMB    │    │   IIS    │
    └──────────┘    └──────────┘    └──────────┘
          │               │               │
          └───────────────┼───────────────┘
                          ↓
                       Clients
```

Distributed architectures are commonly used in enterprise environments.

### 10.1 Advantages

* Workload separation
* Improved scalability
* Easier maintenance
* Independent resource allocation
* Better security boundaries
* Reduced impact of individual failures

---

## 11. Authentication and Authorization

Client-server environments commonly involve authentication and authorization.

### 11.1 Authentication

Authentication answers:

> **Who are you?**

Examples include:

* Username and password
* Certificates
* Biometrics
* Multi-factor authentication
* Security tokens

Example:

```text
User
 │
 │ Credentials
 ↓
Authentication Service
 │
 │ Identity Verified
 ↓
Client
```

### 11.2 Authorization

Authorization answers:

> **What are you allowed to access?**

For example:

```text
User
 │
 │ Authentication
 ↓
Identity System
 │
 │ User Identified
 ↓
Authorization
 │
 ├── Finance Share → ❌
 ├── HR Share → ❌
 └── Public Share → ✅
```

This distinction becomes important when learning:

* Active Directory
* Group Policy
* Microsoft Entra ID
* RBAC
* Microsoft 365
* Zero Trust

---

## 12. Common Protocols and Ports

Client-server services use protocols and ports to communicate.

| Service  | Protocol | Common Port |
| -------- | -------- | ----------: |
| HTTP     | TCP      |          80 |
| HTTPS    | TCP      |         443 |
| DNS      | TCP/UDP  |          53 |
| DHCP     | UDP      |       67/68 |
| SSH      | TCP      |          22 |
| RDP      | TCP/UDP  |        3389 |
| SMB      | TCP      |         445 |
| LDAP     | TCP/UDP  |         389 |
| LDAPS    | TCP      |         636 |
| Kerberos | TCP/UDP  |          88 |

For example:

```text
Client
 │
 │ TCP
 │ Port 443
 ↓
Web Server
```

The port allows the operating system and networking stack to identify the intended service.

---

## 13. Centralized Services in Enterprise Environments

One of the major benefits of client-server architecture is centralized service management.

Instead of every client independently maintaining its own resources, services can be centralized.

For example:

```text
                Enterprise Network
                       │
        ┌──────────────┼──────────────┐
        ↓              ↓              ↓
      CLIENT01      CLIENT02      CLIENT03
        │              │              │
        └──────────────┼──────────────┘
                       │
                       ↓
                    Servers
                       │
        ┌──────────────┼──────────────┐
        ↓              ↓              ↓
       DNS            Files       Authentication
```

Centralization allows organizations to manage:

* User identities
* File access
* Network configuration
* Applications
* Security policies
* Authentication
* Logging
* Backup

from centralized infrastructure.

---

## 14. Client-Server Architecture in On-Premises Infrastructure

In a traditional on-premises environment, the organization operates its own infrastructure.

A simplified architecture may look like:

```text
                    Data Center
                         │
        ┌────────────────┼────────────────┐
        ↓                ↓                ↓
     DC01             FILE01            WEB01
        │                │                │
     AD + DNS         SMB Files       Applications
        │                │                │
        └────────────────┼────────────────┘
                         │
                      Clients
```

The organization may be responsible for:

* Physical servers
* Virtual machines
* Storage
* Network infrastructure
* Operating systems
* Applications
* Security
* Backup
* Monitoring
* Maintenance

---

## 15. Client-Server Architecture in Cloud Computing

The client-server model also exists in cloud computing.

The major difference is where the infrastructure is hosted and who manages the underlying infrastructure.

```text
Client
   │
   ↓
Internet / Private Network
   │
   ↓
Cloud Infrastructure
   │
   ├── Compute
   ├── Storage
   ├── Networking
   └── Applications
```

For example:

```text
User
 │
 ↓
Web Browser
 │
 ↓
Cloud Application
 │
 ↓
Cloud Database
```

The physical infrastructure may be operated by the cloud provider.

---

## 16. Client-Server Architecture in Hybrid Environments

Hybrid environments combine on-premises infrastructure with cloud services.

```text
                 ON-PREMISES
        ┌─────────────────────────┐
        │                         │
        │ Active Directory        │
        │ DNS                     │
        │ Windows Servers         │
        │ File Servers            │
        │ Applications            │
        │                         │
        └────────────┬────────────┘
                     │
                     │ Hybrid Connectivity
                     ↓
                 CLOUD SERVICES
        ┌─────────────────────────┐
        │                         │
        │ Microsoft 365           │
        │ Intune                  │
        │ Defender                │
        │ Cloud Applications      │
        │                         │
        └─────────────────────────┘
```

This architecture allows organizations to continue using existing on-premises systems while gradually adopting cloud services.

The overall evolution may look like:

```text
On-Premises Infrastructure
          ↓
Windows Server
          ↓
Active Directory
          ↓
Enterprise Services
          ↓
Hybrid Identity
          ↓
Microsoft 365
          ↓
Modern Endpoint Management
          ↓
Cloud Security
```

---

## 17. Three-Tier Application Architecture

Many enterprise applications use multiple layers rather than allowing clients to communicate directly with databases.

A common model is the **three-tier architecture**.

```text
┌─────────────────────────┐
│   Presentation Layer    │
│                         │
│ Browser / Client        │
└────────────┬────────────┘
             │
             ↓
┌─────────────────────────┐
│   Application Layer     │
│                         │
│ Business Logic / API    │
└────────────┬────────────┘
             │
             ↓
┌─────────────────────────┐
│       Data Layer        │
│                         │
│ Database                │
└─────────────────────────┘
```

### 17.1 Presentation Layer

The presentation layer interacts with the user.

Examples:

* Web browser
* Desktop application
* Mobile application

### 17.2 Application Layer

The application layer processes business logic.

Examples:

* Web application
* API
* Application server

### 17.3 Data Layer

The data layer stores and retrieves application data.

Examples:

* SQL Server
* PostgreSQL
* MySQL

Separating these layers can improve:

* Security
* Scalability
* Maintainability
* Performance
* Application management

---

## 18. Enterprise Example

Consider an organization with several departments and hundreds of employees.

A simplified infrastructure might look like:

```text
                         Corporate Network
                                │
          ┌─────────────────────┼─────────────────────┐
          │                     │                     │
          ↓                     ↓                     ↓
       DC01                  FILE01                 WEB01
          │                     │                     │
     AD DS + DNS            SMB Shares          Application
          │                     │                     │
          └─────────────────────┼─────────────────────┘
                                │
                  ┌─────────────┴─────────────┐
                  ↓                           ↓
              CLIENT01                    CLIENT02
```

### 18.1 User Authentication

```text
Employee
   │
   ↓
CLIENT01
   │
   │ Authentication Request
   ↓
DC01
   │
   │ Authentication Result
   ↓
CLIENT01
```

### 18.2 File Access

```text
Employee
   │
   ↓
CLIENT01
   │
   │ SMB
   ↓
FILE01
   │
   ↓
Company Files
```

### 18.3 Application Access

```text
Employee
   │
   ↓
CLIENT01
   │
   │ HTTPS
   ↓
WEB01
   │
   ↓
Business Application
```

Multiple services work together to provide the complete enterprise environment.

---

## 19. Key Enterprise Concepts

The client-server model introduces several concepts that will appear throughout this learning path.

| Concept           | Purpose                                   |
| ----------------- | ----------------------------------------- |
| Client            | Requests a service                        |
| Server            | Provides a service                        |
| IP Address        | Identifies a system                       |
| DNS               | Resolves names                            |
| DHCP              | Provides network configuration            |
| Protocol          | Defines communication rules               |
| Port              | Identifies a service endpoint             |
| Firewall          | Controls network traffic                  |
| Authentication    | Verifies identity                         |
| Authorization     | Controls resource access                  |
| Application       | Provides business functionality           |
| Database          | Stores application data                   |
| File Server       | Provides centralized file storage         |
| Directory Service | Provides centralized identity information |

---

## 20. Importance in Microsoft Enterprise Environments

Client-server architecture provides the foundation for many Microsoft technologies.

A traditional Microsoft enterprise environment may contain:

```text
                    Enterprise
                         │
        ┌────────────────┼────────────────┐
        ↓                ↓                ↓
    Windows Server    Active Directory   Network
        │                │                │
        ├── DNS          ├── Users        ├── TCP/IP
        ├── DHCP         ├── Groups       ├── Routing
        ├── Files        ├── Computers    ├── Firewall
        └── Apps         └── Policies     └── Connectivity
```

These technologies later connect to cloud services:

```text
On-Premises
     │
     ├── Windows Server
     ├── Active Directory
     ├── DNS
     ├── DHCP
     ├── File Services
     └── Group Policy
            │
            ↓
       Hybrid Identity
            │
            ↓
       Microsoft Cloud
            │
     ┌──────┼──────┐
     ↓      ↓      ↓
 Microsoft Intune
 365      Defender
          Purview
```

Understanding the basic client-server relationship makes it easier to understand why these services exist and how they interact.

---

## 21. Summary

Client-server architecture describes how systems communicate to provide and consume services.

The key concepts introduced in this section are:

* **Clients request services or resources.**
* **Servers provide services or resources.**
* Client and server are **roles**, not necessarily different physical computers.
* Clients and servers communicate through networks.
* Communication can involve **IP addresses, DNS, routing, TCP/UDP, ports, firewalls, and application protocols**.
* Enterprise environments use different server types for different workloads.
* Common server roles include **DNS, DHCP, file, web, database, application, email, and authentication services**.
* Small environments may use centralized services.
* Enterprise environments commonly distribute workloads across multiple servers.
* **Authentication** determines who a user or system is.
* **Authorization** determines what a user or system is allowed to access.
* Client-server architecture exists in **on-premises, cloud, and hybrid environments**.
* Multi-tier architectures separate application responsibilities into different layers.
* Client-server architecture provides the foundation for understanding enterprise Microsoft infrastructure.

---

