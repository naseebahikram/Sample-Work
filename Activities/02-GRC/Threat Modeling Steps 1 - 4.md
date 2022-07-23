## Threat Modeling: Steps 1 - 4

#### Step 1: Determine Assessment Scope

Read the following overview and Geldcorp Network infrastructure to familiarize yourself with the assessment scope then answer the review questions below.

#### GeldCorp Overview**

- GeldCorp is a financial technology firm that helps clients manage and optimize their stock portfolios. They offer two main services:

  - Custom Trading Platform: A web application that clients use to transfer money between their bank and trading accounts, buy and sell stock, and enable automated trading features.

  - Financial Advising: GeldCorp also allows clients to purchase advisory services. This service gives them one in-person meeting with a financial advisor every quarter. It also grants them access to the live chat feature, which they can use from the web application to request advice 24/7.

- GeldCorp offers these services separately, and therefore runs them as separate businesses. For this activity, you’ll focus specifically on assessing the network assets that these businesses rely on. Then, you’ll identify the threat agents, possible attacks, and exploitable vulnerabilities relevant to its most critical assets. 

#### GeldCorp Network Infrastructure

Network infrastructure includes all the devices that make up a network and aid in transporting data across it. These include routers, firewalls, and switches, which we’ll cover in-depth during a later unit. For now, we’ve provided brief descriptions of the relevant devices in this activity.

- **Corporate Intranet**: Refer to the topology below for a simplified diagram of the corporate intranet.

  - A corporate intranet is a private computer network that allows access only to authorized employees. It’s used to securely share company information and resources, among other purposes.

  - A network topology shows how the nodes, or devices, are arranged and connected to one another in a network. We’ll dive into topologies in a later unit, but for now, note that they are often depicted in maps like the one in this activity.

  ![diagram](https://github.com/naseebahikram/Sample-Work/blob/main/Activities/02-GRC/Images/diagram.png)

- **Router** (receives Internet, receives VPN, provides DHCP)

    - A router is a networking device that forwards (or "routes") resources to other networks. In this case, the router is the hub that sets up the corporate intranet and manages all of the devices on it.  It receives internet, is a VPN gateway, and provides DHCP. 

    - Routers can forward resources to other routers, computers, and access points. An access point is a device, such as a router, that allows other devices to connect to a network. It allows in part for more devices to be on the network.

- **Domain Controller** (Windows Active Directory Command Center)

    - A domain controller is a Windows server that manages network security and is responsible for user authentication and authorization. It’s a primary way for authenticating users on the network.

- **Department Routers** (receive forwarded internet, VPN)
    - Each department has an associated domain name.

- **Department Databases**

    - Each department has a private database in their own subnet. We’ll discuss subnets in depth during a later unit, but for now note that subnetting allows large networks to be divided into smaller networks, and each of these subnets has its own set of IP addresses.

    - All employees in a department have full access to all databases.

- The entire network is managed with Windows Active Directory. We’ll learn more about Active Directory during a later unit, but for now know that AD is a directory service for Windows domain networks. Among other tasks, it is used for managing devices on a network.

- The network and system administration team keep all systems fully patched at all times. GeldCorp does not enforce content filters, meaning that employees can visit any sites they want.

Note the following additional information:

- Each department has its own subnet.

- Employees who connect to the intranet from home must use the VPN.

- All employees in a given department have access to all of that department’s data servers.

#### Review Questions:

After reading the above overview, answer the following questions:

1. Identify Threat Agents: List three threat agents relevant to the web application.
    - Script kiddies
    - Organized cybercriminals
    - Insider threats

2. Identify Possible Attacks: List five attacks relevant to the web application and which threat agent is most likely to use each one. 

    - **Phishing**: An attacker might try to gain access to the private intranet by phishing employees.

    - **Malware**: Attackers might use malware to infect the intranet. For example, they may infect it with ransomware.

    - **Physical attacks**:  Attackers might be able to gain physical access to the building.

3. Identify Exploitable Vulnerabilities: Identify three possible vulnerabilities in the web application infrastructure, and rank them in order of severity. 
  
    - **No content filter**: Employees can download files from any site they want. This makes it much easier for attackers to introduce malware.

    - **Poor access control policies**: Every employee in a department should not have access to all of that department's data.

    - **Older workstations**: Windows 7/8 machines are more vulnerable than newer versions.
