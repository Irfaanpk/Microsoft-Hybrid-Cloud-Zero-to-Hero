Client-Server Architecture

Client-server architecture is one of the fundamental concepts of enterprise IT infrastructure. It explains how computers, applications, and services communicate with each other to provide resources and business functionality.

Understanding the client-server model is essential before moving into Windows Server, Active Directory, DNS, DHCP, file services, Microsoft 365, and hybrid cloud environments.

---

## 📖 What is Client-Server Architecture?

Client-server architecture is a computing model where one system requests a service or resource, while another system provides that service or resource.

The system requesting the service is called the **client**, and the system providing the service is called the **server**.

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

A simple real-world example is opening a website.

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

The web browser acts as the **client**, while the web server provides the requested website.

---

## 💻 What is a Client?

A client is a device or application that requests services or resources from another system.

### Examples of Client Devices

* Desktop computers
* Laptops
* Smartphones
* Tablets
* Thin clients
* Virtual desktops

### Examples of Client Applications

* Web browsers
* Microsoft Outlook
* Microsoft Teams
* File Explorer
* Remote Desktop Client
* SSH clients
* Database applications
* API clients

A client does not always have to be an entire computer.

An application can also act as a client.

For example:

```text
┌─────────────────┐
│   Web Browser   │
│     Client      │
└────────┬────────┘
         │
         │ HTTPS
         ↓
┌─────────────────┐
│   Web Server    │
│     Server      │
└─────────────────┘
```

The important point is that **client and server describe roles**.

A computer can act as a client in one communication and as a server in another.

---

## 🖥️ What is a Server?

A server is a computer or software service that provides resources or services to clients.

Servers can provide many different types of services.

Examples include:

* File storage
* Websites
* Databases
* Authentication
* DNS
* DHCP
* Email
* Applications
* APIs
* Printing
* Virtualization
* Storage services

A server can be:

* A physical server
* A virtual machine
* A cloud virtual machine
* A container
* A software application

For example:

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

---

## 🔄 Client vs Server

| Feature            | Client                     | Server                          |
| ------------------ | -------------------------- | ------------------------------- |
| Primary purpose    | Requests services          | Provides services               |
| Example            | Web browser                | Web server                      |
| Example            | File Explorer              | File server                     |
| Example            | Outlook                    | Mail server                     |
| Example            | Database application       | Database server                 |
| Communication      | Sends requests             | Receives and processes requests |
| Resources          | Usually consumes resources | Usually provides resources      |
| Can be physical    | Yes                        | Yes                             |
| Can be virtual     | Yes                        | Yes                             |
| Can exist in cloud | Yes                        | Yes                             |

The difference is mainly based on the **role being performed**.

---

# 🌐 How Client-Server Communication Works

Clients and servers communicate through a network.

A simplified communication process looks like this:

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

For communication to work correctly, several technologies may be involved.

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

For example, when a user accesses a website:

```text
User
 │
 ↓
Browser
 │
 │ DNS Query
 ↓
DNS Server
 │
 │ IP Address
 ↓
Browser
 │
 │ TCP Connection
 ↓
Port 443
 │
 │ HTTPS
 ↓
Web Server
```

This demonstrates how multiple networking components work together to provide a service.

---

# 📡 Request and Response

Most client-server communication follows a request and response model.

The client sends a request, the server processes the request, and the server returns a response.

### Example: Web Application

```text
Client
   │
   │ "Give me the website"
   ↓
Web Server
   │
   │ Process Request
   ↓
Web Server
   │
   │ "Here is the website"
   ↓
Client
```

### Example: File Server

```text
CLIENT01
   │
   │ "I need Report.xlsx"
   ↓
FILE01
   │
   ├── Check file
   ├── Check user
   ├── Check permissions
   │
   │ Response
   ↓
CLIENT01
```

### Example: DNS

```text
CLIENT01
   │
   │ "What is the IP address of DC01?"
   ↓
DNS Server
   │
   │ "192.168.10.10"
   ↓
CLIENT01
```

### Example: Authentication

```text
User
 │
 │ Credentials
 ↓
Client
 │
 │ Authentication Request
 ↓
Authentication Server
 │
 │ Authentication Result
 ↓
Client
```

---

# 🏢 Common Enterprise Servers

Enterprise environments usually contain different servers for different workloads.

## Web Server

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

## File Server

A file server provides centralized file storage to users and applications.

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

Windows environments commonly use **SMB** for network file sharing.

---

## DNS Server

A DNS server provides name resolution.

It translates names into IP addresses.

```text
CLIENT01
    │
    │ "What is the IP of DC01?"
    ↓
DNS Server
    │
    │ 192.168.10.10
    ↓
CLIENT01
```

DNS is particularly important in Windows and Active Directory environments.

---

## DHCP Server

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

## Authentication Server

An authentication server validates user identities.

In a Windows enterprise environment, **Active Directory Domain Services** provides centralized identity and authentication capabilities.

```text
User
 │
 │ Username + Password
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

## Database Server

A database server stores and manages application data.

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

## Application Server

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

## Email Server

An email server provides messaging services.

Traditional enterprise environments may use:

```text
Microsoft Exchange Server
```

Modern cloud environments may use:

```text
Exchange Online
```

---

# 🧩 Server Roles and Services

A single server can provide multiple services.

For example, a small organization might have:

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

This approach can be suitable for:

* Small organizations
* Development environments
* Test environments
* Learning labs

However, larger organizations commonly separate workloads.

```text
┌──────────────┐
│     DC01     │
│              │
│ AD DS + DNS  │
└──────────────┘

┌──────────────┐
│    DHCP01    │
│              │
│    DHCP      │
└──────────────┘

┌──────────────┐
│    FILE01    │
│              │
│ File Services│
└──────────────┘

┌──────────────┐
│    WEB01     │
│              │
│ Web Services │
└──────────────┘
```

Separating workloads can provide better:

* Security
* Performance
* Availability
* Scalability
* Management
* Troubleshooting

---

# 🏗️ Centralized Architecture

In a centralized architecture, multiple services are hosted on a smaller number of servers.

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

### Advantages

* Simple to manage
* Lower infrastructure requirements
* Easier initial deployment
* Suitable for smaller environments

### Disadvantages

* Single point of failure
* Resource contention
* Limited scalability
* Larger impact if the server fails

---

# 🌐 Distributed Architecture

In a distributed architecture, different workloads are distributed across multiple servers.

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

Distributed architecture is commonly used in enterprise environments.

### Advantages

* Better workload separation
* Improved scalability
* Easier maintenance
* Reduced impact of individual failures
* Better security boundaries
* Independent resource allocation

---

# 🏢 Enterprise Client-Server Example

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
     AD DS + DNS            SMB Shares          Web Application
          │                     │                     │
          └─────────────────────┼─────────────────────┘
                                │
                  ┌─────────────┴─────────────┐
                  ↓                           ↓
              CLIENT01                    CLIENT02
```

Different services work together to provide the complete enterprise environment.

### User Authentication

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

### File Access

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

### Application Access

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

This demonstrates how multiple servers can work together to deliver business services.

---

# 🔐 Authentication and Authorization

Client-server environments commonly involve two important security concepts.

## Authentication

Authentication answers:

> **Who are you?**

Examples:

* Username and password
* Multi-factor authentication
* Certificates
* Biometrics
* Security tokens

---

## Authorization

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
 │ User identified
 ↓
Authorization
 │
 ├── Finance Share → ❌
 ├── HR Share → ❌
 └── Public Share → ✅
```

Authentication and authorization become especially important when learning **Active Directory, Group Policy, Microsoft Entra ID, RBAC, and Zero Trust**.

---

# 🔌 Protocols and Ports

Client-server communication commonly uses network protocols and ports.

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

These ports help systems identify which service should receive network traffic.

For example:

```text
Client
 │
 │ TCP
 │ Port 443
 ↓
Web Server
```

The server listens for connections on the appropriate port.

---

# 🏠 Client-Server Architecture in On-Premises Environments

In traditional on-premises infrastructure, the organization owns or manages the physical infrastructure.

A simplified environment might look like:

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

The organization is responsible for:

* Servers
* Storage
* Networking
* Operating systems
* Applications
* Security
* Backup
* Maintenance

---

# ☁️ Client-Server Architecture in Cloud Computing

The client-server model also exists in cloud computing.

The main difference is **where the infrastructure is hosted and who manages it**.

```text
Client
   │
   ↓
Internet
   │
   ↓
Cloud Service
   │
   ├── Compute
   ├── Storage
   ├── Networking
   └── Application
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

The underlying servers may be located in a cloud provider's data center rather than inside the organization's own data center.

---

# 🔄 Client-Server Architecture in Hybrid Environments

Hybrid environments combine on-premises infrastructure with cloud services.

```text
                 ON-PREMISES
        ┌─────────────────────────┐
        │                         │
        │ Active Directory        │
        │ DNS                     │
        │ Windows Servers         │
        │ File Servers            │
        │                         │
        └────────────┬────────────┘
                     │
                     │ Hybrid Identity
                     │
                     ↓
                 CLOUD
        ┌─────────────────────────┐
        │                         │
        │ Microsoft 365           │
        │ Intune                  │
        │ Defender                │
        │ Cloud Applications      │
        │                         │
        └─────────────────────────┘
```

This hybrid model is particularly important for organizations that are modernizing existing on-premises infrastructure while adopting cloud services.

The concepts learned here will later connect with:

* Active Directory
* Hybrid Identity
* Microsoft 365
* Microsoft Intune
* Microsoft Defender
* Microsoft Purview
* Zero Trust

---

# 🧠 Important Concept: Client and Server Are Roles

One of the most important concepts to remember is that **client and server are roles, not necessarily different types of computers**.

For example:

```text
Computer A
    │
    │ Requests DNS
    ↓
Computer B
    │
    └── DNS Server
```

Computer B is acting as a server for DNS.

But Computer B could also request information from another server:

```text
Computer B
    │
    │ Requests Time
    ↓
Time Server
```

In this communication:

```text
Computer B = Client
Time Server = Server
```

Therefore, the same system can act as both a client and a server depending on the service being used.

---

# 🏢 Enterprise Infrastructure Relationship

The concepts introduced in this section form the foundation for the rest of the repository.

```text
                 Enterprise Infrastructure
                          │
        ┌─────────────────┼─────────────────┐
        ↓                 ↓                 ↓
     Clients           Servers           Network
        │                 │                 │
        │                 ├── DNS          │
        │                 ├── DHCP         │
        │                 ├── AD DS        │
        │                 ├── File Server  │
        │                 ├── Web Server   │
        │                 └── Applications │
        │                                   │
        └───────────────────────────────────┘
```

Later, this architecture will evolve into:

```text
On-Premises Infrastructure
          ↓
Windows Server
          ↓
DNS / DHCP
          ↓
Active Directory
          ↓
Group Policy
          ↓
File Services
          ↓
PowerShell Automation
          ↓
Hybrid Identity
          ↓
Microsoft 365
          ↓
Intune
          ↓
Defender
          ↓
Purview
          ↓
Zero Trust
```

---

# 🔑 Key Takeaways

* Client-server architecture is a fundamental enterprise IT concept.
* A **client requests** a service or resource.
* A **server provides** a service or resource.
* Client and server are roles rather than necessarily different types of computers.
* Clients and servers communicate through networks.
* Communication can involve IP addresses, DNS, routing, TCP/UDP, ports, firewalls, and application protocols.
* Common enterprise servers include DNS, DHCP, file, web, database, application, email, and authentication servers.
* Small environments may use centralized services.
* Enterprise environments commonly use distributed architectures.
* Authentication determines who a user is.
* Authorization determines what the user can access.
* Client-server architecture is used in on-premises, cloud, and hybrid environments.
* Understanding client-server architecture provides the foundation for learning enterprise Windows and hybrid cloud infrastructure.
