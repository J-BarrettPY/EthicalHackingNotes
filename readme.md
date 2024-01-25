# Ethical Hacking
**Course/CEH Exam Notes**

## Overview of Ethics

As part of the code of ethics, you will be sworn to keep information you obtain as part of your work private, paying particular attention to protecting the information and intellectual property of employers and clients. 

You are expected to disclose information that needs to be disclosed to the people whp have engaged your services. You are also expected to disclose potential conflicts of interest.

The first-time responsible disclosure was identified and documented in the 1990s. The security researcher Rain Forest Puppy developed a full disclosure policy, sometimes called the Rain Forest Puppy Policy (RFP or RFPolicy).

Another responsible disclosure took place in mid-2000s by Dan Kaminsky. He found serious flaws in the implementation of the Domain Name System (DNS), which impacts everyone on the internet. He worked with vendors to make sure they had time to fix their services before disclosing the information publicly.

As you perform work, you will be given access to resourced provided by the client or company. Under the EC-Council code of ethics, you will need to agree to, you cannot misue any of the equipment. You cant damage anything you have access to as part of your employment or contact. 

Perhaps it goes without saying, but you are not allowed to engage in any illegal actions during penetration testing. Similarly, you cannot have been convicted of any felony. Along the same lines, though its not directly illegal, you cant be involved with any group that may be considered “black hat”, meaning they are engaged in potentially illegal activities. 

Communication is also important when you embark on an engagement, regardless of whether you are working on contract or are a full-time employee.

# Overview of Ethical Hacking

Fun fact: Mirai botnet, which infected smaller, special-purpose devices running an embedded implementation of Linux, is believed to consist of well over 100k bots with the possibility being more than one million. 

Since 2005, there has not been a year without at least 10 million data records being compromised. In 2017, nearly 200 million records were compromised just from the United States alone. 

One of the challenges of ethical hacking is to think like an attacker. Testing of this nature is often challenging and requires a different way of thinking. When doing any sort of testing, including ethical hacking, a methodology is important, as it helps to ensure that your actions are both repeatable and verifiable. 

EC-Council helps to ensure that this work is done ethically by requiring anyone who has obtained Certified Ethical Hacker certifications agree to this code of conduct.

Ethical hacking, also known as penetration testing or red teaming, is an act of locating the weaknesses and vulnerabilities of computer and information systems by duplicating the intent and actions of malicious hackers. Its all about ferreting out the problems to improve overall security posture of the target. An ethical hacker is a security professional who applies their hacking skills for defensive purposes on behalf of the owners of information systems. Ethical hackers are among the most sought-after information security employees in large organizations.

# Attack Modeling 
There are some testing or assessment methodologies that get used throughout the industry, including the Penetration Testing Execution Standard (PTES) and the Open Source Security Testing Methodology Manual (OSSTMM). These methodologies are typically built around expectations of what an attacker would do or how attackers operate. 

The first is the cyber kill chain, another is the attack life cycle, while a third is the MITRE ATT&CK framework. 

## Cyber Kill Chain
A commonly referred – to framework in the information security space is the cyber kill chain. A kil chain is a military concept of the structure of an attack. The idea of a kill chain is that you can identify where the attacker is in their process so you can adapt your own response tactics. 

Lockheed Martin, a defense contractor, adapted the military concept of a kill chain to the information security space. Kill chai developed by Lockheed Martin:
-	Reconnaissance – Research, identification, and selection of targets.
-	Weaponization – Pairing remote access malware with exploit into a deliverable payload.
-	Delivery – Transmission of weapon to target (e.g., via email attachments, websites, or USB drives).
-	Exploitation – Once delivered, the weapon’s code is triggered, exploiting vulnerable applications or systems. 
-	Installation – The weapon installs a backdoor on a target’s system, allow persistent access.
-	Command & Control – Outside server communicates with the weapons providing “hands-on-keyboard access” inside the target’s network.
-	Actions on Objective – The attacker works to achieve their objective of the intrusion, which can include exfiltration or destruction of data, or intrusion of another target. 

The first stage of the cyber kill chain is reconnaissance. This is where the attacker identifies their target as well as potential points of attack. 

Once the attacker has identified a target, they need to determine how to attack the target. This is where weaponization comes in. The attacker may create  a custom piece of malware, for instance, that is specific to the target. The may just use a piece of common off-the-shelf (COTS) malware, though this has the potential to be discovered by antivirus software installed in the victim’s environment. 

Delivery is how you get the weapon (the malware or the link to a rouge website) into the victim’s environment. This could be a network-based attack, meaning there is an exposed service that may be vulnerable to exploit remotely. This could be sending an attachment via email, or it could be that the malicious software is hosted on a web server the victim is expected to visit and they get infected when they hit the website. Exploitation could be when the malicious software infects the victim’s system. 

Exploitation leads to installation. The attacker will install additional software to maintain access to the system and perhaps give themselves remote access to the system. Once installation is complete, the attacker moves to command & control. You will sometimes see this referred to as C2 or C&C. 

These actions are called actions on objectives. Each attacker may have different objectives they are trying to achieve. Attackers who are criminally oriented are probably looking for ways to monetize the infected systems by stealing information that could be stolen or by selling off access to another organization. So-called nation-state actors may be looking to gain access to intellectual property. No matt what the organization is, they have objectives they are trying to achieve. They will keep going until they achieve those objectives.

## Attack Lifecycle
The security technology and consulting company Mandiant often refers to a different methodology called the attack life cycle. This is different from the cyber kill chain, though there are some similarities. Rather than a theoretical exercise or one with a military focus, thee attack life cycle describes exactly how attackers have operated for as far back as there have been attacks against computing infrastructure. 


```| Initial Recon | Initial Compromise | Establish Foothold | Escalate Privileges -> Complete Mission OR Internal Recon -> Move Laterally -> Maintain Presence -> Escalate Privileges (loop)```


One significant difference between the attack life cycle and the cyber kill chain is a recognition that often an attack is not one-and-done. There is a loop that happens in the middle. Attackers don’t keep launching attacks from outside the network. Once they get into the environment, they use the compromised systems as launch points for additional compromises within the environment. Attackers will gain access to a system and use that system and anything discovered there, like credentials, to move off to another system in the network. Before we get there, though, an attacker identifies a victim and potential attack possibilities in the initial recon stage. The attacker is doing reconnaissance, including identifying names and titles using open source intelligence, meaning they use public source like social network sites, to generate attacks. To gain access, they launch attacks commonly, these would be phishing attacks. This is the initial compromise stage.

Once they have compromised a system, the attacker will work to establish a foothold. This includes making sure they retain access to the system so they can get in when they need to. It may take days or weeks to move from one phase of the attack life cycle to another.

To do much else, the attacker will need to escalate privileges. They need to have administrative privileges to move into the loop that happens as they continue to move through the environment, gathering additional systems along thee way. They will probably be gathering credentials from memory or disk here. They will also be investigating connections they system is known to have had with other systems in the network. This is a form of internal reconnaissance.

The reconnaissance is necessary to be able to move laterally. This is sometimes known as east-west movement. If you think about the network diagram, the connection to the outside world is quite often on the top. On a map, the would be north, so moving into and out of the network is known as north-south. Any movement within the organization is side to side or lateral movement. On a map, side to side would be east-west. To make those lateral movements, attackers need to know what systems there are. 

With every system the attacker gets access to, they need to maintain presence. This means some form of persistence, so any malware that is allowing the attacker access remains running. You might use the Windows registry, scheduled tasks, or other types or persistence to keep any malware running. 

The last phase of the attack life cycle, though leaving it until the end is misleading, is complete mission. Again attacks tend not to be one-and-done. Once an attacker is in your environment, they will likely be continuing to revisit to see if there is anything else they need. They may be continuing to get a broader reach within the organization. The complete mission phase is where data may be exfiltrated from the environment. This again, may not be a onetime thing. The attacker may continue to find additional targets in the environment to exploit, which would likely mean additional exfiltration.

## MITRE ATT&CK Framework
While the attack life cycle does a good job describing the process an attacker goes through, it does not describe the specific behaviors used by the attacker, which are called techniques, tactics, and procedures (TTPs). The MITRE ATT&CK Framework is a taxonomy of TTPs, which means it is a way of organizing TTPs that have been seen in the real world into a set of categories. Mostly, the categories follow the same attack trajectory seen in the attack life cycle and the cyber kill chain, though there are some categories that are called out separately because it’s useful to understand some of the specific TTP categories that may be done in parallel stream or be part of multiple stages of the attack life cycle or cyber kill chain. Following are the stages the ATT&CK Framework identifies:
-	Reconnaissance: The attacker is looking for victims or ways to get into victim’s systems that have been identified. 
-	Resource Development: Infrastructure for managing compromised hosts is put together here, as well as developing exploits or collecting credentials from other sources that could be used.
-	Initial Access: Systems or user accounts are compromised to provide the attacker access to a resource that can be used.
-	Execution: This is not a stage itself, but instead describes a series of actions or behaviors an attacker might use to maintain access to the system. This could include executing PowerShell scripts.
-	Persistence: The attacker needs to ensure they maintain access beyond reboots or other system changes, so they need to be sure they have a program that always runs when the system is started, or at least when a user logs in.
-	Privilege Escalation: As user behavior is restricted, attackers would typically look to gain administrative privileges. The process of obtaining the level of permissions is called privilege escalation.
-	Defense Evasion: Businesses will do a lot of work trying to protect systems, looking for malware and instances of persistence. When attackers try to get access and maintain access regardless of the protection measures in place, it’s defense evasion and may include masquerading or execution hijacking or tampering with protections in place.
-	Credential Access: A common attack practice is to gather usernames and passwords. This may be done either from previous attacks or users directly. Any username and password set may be useful at some point.
-	Discovery: Any activity that collects information within the victim environment could be considered discovery.
-	Lateral Movement: Attackers will generally move from one system to another within the victim environment, to collect more information or to gather details about systems or users that could be used elsewhere.
-	Collection: Once the attacker has found information they want to use or sell, they need to pull it together. This is the collection refereed to here. It may be something simple like staging the data somewhere in the network.
-	Command and Control: Thee attacker needs a way of getting remote access to systems or to send commands to those systems. Usually, there is infrastructure in place to perform this command and control work.
-	Exfiltration: Data that has been collected needs to be moved out to the attacker locations so it can be dealt with. Moving the data out of the target environment to the attacker’s place is exfiltration. 
-	Impact: Attackers aren’t always looking to steal information. Sometimes they are looking to be destructive, or in the case of some types of ransomware, they are looking to modify data by encrypting it so victims cant get access, requiring the pay the attacker. 

# Methodology of Ethical Hacking
The basic methodology is meant to reproduce what real-life attackers would do. You will see similarities here to both the cyber kill chain and the attack life cycle.

## Reconnaissance and Footprinting
Reconnaissance is where you gather information about your target. Footprinting is just getting an idea of the “footprint” of the organization, meaning the size and appearance. The objective of reconnaissance and footprinting is determining the size and scope of your test. 

In the process of doing this work, you may also turn up personal information belonging to employees at your target. This will be useful when it comes to social engineering attacks. These types of attacks make up `80 to 90 percent` of infiltration as a result of these types of social engineering attacks. 

## Scanning and Enumeration
Once you have network blocks identified, you will want to identify systems that are accessible within those network blocks; this is the scanning and enumeration stage. You will need to identify services running on any available host. These services will be used as entry points. This includes not only a list of all open ports, which will be useful information, but also the identity of the service and software running behind each open port. 

This may also result in gathering information that different services provide. This includes the software providing the services, such as NGINX, Apache, or IIS for a web server. Additionally, there are services that may provide a lot of details about not only the software but the internals of the organization. This may be usernames. Some Simple Mail Transfer Protocol (SMTP) servers will give up valid usernames if they are queried correctly. Windows servers using the Server Message Block (SMB) protocol or the Common Internet File System (CIFS) protocol can be asked for information.

## Gaining Access
This is where you demonstrate that some services are potentially vulnerable. You do that by exploiting the service. Documentation is very important for this part.

Technical attacks, like those exploiting vulnerabilities in listening network services, are sometimes thought of as how systems get compromised, but the reality is that social engineering attacks are far more likely to be the way attackers gain access to systems. This is one of the reasons why enumeration is important – because you need targets for social engineering attacks. 

Another mechanism for gathering information from users is to get them to visit a website. This may be a website that you, as the attacker, have loaded with malicious software that will infect their systems.

## Maintaining Access
 As attacks take time and vulnerabilities change with patching or systems might need to shutdown, you will need to ensure you have persistent access.

This is another stage where malware can be beneficial. You may need to install a rootkit, for example, that can provide you with a backdoor as well as the means to obscure your actions and existence on the system. You may need to install additional software to maintain access. 

## Covering Tracks
Covering your tracks is where you hide or delete any evidence to which you managed to get access. This can be accomplished with malware that ensures that your actions aren’t logged or perhaps the malware misreport system information, like network connections. 

One thing to keep in mind when you are trying to cover your tracks is that sometimes your actions may also provide evidence of your work. For example, **wiping logs on a Windows system will leave a log entry indicating that the log have been wiped.**

Ethical Hacking Methods:
-	Reconnaissance and footprinting
-	Gaining access
-	Covering tracks
-	Planning and direction
-	Dissemination and feedback

## Flashcard Review
-	Black-hat hacker – Who violates computer security for personal gain or pure maliciousness?
-	White-hat hacker – Who is the opposite of a black-hat hacker?
-	Gray-hat hacker – Who falls somewhere between a black-hat hacker and a white-hat hacker?
-	Removing evidence of your presence in a system - What is the purpose of covering the track?
-	Determining the size and scope of your test - What is the objective of reconnaissance and footprinting?
-	Giving attackers remote access to the infected system - What is the purpose of the command and control (C2) phase?

# Network Foundations

## OSI Layers 
-	Application
-	Presentation
-	Session
-	Transport
-	Network
-	Data Link
-	Physical

Application: The Application layer is the one closest to the end user. Application layer protocols manage the communication needs of the application. For example, the Hypertext Transfer Protocol (HTTP) is an Application layer protocol. 

Presentation: The Presentation layer is responsible for preparing data for the Application layer. It ensures the data handed up to the application is in the right format so it can be consumed. When systems are communicating, there may be disconnects in formatting between the two endpoints, and the Presentation layer makes sure that data is formatted correctly. As such, character encoding formats like the American Standard Code for Information Interchange (ASCII), Unicode, and the Extended Binary Coded Decimal Interchange Code (EBCDIC) all belong at the Presentation layer. Additionally, so does the Joint Photographic Experts Group (JPEG).

Session: The Session layer manages the communication between the endpoints when it comes to maintaining the communication of the applications (the client or sever). Remote procedure calls (RPCs) are an example of a function at the Session layer. The Session layer takes care of making sure that files are successfully transmitted and complete for example.

Transport: The Transport layer takes care of segmenting messages for transmission. Both the TCP and the UDP are transport protocols. 

Network: The Network layer gets messages from one endpoint to another. IP is one protocol that exists or operates at this layer.

Data Link: One other address to contend with is the media access control (MAC) address. This is a layer 2 address, identifying the network interface on the network so communications can get from one system to another on the local network. The Address Resolution Protocol (ARP), virtual local area networks (VLANs), Ethernet, and Frame Relay are Data Link layer protocols.

Physical: This is all the protocols that manager the physical communications. 10BaseT, 10Base2, 100BaseTX, and 1000BaseT are all examples of Physical layer protocols.

## TCP

-	Application
-	Transport
-	Internet
-	Link

Essentially what happens is that the Session, Presentation, and Application layers from the OSI model are collapsed into the Application layer in the TCP/IP model. Additionally, the Physical and Data Link layers from the OSI model are collapsed into the Link layer in the TCP/IP model. 

# Knowledge Check
True or false about communication models:
-	They are broken into layers and the layers are stacked on top of one another. Hence, they are generally referred to as communication stacks.
-	They make use of the protocol, which is a set of rules or conventions that dictate communication.
-	The two main communication models are the OSI model and the TCP/IP model.
-	The OSI model has four layers, whereas the TCP/IP model has seven layers.
-	The OSI model is developed by ISO, whereas the TCP/IP model is developed by ARPAnet.

F, T, T, F, T

Application: Determines whether a remote communication partner is available and accessible.
Network: Responsible for adding routing and addressing information to the data.
Presentation: Imposes common or standardized structure and formatting rules onto the data.
Session: Responsible for establishing, maintaining, and terminating communications between two computers.
Transport: Responsible for managing the connection integrity and controlling the session.

TCP/IP Architecture Layers:
-	Application
-	Transport
-	Internet
-	Link

## Topologies
-Bus network, consists off a single network cable to which every device on the network connects.
-Star network has a mediating device between all devices. This may be a hub or switch.
-Ring network centralized unit which all devices connect to.
-Mesh all devices are connected to each other.

## Physical Networking

# Knowledge Check
-	A MAC address is represented in hexadecimal values because it’s a common way to represent octets.
-	The common format of a MAC address is 8 octets, generally separated by colons.
-	Users send messages to every device on the network by using the broadcast address. The broadcast MAC address is ff:ff:ff:ff:ff.
-	Switching makes determinations about what traffic goes to which port based on the destination IPv4 address.
-	Switching reduces the amount of traffic going out the switch port and down the wire and improves performance.

T, F, T, F, T

## IP

# Knowledge Check
-	IPv6: Uses 128-bit addresses laid out in a hexadecimal notation.
-	IPv6: Supports auto and renumbering address configuration.
-	IPv4: Supports manual and DHCP address configuration.
-	IPv4: Uses 32-bit addresses laid out in a dotted-decimal notation.

Type of service: Assists network elements in making decisions about the QoS by prioritizing and deprioritizing messages.
Time to live: Indicates how long a message can stay on the network before being considered expired.
Fragment offset: Indicates where the data in the packet aligns and is measured in units of 8-byte blocks.
Checksum: Determines whether the header is intact and is defined as a 1’s complement sum of the 16-bit words.
Protocol: Informs the receiving system which headers to look for in the transport header.

## TCP

# Knowledge Check

Sequence number: A 32-bit number set to a random value when the conversation is initiated.
Data offset: A 4-bit value indicating the number of 32-bit words in the TCP header.
Control bit: A 6 flag bit value used to indicate the disposition of the message. 
Source port: A 16-bit field that involves traffic originated from on the sending side.
Checksum: A 16-bit field used to make sure that the communication hasn’t been corrupted. 
Destination port: A 16-bit field assigned to the application communicating with the server.

## Network Architectures
MAN: Serves a large geographical area that sits in between a local area network and a wide area network.
LAN: Includes systems that are local and probably in the same room or building or on the same floor.
VLAN: Handles the isolation at layer 2 by software/firmware rather than physically.
WAN: Consists of a network whose nodes are more than 10 or so miles apart.

## Cloud Computing

## Storage as a Service (SaaS)
Storage as a service has a large number of uses, including backups and the ability to access your data no matter where you are or what device you are using.

## Infrastructure as a Service (IaaS)
Virtualizing your complete infrastructure.

## Platform as a Service (PaaS)
Using PaaS, you can quickly create an entire virtual network with all of the virtual devices needed to support the service or application. 

## Software as a Service
Using software online, such as Google Docs or Office Online. 

# Knowledge Check

PaaS: Provides the ability to develop applications in a virtual environment without the cost of a physical platform.
IaaS: Offers computer networking, storage, load balancing, routing, and VM hosting.
SaaS: Requires some type of front end or web portal to make itself available to the user. 



