# Ethical Hacking
**CEH Exam Notes from EC-Council**
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

# Flashcards
-	What is the Open System Interconnection (OSI) model?
A: A seven-layer model describing functions of communications systems.
-	What is the Transmission Control Protocol (TCP)/Internet Protocol (IP)?
A: A four-layer architecture of communications protocols.
-	What is a subnet mask?
A: A four-octet value indicating which part of an Internet Protocol (IP) address in the network and which is the host.
-	What is the Classless Inter-Domain Routing (CIDR)?
A: The number of bits covering the network portion of the Internet Protocol (IP) address.
-	What is layer 7?
A: An Application layer of the Open System Interconnection (OSI) model, where protocols like Simple Mail Transfer Protocol (SMTP) and File Transfer Protocol (FTP) reside.
-	What is the star network?
A: A network topology where all endpoints connect to a central device.
-	What is a Transmission Control Protocol (TCP)?
A: A layer 4 protocol that is connected-oriented.
-	What is the User Datagram Protocol (UDP)?
A: A layer 4 protocol that is connectionless.
-	What is a three-way handshake?
A: The three messages used to establish a Transmission Control Protocol (TCP) connection (SYN, SYN/ACK, and ACK)
-	What is a virtual machine?
A: An operating system that doesn’t run on physical hardware but instead runs on a hypervisor, which virtualizes central processing unit (CPU), memory, network, and disk. 
-	What is a virtual area network (VLAN)?
A: A LAN where the isolation at layer 2 is handled by software/firmware rather than physically.
-	What is IP Security (IPSec)?
A: A set of functionality introduced in IPv6 that adds confidentiality and integrity controls to packets being transmitted.


# Chapter 3 : The Triad
The three elements of the triad are confidentiality, integrity, and availability. 

## Confidentiality
Keeping stuff safe and secure, yo.

## Integrity
Keeping stuff the same and uncorrupted, yo.

A man-in-the-middle attack is one way for an attacker to compromise integrity. The attacker intercepts the data in transit, alters it, and then sends it on the way.

## Availability
Keeping stuff on, yo.

Misconfigurations can result in problems with availability. So can malicious attacks, like DoS attacks.

## Parkerian Hexad
In 1998, Donn Parker extended the initial three properties by adding three more. The three additional properties:
-	Possession (or Control): Confidential device, data, or information is no longer in the possession of your control.
-	Authenticity: Making sure that when you get a piece of data, no matter what it is, its actually from where it says its from.
-	Utility: Making sure that whatever you have, such as data, has a purpose. 

# Knowledge Check

Integrity: The consistency, accuracy, and validity of data or information.
Confidentiality: A characteristic of a business resource ensuring access is restricted to only permitted users, applications, or computer systems.
Availability: A characteristic of a resource being accessible to a user, application, or computer system when required.

Parkerian Hexad properties:
-	Integrity
-	Possession
-	Utility
-	Authenticity 

# Information Assurance and Risk

Risk combines the likelihood of an event and its potential negative impact. It's more than just probability - it involves quantifying both the chance of an occurrence and its consequences. 

Calculating risk, especially in complex areas like information security, is difficult due to variable factors. Understanding risk requires evaluating both the potential loss and its likelihood, crucial for prioritizing in fields like information security. 

This approach distinguishes high-risk scenarios by considering both severity and probability, countering the common tendency to focus only on extreme outcomes.

A threat agent is an entity that poses a potential danger, often exploiting vulnerabilities through various threat vectors. Understanding these agents and vectors is crucial for identifying and mitigating risks to valuable resources. Information assurance involves assessing these risks and implementing controls—preventive, detective, or corrective—to safeguard information assets. 

These controls can be technical, like software solutions; administrative, like policies and procedures; or physical, like security cameras. Managing risk in business involves four strategies: 
-	Acceptance (acknowledging and preparing to bear the risk)
-	Transference (shifting the risk to another party, often through insurance)
-	Mitigation (reducing the risk through various controls)
-	Avoidance (not engaging in activities that introduce the risk). 

Each strategy is chosen based on the business's understanding of the risk and its appetite for handling it.

# Knowledge Check
Indicate if each of the given statements related to risk is true or false:
-	Risk is the exposure to the chance of injury or loss.
-	Risk is the intersection of asset and gain.
-	A threat is something that can incur a breach of confidentiality, integrity, or availability.
-	Race conditions are examples of risks that can be exploited.

T, F, T, F

# Policies, Standards, and Procedures
Once a policy is created, standards are built out of those policies. Closest to where the work actually gets done are procedures. These are developed because of what the standards say.

## Security Policies
A security policy is a statement of intention with regard to the resource of a business. It defines what a company considers to be security – what resources need to be protected, how resources should be utilized in a proper manner, how resources can or should be accessed. These policies are essential to good corporate governance, since the policies are lines that management draws. This means that having management set the tone and direction is not only a good idea, its also required. 

Security policies are not only about defining important resources, they are also about setting expectations of employees. For example, an acceptable use policy. 

Keep in mind as you are thinking about security policy the goals of your policies should be the confidentiality, integrity, and availability of information resources.

Policies should be revisited on a regular basis. They are sufficiently high-level that they shouldn’t change every time there is a new set of technologies available, but they should evolve with changes in the threat landscape. 

## Security Standards
A standard is a direction about how policies should be implemented. The standard starts down the path of how we get from statements of intent to implementation, so we start to drill down from the high level of the policy. 

Take, for example, a policy that states that all systems will be kept up-to-date. To get closer to implementation of that policy, you might have standards that relate to desktop systems, server systems, network devices, and any embedded devices. The requirements for each of those device types may be different, so the standards for them may be different. Desktop systems may just be expected to take all updates as they come, with the expectation that any potential outage could be remediated quickly on the off change that there was an outage on a handful of users’ desktops. 

## Procedures
Procedures are the actual implementation of the standard. These provide guidance about how, specifically, the standards are achieved at a granular level. This may be accomplished with step-by-step instructions on what needs to be done. There may be multiple procedures for each standard, since there may be multiple organizations involved in implementing the standard. 

## Guidelines
Guidelines are not standards in that they may not be requirements. Instead, they are suggestions on how policies may be implemented. A guideline may provide information about best practices, with the hope that the best practices may follow.

# Knowledge Check
Standard: Provides requirements specifying how an organization implements its information security policies. 
Guideline: Provides the best strategies and suggestions about a given concept, technology, or task.
Policy: Refers to high-level statements for an information security program.
Procedure: Refers to a gradual process that an individual or organization must follow to achieve a security objective. 

# Organizing Your Protections

The MITRE Corporation developed ATT&CK in 2013 to collect common tactics, techniques, and procedures (TTPs) used by attackers. 
The ATT&CK Framework is broken out into the following stages:
-	Reconnaissance: The attacker is gathering information about the target in this stage.
-	Resource Development: The attacker has to do a lot of work to create an infrastructure they will use to launch attacks from. This may include registering domain names, creating accounts, acquiring systems.
-	Initial Access: The attacker here compromises the first systems. They may compromise an existing public-facing application or website. They may use phishing to get malware installed on a target system. They are getting their initial foothold into the organization in this stage.
-	Execution: There are a lot of techniques an attacker may user to get code executed. The attacker doesn’t always have direct interactive access to the system, meaning they cant just double-click an icon or run a command-line program. They may rely on other techniques to get their code executed. There are a lot of ways of doing this, including using scheduled tasks, inter process communication, system services, or operating system-specific techniques like using the Windows Management Instrumentation (WMI) system. 
-	Persistence: With persistence, the attacker is trying to maintain consistent access to the system they have compromised. Systems reboot, sometimes they are powered down and later restarted, or sometimes users log out and then later log back in. 
-	Privilege Escalation: With privilege escalation, attackers are trying to get the highest level of privileges they can. Most users don’t have much in the way of access to their systems. They can get to their data and run programs, but they cant do useful things like install system services or extract system memory. This is where getting additional, elevated privileges is helpful. They may do this by injecting code into an exiting process that already has administrative privileges. They may get a service to run at boot time, since the boot process automatically has elevated privileges. 
-	Defense Evasion: Attackers will need to get through a lot of different types of defense. Businesses certainly, though people as well, make use of software on system to protect against these very attackers. This may be anti-malware or some other detection or prevention software. Attackers need to execute software in ways that wont be seen as malicious or suspicious. This may be using an old-school technique like using a rootkit, where the attacker may be provided remote access while also hiding all of the software being used from the user or other software looking for it. (LOL no mention of obfuscation in this section? WTF??? -------- hackers obviously obfuscate code to get around anti-malware, either manually obfuscating the code to be unreadable or using software which compacts their code making it “laired” and extremely difficult without using forensics to see whats happening. uCertify hackers sucks.)
-	Credential Access: Applications and systems typically require usernames and passwords to grant access. Attackers will want to try to get these credentials for user elsewhere. 
-	Discovery: Attackers are probably not going to be satisfied getting access to just your system. They will be looking for additional systems to get access to.
-	Lateral Movement: One of the reasons for doing discovery, in addition to seeing what data you may have access to that may be stolen for profit, it to determine what other systems may be attacked from your system. The attacker may make use of you and whatever you system has access to.
-	Collection: Just as with discovery, collection is about gather information. This may be information that could be used to attack other systems, or it could be information the attacker wants to steal for sale or use somewhere else.
-	Command and Control: Keey in mind that attackers will want to maintain access to the systems for as long as possible. This stage means setting up and retaining remote access control over the entire environment.
-	Exfiltration: Even if they continue to remain in the environment, they will want to get data they have collected out. This is where they exfiltrate the data.
-	Impact: This is where the attacker may decide to burn the house, as it were…………….. Okay so they blow stuff up or whatever according to boomers.

# Knowledge Check
Execution: Tries to run malicious code, such as running a remote access tool.
Privilege Escalation: Tries to gain higher-level permissions, such as leveraging a vulnerability to elevate access.
Reconnaissance: Gathers information to plan future adversary operations, such as information about the target organization. 
Impact: Manipulates, interrupts, or destroys systems and data, such as encrypting data with ransomware. 
Credential Access: Steals accounts names and passwords, such as keylogging.
Persistence: Tries to maintain their foothold, such as changing configurations.

# Security Technology
## Firewalls
duh.

## Packet Filters
At the basic level, a firewall is a packet filter. 

## Stateful Filtering
Keeps track of the state of messages within the conversation between client and server. This means the firewall has to have a state table, so it knows about all of the traffic flows passing through it. 

## Deep Packet Inspection
A deep packet inspection (DPI) firewall looks beyond the headers and into the payload of the packet. With this approach, its easier to identity malware and other inbound attacks. A DPI firewall would require signatures that it should look for in the packet to determine whether something is going to be malicious so it can block the traffic from coming into the network.

## Application Layer Firewalls
There are application layer firewalls in addition to the DPI firewalls. While these firewalls also inspect the packet, they commonly are specific to a particular protocol. 

## Unified Threat Management
Sometimes firewalls aren’t enough. Even in the case of application layer firewalls, you still need to protect users. Users are often the most vulnerable point of your network, and they are regularly targets of social engineering and malware attacks. A unified threat management (UTM) device is one that consolidates a lot of security functions into a single system that may be placed at a single point in the network. 

## Intrusion Detection Systems
Where firewalls have the ability to block or allow packets in the network stream, a network IDS can take some of the same sorts of rules and generate log messages. A network IDS watches all network traffic that passes by the network interface. This means that placement is important. There may be different approaches to placement, depending on the IDS product being used. One of these approaches is to place the IDS connected in parallel rather than in series at the very perimeter of the network so all network traffic coming in can be observed.

IDS just alert or log.

## Intrusion Prevention Systems
With the IPS in the flow, it can act like a firewall, making decisions about whether to accept or reject packets as they enter the network. The difference between an IPS and a firewall is that the “firewall rules” on an IPS would be dynamic. Rather than having large blanket rules blocking IP addresses wholesale, the IPS would make decisions based on the contents of the packet. 

## Endpoint Detection and Response
Endpoint Detection and Response (EDR) is a class of software that can perform a range of functions that are useful to security operations staff. One function they may provide is anti-malware. EDR solutions may alsop detect other malicious behavior.

## Security Information and Event Management 
A good practice from the standpoint of both system administration and security is system logging. Logs are helpful to diagnose problems in the system and network. They can also help in an investigation of a potential issue. Forensic investigators and incident responders will find them invaluable. 

This is where a good log management can be helpful. In the case of security incidents, these log management systems can also include search and correlation tools. While there are many log management solutions, many organizations are moving to something called security information and event management (SIEM). SIEM software, however, is not simply a log management solution. SIEM software is used to correlate and analyze security alerts and better visualize your data. 

The advantage to using SIEM is being able to pill a lot of data together so you can get broader picture of what is happening across the network. 

# Knowledge Check

WAF: Uses a set of rules to detect and block requests and responses.
DPI: Evaluates the contents of a packet that is going through a checkpoint.
Stateful Filtering: Tracks the status of active connections and uses this information to determine which network packets to allow through the firewall.
Packet Filtering: Manages outgoing and incoming packets and allows them to pass or halt based on the IP addresses, protocols, and ports.

# Flashcards

What monitors network traffic and parse through it to identify packets that contain possibly malicious content?
A: Snort
What is a procedure?
A: The actual implementation of the standard.

What is a firewall?
A: System or software that allows blocking, rejecting, or allowing network traffic.

What is a threat?
A: An entity likely to cause damage or loss to an organization.

What is a risk?
A: The measurable potential (probability) for loss or damage.

What is the security information and event management (SIEM)?
A: A log management solution used to correlate and analyze security alerts.

What is unified threat management (UTM)?
A: Next-generation firewall device that may include intrusion detection system (IDS), anti-malware, and other security functions.

What is the security triad?
A: Three essential security properties: confidentiality, integrity, availability.

What is a security policy?
A: A high-level statement of the security objectives of an organization.

# Footprinting and Reconnaissance
## Open Source Intelligence
Provides details about your target. If you are doing red teaming stuff, you may need to locate as much information as you can so you know not only what your attack surface looks like but possible ways in. Additionally, you can find a lot of information about individuals within an organization. This is useful for social engineering attacks – having contacts to go after is essential.

The second reason is that organizations aren’t always aware of the amount of information they are leaking. As noted earlier, attackers can find footholds, as well as potential human targets for social engineering attacks. 

## Companies
There are several starting points when it comes to acquiring open sources intelligence about your target. The first is to look at the company overall. Youll want to gather information about locations the company’s has. 

## EDGAR
Public companies are required to provide information about themselves. There are resources you can use to look up that information. In the process, you may gather information about a company’s organizational structure. The organizational structure can tell you who has what position, so when you are working on sending out email messages to gather additional information later, you know who they should appear to be from. You can select the holder of an appropriate position. 

The Securities and Exchange Commission (SEC)  has a database that stores all public filings associated with a company. The Electronic Data Gathering, Analysis, and Retrieval (EDGAR) system can be used to look up public filings such as the annual report in the form 10-K. Additionally, the quarterly reports, 10-Qs, are also submitted to EDGAR and stored there. These reports provide details about a company’s finances. The 11-K, a form including details about employee stock option plans, is also filed with EDGAR. Accessing EDGAR is as easy as going to EDGAR at the SEC website. 

One of the most useful forms you can fin in EDGAR is Schedule 14A on SEC site, which is a proxy statement and will include the annual report to the shareholders, which may include a lot of useful information for you. 

## Domain Registrars
EDGAR is only for public companies. Not every company is public. Another source of information, related to the internet itself, is the domain registrars. You wont get the same sort of information from the domain registrars as you would from EDGAR, but its still sometimes a decent source of information. For a start, you can get the address of what is probably the company’s headquarters.

This is not a guarantee, however. As mentioned, companies are starting to hide information provided to the registrars. Information is hidden behind the registrar. When you ask for information, you will get what the registrar has been asked to present and not necessarily the real details. 

Before we get too far down this road, though, its probably useful for you to understand how the internet is governed when it comes to domains and addresses. First, there is the Internet Corporation for Assigned Names and Numbers (ICANN). Underneath ICANN is the Internet Assigned Numbers Authority (IANA), which is responsible for managing IP addresses, ports, protocols, and other essential numbers associated with the functioning of the internet. 

In addition to ICANN, responsible for names and numbering, are the domain registrars. These organizations store information about addresses they are responsible for as well as contacts. There was a time when registering a domain and other data went through a single entity. Now, though, there are several companies that can perform registrant functions. 

To grab information out of the regional Internet registry (RIR), you would use the whois program. This is a program that can be used on the command line on most Unix-like systems, including Linux and macOS. There are also websites that have implementations of whois if you don’t have a Unix-like system handy.

## Regional Internet Registries
Not all the useful information is stored with he domain registrars. There is other data that is important to be kept. Earlier, we discussed IANA. While the IANA server provided information about domain registrars, its purpose has long been to be central clearinghouse for addresses. This includes not only port numbers for well-known services but also IP addresses, based on need, to the RIRs. The RIRs then hand them out to organisations that fall into their geographic region.

There are five RIRs around the world. They are based in different geographic regions, and an organization would refer to the RIR where they are located for things like IP addresses. The RIRs are the geographic areas they are responsible for are listed here:
-	African Network Information Center (AfriNIC): Africa
-	American Registry for Internet Numbers (ARIN): United States and Canada, as well as Antarctica and parts of the Caribbean.
-	Asia Pacific Network Information Centre (APNIC): Asia, Australia, New Zealand, and neighboring countries.
-	Latin America and Caribbean Network Information Centre (LACNIC): Latin America and parts of the Caribbean.
-	Reseaux IP Europeens Network Coordination Centre (RIPE NCC): Europe, Russia, Greenland, the Middle East, and parts of Central Asia.

All of these RIRs have their own databases that can queried using whois, just as we used whois to query information from the domain registrars. Typically,, you would use whois against the RIRs to find out who owns a particular IP address. 

## People
Use OSINT tools like theharvester.

## Social Networking
Getting information via social media lol.
## Username Search.
Sherlock or maigret.

## LinkedIN
Social media but for work.

# Knowledge Check
Click to select regional Internet registries (RIRs):
-	AfriNIC
-	LACNIC
-	ARIN
-	RIPE NCC

# Domain Name System
DNS is a tiered system, and its tiered in a couple of ways. First in the Fully Qualified Domain Names (FQDNs) we use. An example to demonstrate: www.labs.domain.com is an FQDN because it refers to a specific host or system. It’s best to read FQDN from right to left, because that’s how DNS will read it when it comes time to resolving the FQDN to an IP address.

In the beginning were the top-level domains (TLDs), and they were .com, .org, and .edu, as well as the ones for the different counties (.uk, .au, .ca, .sk, .us, and so on). Later, many more were added, but they are all still TLDs. 

Second-level domains are where we start adding in organizations. The TLDs belong to the internet at large, so to speak. They have organizations that manage them, but they don’t “belong” to any one organization, at least not in the way the second-level domains can be said to. In our example, the second-level domain would be ‘domain’. 

Under second-level domains are subdomains. Every domain can have as many levels of subdomains as they are willing to manage. 

## Name Lookups
When you visit a website, you enter something called a Uniform Resource Locater (URL). The URL consists, commonly, of two parts. The first is the Uniform Resource Identifier (URI). This is the protocol used (e.g., http:// or ftp://). Following the URI is the FQDN. Your browser will issue a request to the operating system to open a connection to the FQDN at the default port indicated by the URI.

Before the connection can be opened, the system needs to have an IP address to put into the layer 3 headers. So, it issues a name resolution request. Each computer will have at least one name resolver configured. The name resolver is the system your computer goes to accomplish the name resolution. 

The name resolver for TCP/IP networks is a DNS server, though other network protocols will use other name services. It takes in DNS requests and resolves them, based on what is being asked. Typically, the name resolver you will have configured will be what is called a caching name server. This means it gets requests from endpoints, resolves them, and caches the results for efficiency. This is distinct from what is known as authoritative server, which holds the records for a given domain. So, the first DNS request is the one from your system to the caching server, wherever it happens to be located.

We start with the request labeled A. This goes to the name resolver labeled Caching DNS. The caching DNS server checks its cache and sees that it has no IP address stored, so it begins something called a recursive name query or recursive name resolution. It’s called recursive because it will end up with multiple requests that keep getting narrower until we end up with what we want. The caching server will need to start with the TLD. It will have a hints file, indicating the IP addresses for the root name servers. For our example, the caching server will need to identify the server to use for the .com TLD. Once it has identified the server it needs to send a request to, request B goes out, asking the root server for the IP address of the name server for the domain.com domain.

The root server has the name server details for all the domains that fall under the TLD it is responsible for. The root server will reply to our caching server with the IP address for the name server for domain.com. When we did the whois lookups earlier, at the end of a whois lookup on a domain will be the name servers for that domain, since the name servers are stored with the domain. This, though, is why what we are doing is called a recursive query. We cant just ask the root server for the IP address of the hostname, so we have to ask it for a pointer to who to ask next. 

Request C is the DNS request asking the authoritative name server for domain.com about labs.domain.com. Since labs.domain.com is separate from domain.com, what our caching server gets back is another name server. We are now at the point where the FQDN is being asked for. Request D goes out asking for the IP address of www.labs.domain.com. The authoritative server, which is the one we are asking because it has the authoritative information about that domain, responds with the IP address. It may actually respond with multiple IP addresses, but for our purposes, were going to just say it comes back with a single IP. Once the caching server has the IP, it sends the response back to our system, which can then issue request E, which isn’t a DNS request but a connection request to the web server.

While DNS stores mappings between FQDNs and IP addresses, those are not the only data mappings that are stored. Some of the different record types you can and may want to look up include:
-	A: An A record is an address record and it converts an FQDN to an IP address.
-	AAAA: An AAAA record converts an FQDN to an IPv6 address.
-	MX: Every domain has a mail exchanger record, used to indicate the host that email should be sent to for that domain.
-	NS: The name server records are the FQDNs and IP addresses of the authoritative name servers for that domain.
-	SOA: The start of authority record holds information about the zone, including the serial number, indicating when zone information has changed last.
-	CNAME: A canonical name is an alias for an FQDN. This maps one hostname to another hostname or FQDN. The CNAME may refer to specifically a hostname since the domain name may already be assumed if its in the same domain.
-	PTR: A pinter from an IP address to an FQDN. Unlike an A record, this is not necessary, but its considered useful. An FQDN always has to map to an IP address but an IP address does not have to map to a hostname. Often multiple FQDNs may map to a single IP address.

# WOW THAT’S A LOT OF INFO LETS REVIEW!

Example:
```
https://www.labs.domain.com
```

Fully Qualified Domain Names (FQDNs): `www.labs.domain.com`
Top-Level Domains (TLDs): `.com`
Scheme (part of URL and thus URI): https://
Uniform Resource Locater: `https://www.labs.domain.com`
DNS: Resolves IP address to domain names and vice versa. 

## Using Host (DNS Lookup Using host)
Perhaps the easiest tool to use is host. This is a program that you will find on most Unix-like systems, including Linux systems. You can pass the hostname you want the IP address for to host and you will get a response. 

In addition to just a straightforward lookup of an IP address, we can use a different server than the one that is defined as our resolver. 

## Using nslookup
Another tool that can be used is nslookup. This can be used just like the program host, meaning you can just run nslookup www.example.com and get a response. An advantage to nslookup, however, is that you can issue many requests without having to keep running nslookup. When you run nslookup without any parameters, you will be placed into an nslookup shell, where you are interacting with the program, issuing requests. 

DNS supports multiple resource records, though the most common is the address (A) record. When you see set type=ns, im telling nslookup to issue subsequent requests asking for name server (NS) records. This will tell us the authoritative name servers for the given domain. Once I had the list of NSs, I was able to set the server I was asking to one of the NSs. What this means is that instead of going to my caching server, nslookup is going to issue a DNS request directly to the authoritative server, which wouldn’t have to do any recursive search since it has the information being requested. 

## Using dig
The program dig is another utility that can be used for name resolutions. It also supports the same things we have been doing, meaning we can indicate a different name server and also request different resource records.

Using dig, we can do exactly what we did earlier with host and nslookup. On the command line, you indicate the resource record you want. In our command line (dig mx wiley.com @car-ibextdns-01.wiley.com), mx is the resource record being requested, but it could just as easily be A or NS. It could also be PTR, if we wanted to get back an IP address from an FQDN. After the record type is the request. Since we are looking for a mail exchanger record, this would be a domain name, though you could issue an FQDN here, and you would get the mail exchanger records for the last domain that’s part of the FQDN. Finally, we indicate the server to ask using the @ sign.

## Zone Transfers
Issuing single requests is fine, but it assumes you know some information. In most cases, applications are asking for the information about IP addresses from FQDNs so the application can function correctly. In our cases, as ethical hackers, we are sometimes looking for all the hostnames that belong to a domain. This can be done using something called `zone transfer`. A zone transfer is legitimately used between multiple authoritative server for a domain and then multiple secondary servers. The secondary servers would issue a zone transfer request to the primary and update their records accordingly.

We can use that capability, theoretically, to request all the records in a domain. Because of this capability, though, two things have happened. First, most domains you will run across wont allow zone transfers from anyone other than the secondary NSs that have been configured. Second, many companies use something called `split DNS`. Split DNS is where the outside world is given an authoritative server address to use for externally resolvable hosts, like the web server and the mail server. Any system inside the enterprise network would use the company resolver, which would be configured as authoritative for the corporate domain. This means it can have many other systems that are not known or available to the outside world but that internal systems can resolve and connect to.  

To issue a zone transfer request, you can use the utilities we’ve already been using, though there are others. If you wanted to attempt a zone transfer using dig, for instance, the request type would be axfr. 

## Brute Force
As zone transfers are generally disallowed, you may have to rely on less elegant solutions to gather information about your target. Fortunately, there are some tools that may be of help here. One is `dnsrecon`, which can be used to extract some of the common resource record in DNS. Additionally, it can be used to identity hostnames as a result of repeated requests based on a world list provided to the program. 

## Passive DNS
In practice, there are two different phases of reconnaissance. While there is a lot of focus on gathering information to launch attacks, there is a lot of reconnaissance that happens after exploitation as well. You can perform reconnaissance from the outside as well as from the inside. Once you are on the inside, some of this gets a little easier, or at least we open some other doors for reconnaissance. A technique of using cached DNS entries on a local system is called `passive DNS reconnaissance`.

Each time you perform a DNS lookup on some systems, the result will be cached locally. This caching of the address saves having to send a network request the next time you want to visit the same host. The length of time the entry will be cached is set by the time to live field in the DNS entry. This begins with the start of authority (SOA) record. This indicates when the domain record itself expires. Effectively, this tells anyone looking for information about the domain when they need to check again to see who the authoritative domain name servers are. There are NS records associated with every domain indicating what servers to ask for answers about that domain. These authoritative servers should always be asked unless a record is cached locally, whether directly on thee client requesting the information or the local caching serve the client is asking.

In addition to the SOA record providing the timeout length for the domain itself, meaning the length of time you can rely on the name servers being valid before needing to check again, each individual record stored in DNS can have a time to live (TTL) value. This indicates how long any system can cache the result before checking again with the authoritative DNS server to ensure the value hasn’t changed. According to the specification for DNS, you don’t wait until the very end of the lifetime of an entry but instead use some value that is less than the full TTL. The TTL does provide guidance, though, on how long to hold on to a value in your local cache. 

Windows systems will cache values, and you can dump the cache on them, as you see in the partial dump that follows here. To dump cache on a Windows system, you would use command-line access, either the old command line, or using PowerShell, you would just run `ipconfig /displaydns`. On Linux systems, you can get the same information only if your system is running a caching server. This may be a program like `dnsmasq`, which does DNS forwarding, or it could be the `nscd` service, which is the name server caching daemon.

If you are doing external reconnaissance, this technique is unlikely to be of much use to you. Once you gain access to the inside of the network, though, you want to know all of the systems and IP addresses. From the outside, you can query open sources for details about address blocks that may be owned by the organization. On the inside of the network, they are probably using private addresses. There is no record anywhere of the blocks being used, unless you happen to get access to a network management system that records all the address blocks. Instead, what you can do is dump the DNS cache on a system you have access to. What you will get is not only hostnames but also the IP addresses that resolves to those hostnames. 

If you see a lot of entries for the domain owned by the company in thee cache dump, you may well be seeing internal DNS records. Another way you may know you have internal addresses is if you see something ends in `.local.`. This is a top-level domain that cant be used across the internet, so it is sometimes used as a top-level domain (the last part of the fully qualified domain name that includes the hostname and the domain name) for the internal DNS implementations.

 It is common for companies to use an implementation called `split DNS` where there is one server from the outside world, with a limited number of records. Typically, youd have FQDNs for any system that exposes essential services to the outside world. On top of the external DNS, there is probably an internal DNS. This is where all the systems inside the network get registered so you can use FQDNs rather than IP addresses. Your own system on an enterprise network may register with the DNS server so someone trying to get to your system would just refer to the FQDN of your system and be able to resolve that FQDN to an IP address. 

# Knowledge Check

Indicate if each of the given statements about a domain name system is true or fales:
-	It is a tiered and decentralized naming system for computers, services, or other resources connected to the internet.
-	It translates IP addresses to names and back that are available on the private network.
-	It provides various information with domain names assigned to each of the participating entities.
-	It defines the DHCP protocol as part of  the Internet Protocol Suite.

T, F, T, F

# Passive Reconnaissance

There is a lot of information that can be collected in a passive manner. For example, watching the network headers as they go by, from the layer 3 headers to application headers, can turn up some interesting information. While it can be time-consuming to capture packets and try to read through them manually, there is a program that will do a lot of that work for us. The program is `p0f`, and it will sit and watch network traffic as it presses by interface, making observations as the traffic passes. Unfortunately, p0f isn’t as useful as it once was. The reason for that has nothing to do with p0f but more to do with the face that web servers are generally encrypting traffic by default, which means p0f cant watch the HTTP headers, identifying the server and other useful information.

Very little what you see here is anything you wouldn’t be able to determine yourself if you knew how to read packet headers. The packet capture and analysis program `Wireshark` could provide much of this information. Some of the interesting bits, though, include identifying system uptime. This is the uptime on systems on my local network, so it’s less interesting, perhaps, than it would be if we could so easily identity uptime on remote systems. 

One tool you can use to quickly look up information from your web browser is `Recon`. This is a plugin for web browsers like Firefox and Chrome. When you activate it, a window appears and allows you to search for information quickly. While it isn’t strictly passive reconnaissance, it does give you quick access to tools like whois lookups, Google dorks, and other important searches. 

(I checked out Recon. Its nothing special compared to alternative OSINT tools.)

# Website Intelligence

Starting from the bottom of the stack, we can look at what the web server is as well as the operating system. One way to get some of this information is just to connect to the web server and issue a request to it. In the following code, you can see the HTTP headers returned from a request to a website. While we don’t get the actual web server name, we do get some interesting information (yawn).

There is actually an easier way to do this – use netcraft.com – which will give hosting history for websites. This will provide the owner of the netblock that contains the IP address. It will also tell you the operating system the web server runs on. 

JUST USE NMAP?

Use Wappalyzer extension of Firefox or Chrome. This will provide you lots of information such as server, programming frameworks, ad networks, and tracking technology. (its legit). 

There are other ways you can dig into web pages and the technologies used. One of them is Firebox. Its available on Firefox, though there is also Firebug Lite that’s available for chrome. 

You can mirror websites using stuff like HTTrack. Or you can just write your own code and accomplish the same thing in less than 30 lines lol.

# Technology Intelligence 

## Google Hacking

Google hacking is an important skill to have. It will improve the search response, saving you a lot of time clicking through pages that aren’t especially valuable. The Google hacking techniques will help you to identify technology and vulnerabilities. In addition to Google hacking techniques, there is the Google hacking database, which is a collection of Google dorks that have been identified by someone as a way to search for a number of things. A dork is a string using Google keywords, designed to search for useful responses. 

First, the Google keywords. If you’ve been using search engines for a long time, you may be familiar with the use of quotation marks and Boolean terms to help ensure that you are getting the right strings in your responses. In addition to those, Google uses positional keywords. You may, for instance, want to look only in the URL for a particular string. To search in the URL, you would use `inurl` as in the example, `inurl:index`. This example would find pages that included the word index anywhere in the URL. This might typically be a page like index.html, index.php, or index.jsp. If you wanted to ignore the URL and only search in the text, you could use the keyword `intext`.

Since you are working for an organization, you have one domain or maybe a small handful of domains. This means you will, at some point, want to search only within those domains. To do that, you can use the `site` keyword. You may also want to limit your results to a single filetype, such as a portable document format (PDF) file or a spreadsheet. To limit your results to just on filetype, you would use the `filetype` keyword.

A great place to look for examples of useful Google dorks is the Google Hacking Database (exploit-db.com). The Google Hacking Database (GHDB) stores search terms in several categories, including footholds, vulnerable files, error messages, and sensitive directories. Creating these useful search strings requires that you know not only about the Google hacking keywords but also about what you are looking for.

Spending time at the GHDB can provide you with a lot of ammunition for looking for possible issues within your target. Some of this will be blind, if you have no idea what to expect within your target. To make sure you are only searching within your target, of course, you would need to add site: and the domain name to your search parameters.

## Internet of Things (IoT)
The IoT is made up of devices that may have little tot no input or output capabilities, at least from a traditional standpoint. If a device can run general applications and also has a keyboard and a screen, such as a computer, tablet, or smartphone, its not part of the IoT. Many other devices, like network-connected thermostats, light bulbs, fans, refrigerators, and a number of other essentially single-purpose devices, are IoT devices. 

These devices can be useful when it comes to infiltrating a system. Malware like Satori can infect multiple IoT devices, and once infected, those devices can be used to attack other systems. They may also be good starting points into the enterprise network, depending on the device. This is another area where search engines, though, can be helpful to us. Shodan (www.shodan.io) is a search engine specifically for IoT devices. Shodan keeps track of a large number of devices along with vendors, device types, and capabilities.

Shodan also requires understanding your target and what can be used to identity these devices. 

# Knowledge Check
Indicate if each of the given statements about Google hacking is true or false:

-	It improves the search responses, saving users a lot of time clicking through pages that aren’t especially valuable.
-	It is used to identify security vulnerabilities in non-web-based applications and gather information for collective targets. 
-	It discovers error messages disclosing sensitive information and files containing credentials. 
-	It includes GHDB, which is a collection of Google APIs identified by someone as a way to search for several things.
-	A dork is a string using Google keywords designed to search for useful responses.

T, F, T, F, T

# Flashcards
What is a Domain Name System (DNS)?: Used to resolved hostnames to IP addresses and vice versa, as well as obtain other information associated with a domain.
What is reconnaissance?: Identifying information about the target before attacking.
What is the Electronic Data Gathering Analysis, and Retrieval (EDGAR) system?: Used to store information about public companies.
What is whois?: A program used to request information about domains and addresses.
What is a regional Internet registry (RIR)?: An organization that manages IP addressing in one of five regions around the world.
What is nslookup?: A utility used to query Domain Name System (DNS) servers.
What is zone transfer?: A Domain Name System (DNS) request to pull all records from a domain.
What is Google hacking?: Using advanced operators to narrow search responses.
What is footprinting?: Identifying the size and scope of the target network.
What is brute force?: Applying a strategy of attempting every possible input to identify the correct one (such as passwords).
What is Internet Corporation for Assigned Names and Numbers (ICANN)?: An organization that assigns names and numbers across the internet.
What is Shodan?: A website that can be used to locate the Internet of Things (IoT) devices around the world.

# Scanning Networks
# Ping Sweeps
Rather than blindly throwing attacks at addresses spaces you’ve identified, you may want to identity systems that are responsive within those address spaces. Responsive means that when network messages are sent to them, they provide an appropriate response to the messages. This means you can identity systems that are alive before you start aiming attacks or probes at them. One way of determining system that are alive is to perform a ping sweep. A ping sweep is when you send ping messages to every system on the network. The ping is an ICMP echo request, which is a common message to be sent.

## Using fping
While there are many tools that can perform a ping sweep, one of the common of is `fping`. This is a tool designed to send ICMP echo requests to multiple systems. Example parameters used with fping are `aeg`, which means fping shows hosts that are alive, shows elapsed time, and generates a list of targets from an address block.

Since the `e` parameter is added to fping, it provies the elapsed time. 

## Using MegaPing
Another tool that can perform a ping sweep, as well as several other functions, is MegaPing. MegaPing is a GUI-based tool that runs on Windows. It incorporates several functions into a single interface. The ping sweep can be accomplished using the IP Scanner tool, which you would select from the list on the left side. 

# Knowledge Check
MegaPing: Runs under Windows and incorporates multiple functions into a single interface.

MegaPing: Performs ping sweep using the IP Scanner tool.

Fping: Shows hosts that are alive, shows elapsed time, and generates a list of targets from an address block.

Fping: Sends ICMP echo requests to multiple systems. 


# Port Scanning
A port is a construct within the operating system’s network stack. When an application has network service functionality, it binds to a port, meaning it reserves the port and registers the application to get messages that come in on that port. Any communication received by the system addressed to one of the ports get forwarded to the application that is registered to that port. When there is an application listening on a port, it is considered to be open. Remember that ports exist at the Transport layer, so applications determine whether they are going to use UDP or TCP as the protocol to listen on. 

TCP, as you should know, uses a three-way handshake to initiate connections. To accomplish the handshake, TCP makes use of flag settings, which means there is a set of bits that are enabled or disabled to set or unset the flags. The three-way handshake uses the SYN and ACK flags to complete the connection process. Other flags, such as URG, PSH, and FIN, are used for other purposes, and the RST flag is used to let other systems know to cease communications on the destination port in the received message. Port scanners make use of the known rules in the protocol to make determinations about whether a port is open or not.

Open ports should respond to a SYN message with a SYN/ACK. Closed ports should respond to a SYN message with a RST message.

UDP is another story altogether. There is no defined way of beginning a conversation from the standpoint of the protocol. UDP messages are sent from a client to a server, and its up to the server how it responds. The operating systems network stack has no role other than to pass the message up to the application once the Transport layer headers have been processed. This can be a challenge for port scanners. The reason is that with no defined response, its hard to determine whether a lack of response is because of a closed port or just because the application didn’t receive what it expected. 

Since there is no defined response, port scanners have to make a best guess. If there is no response to a probe message, port scanners don’t assume the port is closed because it may not be. Not only may the application just not have responded, but its possible the UDP message was lost in transmission, since nothing is the protocol ensures that it gets from end to end. Because either is possible, the probe messages will be re-sent. There is a delay of some small period of time between each message. Sending multiple messages with delays between them can cause significant UDP port scans to take quite a  bit more time than a TCP scan.

## NMAP
The de facto port scanner is `nmap`, short for network mapper. This is a program that has been around since 1997 and has become so commonly used that other port scanners implement the same command-line parameters because they are so well-known. It isn’t just a port scanner; its primary role and other functions are just extensions of the core purpose of nmap.

NMAP can perform UDP scans as well as multiple types of TCP scans when it comes to port scanning. In addition, nmap will detect operating system types, applications, and application versions. Perhaps more significantly, nmap supports running scripts. These scripts allow anyone to extend nmap’s functionality. The scripting engine, powered by the Lua programming language, has modules that scripts can be built on top of to make the job or probing systems much easier.

## TCP Scanning
As it’s the most detailed and complex type of scanning done, I’ll cover the different types of TCP scans that nmap can perform. First, we know that transport protocols use 2 bytes for the port number in their headers. This means there are 65,536 possible ports (0-65535). Scanning that many ports, especially considering that the vast majority of them aren’t used by listening applications, is very time consuming. To be efficient, nmap will scan only 1,000 ports by default, though you can specify any ports for nmap to scan that you would like. These 1,000 ports are the ones that are most likely to have a listening service.

There are many types of TCP scanning. One of the first ones to look at is the SYN scan. This sometimes called a half-open scan, because connections are left half open. NMAP will send a SYN message to the target. If the port is open, it responds with a SYN/ACK message, and nmap will respond to that with a RST message, indicating it doesn’t want to continue with the connection. If the port is closed, the target system will respond with its own RST message. SYN scan is used by adding the `-sS` parameter.

## UDP Scanning
UDP scanning is much more straightforward than TCP scanning. There are no options for UDP scanning. NMAP sends out UDP messages and then watches whatever responses may come back. The expectation is that if a port is closed, the system will respond with an ICMP port unreachable message. If a port is open, the service may respond with something or it may just not respond at all. 

## Port Scanning
Basically download nmap and try it out (lol). 

## Scripting
Add `--script=[script  name]`
Use `--script-help` for help.

## Zenmap
Nmap but with GUI. Use CLI nmap instead tbh.

## Masscan
Have you ever wanted to just pot scan the entire internet to identify all the web servers that responds (yes)? Of course, if you were going to do that, youd want to do it flat-out, as fast as you possibly can. According to masscan’s developer, Robert Graham, that was essentially the purpose for masscan. At its core, it’s a port scanner. It does some of the same things that nmap does. The difference is that it was developed to go as fast as your system and network connection you have will allow it to go.

Since nmap has become the de facto port scanner and people who are inclided to do port scans know how nmap works, masscan uses the same sorts of command-line parameters as nmap. Port scanning isn’t really fancy, when you come down to it. You tell the port scanner what ports you want to scan and the systems you want to scan. 

Masscan can be used with `--randomize-hosts`, which means that the IP addresses tested would not be in numerical order. Instead, the order will be randomized. The idea behind randomizing hosts is to potentially get around network monitoring tools. If you scan in order, it is fairly clear that a scan is happening. Randomizing scanning makes it a little less obvious what is happening. This may be especially true if you slow the rate down.

Masscan doesn’t just do port scanning, though, even really fast scanning. It can also do some information gathering, much like nmap can. You can request that masscan grab banners. This is done using the `--banners` parameter. 

## MegaPing
As noted earlier, MegaPing has a number of capabilities, including the ability to run port scans. These are not just run-of-the-mill scans, however. You’ll remember that nmap scans 1,000 ports by default. These are commonly used ports. You can certainly select other ports you want. One thing MegaPing provides us with that we don’t get with nmap is some preselected port collections. One of these is Hostile Ports, which are ports that are commonly misused as well as ports that may commonly be used by Trojan horse programs and other malicious software (malware).

## Metasplot
While Metasploit is known primarily for being an exploit framework, which you turn to when you want to start exploiting services, meaning you want to get unauthorized access to the service, there are thousands of modules available that are not exclusively about exploiting services. We can use Metasploit for port scanning. Just to give you a sense of the types of port scanning we can do, the following is a list of the modules, at the time of this writing, available in Metasploit. This was obtained using msfconsole, which is one of the ways you can access Metasploit over the command line.

# Knowledge Check
`masscan` is used to scan the entire internet to identify all of the web servers that respond. It can indicate at what rate users want to scan and perform very fast scans. While `Metasploit` is known primarily for being an exploit framework. It allows users to enter the mind of a hacker and use the same methods for probing and infiltrating networks and servers.

Indicate if each of the given statements about Zenmap is true or fales:
It is a multi-program, free, and open source application designed to make Nmap easier for beginners to use.

It performs a port scan and saves results in JavaScript Object Notation (JSON) form.

It has been the command-line interface (CLI) version of nmap for years and is suggested as an overlay for nmap.
It provides various advantages, namely interactive and graphical results viewing, comparison, convenience, discoverability, and so on.

T, F, F, T

# Vulnerability Scanning
You can start hunting and pecking at ports after doing a lot of research about vulnerabilities that may exist within those applications. You could also just find a lot of exploits and start throwing them at the applications on the open ports. This may be a simple way of checking to see if there are vulnerabilities. You just check all the exploits you can find against your target. There are a few issues with that approach, however. The first is that you may end up causing failures on your target systems where you may not mean to. Blind testing can lead to unexpected results, and one of your objectives, from an ethical standpoint, is to cause no harm.

It wouldn’t be very professional to tell your client that you’re just going to throw a lot of exploits at their system without any idea what the impact would be and that they may experience outages as a result. Your job is to control your testing – to be knowledgeable about what you are doing and what the possible outcomes are.

Another issue is that if you are engaged in a red team test where the target has no idea you are running attacks, you want to be sure they don’t detect you, or at least you want to do everything you can to avoid detection. Blindly running a lot of exploits against a lot of systems, including systems that may not even have the application that’s vulnerable, is going to be noisy, and if there is any detection capability, you will be caught. That means you will have failed. 

A better approach is to use a vulnerability scanner, which takes an intelligent approach to identifying potential vulnerabilities. A vulnerability scanner will identify open ports and listening applications and then determine what vulnerabilities may be possible based on those applications. The scanner will then run tests that have been defined for those vulnerabilities. The objective of a scanner is not to compromise a system; it is just to identify potential vulnerabilities.

This does not guarantee that what the scanner has identified is an exploitable vulnerability. It means that the scanner has found something it believes is a vulnerability based on interactions with the target system as compared with data the vulnerability scanner has. This is called a false positive. Any issues found by a vulnerability scanners needs to be verified manually. 

False Positive: The scanner has identified something it believes to be a vulnerability. After investigation, it turns out its not really a vulnerability. 

False Negative: The scanner has not identified a vulnerability. It later turns out that there was a vulnerability that the scanner missed.

True Positive: The scanner has identified a vulnerability that, after manual investigation, turns out to be a legitimate vulnerability. 

Ture Negative: The scanner has not identified a vulnerability, and there is not a vulnerability to identify.

The first vulnerability scanner was created in the 1990s by Dan Farmer and Wietse Veneema, known as Security Analysis Tool for Auditing Networks (SATAN).

## OpenVAS
SATAN was open source, meaning you could look at everything SATAN was doing and, if you felt like it, extend its functionality by adding modules yourself. 

Another opensource vulnerability scanner  in the early 2000s was Nessus. It was initially released in 1998 as a freely available vulnerability scanner and remained so until 2005 when the company, formed three years before, closed the source code, making all future development proprietary to the company. The existing source code for version 2 was open, however, and two separate projects were created, where the Nessus code for version 2, abandoned by the Nessus developers, was forked to create a basis for the new projects.

One of these forks was the Open Vulnerability Assessment System (OpenVAS). Initially, OpenVAS was the same as Nessus, as you’d expect. Over time, OpenVAS developed its own application architecture, using multiple tiers that Nessus hadn’t explicitly used. Nessus initially had a native application client to manage the scans, and OpenVAS continued to use the same native application. OpenVAS developed the Greenbone Security Assistant (GSA) as the user interface for OpenVAS. Today GSA is accessed through a web interface.

OpenVAS allows you to have multiple users, each of which may have different permissions. Some users may be able to create scans, while others may only be able to look at the scan results. Other users would be able to create users and administer the OpenVAS installation. In addition to users, OpenVAS supports roles. Permissions within the rooles can be altered, and now roles can be created. When you install OpenVAS, the admin user is created as part of the setup process, and a random password is generated.

## Setting Up Targets in OpenVAS
A scan in OpenVAS has many components. When you create a scan, you need a target or set of targets. Creating a target also requires some information. You need the set of IP addresses you want to run tests on. You can also exclude addresses from the set you are testing. You may do this to provide a network block in your target list, but you may also have fragile systems in the network block. Because of that, you may want to tell OpenVAS not to test that address.

One thing a vulnerability scanner like OpenVAS does is scan ports to determine which ones it should be focusing testing on. You can determine the range of ports you want to test. This can limit the amount of testing you do if you care only about testing against particular services. 

## Scan Configs in OpenVAS
The core of a scan is in the scan config. The scan config is the definition of what plugins are tested against the target. By default, there are eight scan configs defined in OpenVAS. You can see the number of network vulnerability tests (NVTs) that have been enabled in each config. The NVTs are categorized into families for organizational purposes. You can enable the entire family or just enable individual NVTs as you need to. 

## Scan Tasks
Scan configs are targets are necessary to create a scan task. You’ll be able to create the target as part of creating a scan task, and it will persist just as if you had gone to the target configuration separately. The scan config, though, has to be done ahead of time unless you want to use one of the prepackaged scan configs. 

## Nessus
Nessus is the parent of OpenVAS, which makes it worth looking at, especially to see how it has diverged from the path OpenVAS took. When you log in, youre taken to your list of scans, which will be empty at first. To start a scan, you would click the New button, which will take you to a list of the different scan policies that are available.

Like OpenVAS, Nessus uses Network Attack Scripting Language (NASL) scripts. They are stored with the rest of the Nessus installation. On Windows, the installation would be in the Program Files directory. On Linux, the files are stored in `/opt/nessus` with the plugins in `/opt/nessus/lib/plugins`. 

## Looking for Vulnerabilities with Metasploit
One example of a vulnerability scanner metaploit has is a module called Eternal Blue vulnerability. This is a vulnerability in the implementation of the Server Message Block (SMB) protocol that was discovered by the National Security Agency (NSA), which developed an exploit for it, which was released without the NSA’s approval by a group called the Shadow Brokers.

There are a large number of scanners available in Metasploit. Not all the scanners are directly related to the vulnerabilities. Search for the word ‘scanner’ in Metasploit will return around 619 results.

# Knowledge Check

True Positive: A legitimate attack that triggers to produce an alarm.

False Negative: No alarm is raised when an attack has taken place.

True Negative: An event when no attack has taken place and no detection has been made.

False Positive: An event signaling to produce an alarm when no attack has taken place.

# Packet Crafting and Manipulation
When you are sending data out over the network, there is a clear path it follows before exiting the network interface on your system. We’ve gone over this to a degree by talking about the Open Systems Interconnection (OSI) model. Let’s say that you are visiting a web page. You enter a URL into the address bar. Your browser takes the input and creates the HTTP request headers that are needed to send to the server. For simplicity, we’ll skip the encryption pieces and just talk about how the complete packet is put together.

The application makes a request of the operating system to open a connection to the server. This triggers the operating system to build a packet using information provided by the application. This includes the hostname or IP address as well as the port number. Unless otherwise provided, the port number will default to either 80 or 443, depending on whether the communication is HTTPS or HTTP. This information will allow the operating system to create the necessary headers for both TCP and IP, layers 4 and 3.


All of this is to say that the application initiates requests based on interaction from the user. It follows a clear path, and the information placed into the necessary headers for each protocol in coherent and easily traced back to the original source of the information. Sometimes though, you may need to send data that doesn’t follow a coherent path. It could be that you need to manipulate headers with data that wouldn’t normally be found in the header fields. Each header field is known size and is binary, which means you aren’t going to be sending a character instead if a number, for instance. Nothing in the network headers, looking at layers 4 and below for sure is data that would go through an ASCII decode to be converted to character data.

There are a number of tools that can be used to craft or otherwise manipulate the header data. Some of these are designed for the sole purpose of creating packets that would look the way you want them to look. This may be a tool like packETH,which uses a GUI to let you set the fields. Others have other purposes that allow you to interact with the target system in a way that you may not otherwise be able to do without writing your own program. A tool like `hping` will let you build a packet based on the command-line parameters. Using a tool like hping, you could assess the response from the system. Finally, you may want to mangle the packet using a set of rules, which would put the operating system’s network stack to the test, to see if it can handle poorly constructed packets.

## HPING
The program `hping` is considered by the developer to be the Swiss Army knife of TCP/IP packets. You could use it as a straightforward ping program, sending ICMP echo requests. Since hping is primarily a packet crafting program, allowing you to initiate connections using different protocols with the header settings you want, the default mode may not work well for you. By default, if you don’t specify anything other than the target host or IP address, hping will send messages to port 0 on your targe with a varying source address. Address 0 is essentially an invalid destination since it is considered reserved and has no purpose. You shouldn’t get any response from the system you are sending traffic to. If you do, the target host is really violating the protocol. While hping uses TCP for this port 0 is invalid for both UDP and TCP.

While you can use hping as a replacement for the ping program, by calling it with the -1 parameter, meaning you are using ICMP mode, you can also create connections to specific ports.  You will get the same behavior you would get with the ping program, meaning you will be getting thee “aliveness” of the system and the round-trip time. You will get something even more detailed, though, since you will know whether a particular service is up and running. This may be useful if you are doing testing against an application. You want to know when the service fails. You will get a lot of detail from the response in addition to the round-trip time. 

`hping` will provide you with all the flags that are set in the response. This includes the SYN and ACK flags as well as thee don’t fragment bit, indicated by the DF in the response. 

In addition to ICMP and TCP, you can send UDP messages. There are fewer paramets used to send UDP messages because of the limited number of options available in the UDP headers. We can, though, use `hping` to perform a port scan. We can scan a range of UDP ports by using the `--scan` (or -8) parameter. 

## PackETH
Where hping used command-line parameters, packETH takes a GUI approach to being able to set all the parameters. The sets of headers vary, depending on the protocols selected, and each of the lower-layer headers indicate the next protocol, meaning the next set of headers. When you select which protocols you are using, packETH will adjust to provide all of the header fields for the protocol you have selected. You will also see where IP is selected as the next protocol in the layer 2 header. You cant see the layer 2 header in this screen capture, but you would be able to set addresses, determine what version of the layer 2 protocol you are using, and also add in 802.1q fields, which provides a tag field to indicate which virtual LAN (VLAN) the frame should be on.

While you can create packets following known and understood fields, you can also create your own packets. Your layer 2 headers have to be set with MAC addresses in the source and destination so there is somewhere for the frame to go, but beyond that, you can do whatever you like by selecting User defined payload in figure. 

## Fragroute
`fragroute` is a program used to mangle packets before they are sent to a target you specify. It works by making adjustments to the routing table so all messages going to the target are sent through the fragroute application first. To make fragroute work, you need to create a configuration file. This configuration file has directtives telling fragroute how to handle packets that pass through the application. In the following code listing, you can see a configuration file with a handful of directives that are guaranteed to create really messed-up network traffic.

The directives here tell fragroute to do a number of things to packets. The first thing is to delay random packets by 1 millisecond. Next, there is a 30 percent chance of duplicating the last packet. The `ip_chaff` line adds duplicate packets into the queue. When messages are sent out, they have a maximum transmission unit (MTU) size that is dictated by the data link protocols. 

# Knowledge Check
PackETH: Allows user to adjust to provide all the header fields for the protocol they have selected.

Hping: Allows users to initiate connections using different protocols with the header settings they want.

Fragroute: Used to deform packets before they are sent to a specified target.

# Evasion Techniques 
Common evasion techniques:
-	Hide/Obscure the Data: You could use encryption or obfuscation to disguise what you are doing. Encrypted traffic cant be investigated without violating the end-to-end nature of encryption. The goal with encryption is that the message is encrypted from the sender to the recipient, without being decrypted at waypoints in between. You could also encode the data using various encoding techniques. Including URL encoding, which replaces characters with the hexadecimal value of their ASCII code. 
-	Alterations: Intrusion detection/protection systems in particular will often use something called a signature. In the case of malware, this may be a cryptographic hash value that can be compared against a database of known malware. If there is a match of the hash, the messages can get dropped. When it comes to a cryptographic hash, though, the change of a single character in the file contents will field a completely different hash value, meaning whatever you are doing wont get detected. This strategy is commonly called polymorphisms, from polymorph, meaning many shapes or forms.
-	Fragmentation: Fragmentation attacks can be used to evade network security mechanism simply because these devices, when they are inline, would take time to reassemble the message before the adversarial activity would be seen. You can use a tool like fragroute to help with fragmentation.
-	Overlaps: When messages are fragmented, it may happen at either the Network layer or the Transport layer, as you saw from looking at fragroute. When the messages need to be reassembled, all of the pieces need to be there and in a sane state so the puzzle can be fit back together. When using TCP, you can overlap sequence numbers.
-	Malformed Data: Protocols are sets of rules about how communications are expected to happen. If you violate those rules, you can get unexpected results. Even if you aren’t violating the rules but instead are taking advantage of loopholes, you can get some useful data. This is why nmap uses Xmas, FIN, and NUL scans. The behavior is unexpected, though not technically illegal from the standpoint of the protocol. 
-	Low and Slow: Fast scans can be easy to detect. Harder to detect are scans that are taking place over a long time frame.
-	Resource Consumption: It may be possible to get devices to fail open by consuming resources such as CPU or memory. 
-	Screen Blindness: In the case of IDS, the device or software will issue alerts. It is expected there will be someone looking at those alerts. If you can generate enormous volumes of alerts from traffic youdon’tt care about, you can cause they people looking at the alerts to go screen blind, meaning they just aren’t seeing the important details anymore because they are overwhelmed by what they are looking for.
-	Tunneling: A tunnel is a way of transmitting data inside something else. For example, the Generic Routing Encapsulation (GRE) protocol can create a  tunnel by taking packets and encapsulating them inside GRE packets. This makes it look like what is passing through is a GRE packet when there is really something in the payload.
## Evasion with nmap
Nmap has its own evasion built in, to a degree. This would be in regards to `-t` scans and how hardcore the scan goes.

You can also “blind” the defender to use a number of decoys by generating a lot of bogus traffic alongside the port can you actually care about. You do this by passing the `-D` flag.

You can use `--spoof-mac` followed by a MAC address or by a vendor to spoofy a mac address.

# Flashcards
What is a vulnerability?: A weakness in a piece of software or a configuration that could lead to exposure or exploitation.

What is ping sweep?: Using Internet Control Message Protocol (ICMP) echo requests to identify all responding hosts on a network.

What is port scanning?: Identifying open ports on target hosts.

What is nmap?: A utility used to scan for open ports.

What is thee SYN scan?: A port scanning technique targeting Transmission Control Protocol (TCP) ports by sending the SYN request.

What is Nessus?: A vulnerability scanner utilizing plug-ins, which are separate files, to handle the vulnerability checks.

What is evasion?: A technique of performing an action like port scanning in a way to avoid detection.

What is tunneling?: Encapsulating data inside of another protocol to get it from one endpoint to another.

What is an XMAS scan?: A method of port scanning that sends the FIN, PSH, and URG flags in a Transmission Control Protocol (TCP) header.

What is the Open Vulnerability Assessment System (OpenVAS)?: A vulnerability scanner forked from Nessus.

What is hping?: A utility used to craft a packet on the command line.

What is packet crafting?: Generating a packet that has fields set in a way specified by the attacker, which may include a payload in addition to headers.

What is MegaPing?: A tool that runs on Windows that can perform a number of reconnaissance tasks.

# Searching for Exploits 

`exploit-db.com`

Kali Linux has a repository of exploits available as well as a tool that can be used to search the repository from the command line.

Finding Exploits with `searchsploit`
Example, to search for exploits on OpenSSH, you could type:
```
searchsploit openssh
```

# System Compromise 

## Metasploit Modules

If there is a known exploit for a vulnerability available, it has likely found its way into Metasploit. This is a program that was originally developed as an exploit framework. The idea was to provide building blocks so exploits could quickly be developed by putting together a set of programming modules that could be used. Additionally, shellcodes and encoders are available to put into exploits being developed. 

Almost the entire lifecycle of a penetration test can be handled within Metasploit. As of the moment of this writing, there are more than 1,000 auxiliary modules, many of which are scanners that can be used for reconnaissance and enumeration. Using these modules, you can learn what the network looks like and what services are available. You can also import vulnerability scans from OpenVAS, Nessus, and of course, Nexpose, which is developed by the same company that is responsible for Metasploit. Once you have all of this information, though, you want to move to exploitation. There are currently over 2,200 exploit modules in Metasploit, though the number changes fairly regularly because of the popularity of the software and the development work by Rapid 7.

We’re going to start with `msfconsole` program in Kali Linux, which Metasploit is installed by default. You do need to set up the database that is used to store information about hosts, vulnerabilities, and any loot acquired. Below you can see starting up `msfconsole`, which is the command-line program used to interact with Metasploit.

```
Sudo msfconsole
```

Once `msfconsole` is started, we need to locate an exploit for a vulnerability that has been identified. To find an exploit, you simply search for it:

```
search eternalblue
```

There is more than one that we could use here, depending on what we want to accomplish. In this case, I want to get a shell on the remote system; the auxiliary module will allow us to execute a single command on the remote system, which would be the same as the one ending in `pseexec`. As a result, we’re going to use the exploit ending in `010_eternalblue`. This will give us a shell on the remote host. From that shell, we can start issuing commands, but more than just one, which the others would let us do.

Once we know what module we are using, we load it up using the `use` command in the `msfconsole`. Each module has a set of options that can or needs to be set. In some cases, the options will have defaults already set so you don’t need to do anything. The one parameter that will always need to be set is the one for the target. This will either `RHOST` or `RHOSTS`, depending on whether the module expects to have multiple targets. A scanner module, for example, will use `RHOSTS`, while an exploit module will generally have `RHOST` as the parameter name. 


## Exploit-DB
You can search `exploit-db.com` for exploits associated with vulnerabilities.


# Gathering Passwords

Once you have an exploited system, you will want to start gathering information on it. One type of information is the passwords on the system. There are a couple of ways to gather these passwords. In the preceding code listing, we got a Meterpreter shell on a target system. Using Meterpreter, we can gather information about the system so we know what we’re getting from password data. The command `sysinfo` will tell us the system name as well as the operating system. This tells us were going to be looking at LAN Manager hashes when we grab the passwords. We can do that using the `hashdump` command.  

The hashdump provides the username, the user identifier, and the hash value of the password. We’ll need that when it comes to cracking the password. 

This is not the only way we can grab password hashes. There is a module named `mimikatz` that can bee used. 

When we compromise a Linux system, we can’t use hashdump, but we still want to grab the passwords. Either we can get a shell directory from an exploit, or if we use a Meterpreter payload, we can drop to a shell. This is where we’d be able to access the passwords. In the following code, you can see dropping thee shell from Meterpreter. From there, we can just use `cat` to print the contents of the `etc/shadow` file. We do need to have root access to see  the contents of the shadow file. You can see by running `whoami`.

## Password Cracking

## John the Ripper
Offline password cracking tool. Can use wordlists. Incremental mode to try every possible combination of characters.

## Rainbow Tables
Rainbow tables are stored precomputed hashes. The rainbow table isn’t as straightforward as just a mapping between a hash and a password. The rainbow tables are stored in chains in order to limit the number of plaintext passwords stored. In some cases, the plain text can be inferred if it is not stored directly. There are many tools that can be used to look up passwords from these tables, but first we need the tables. The Rainbow Crack project has a tool to look up the password as well as a tool that will create the rainbow table. This creation tool isn’t used to generate hashes from wordlists. Instead, it will generate a hash from all possible password values within the constraints provided. 

## Kerberoasting
Kerberoasting is another type of password cracking attack that relies on getting access to a network. The name is based on the face that Active Directory authentication over a network uses a protocol called Kerberos. Kerberos, in turn, is named for the three-headed dog of Greek mythology who guarded the gates of the Underworld to prevent those there from leaving. 

To perform a Kerberoasting attack, you need to have compromised an account on the domain. The compromised user account will receive a TGT from the KDC when they are authenticated. This has been signed by the Kerberos ticket-granting ticket service account that is part of the AD design. The attacker, who has control of the compromised user account, wants to compromise a service on the network. They will request a service ticket for that service. A domain controller with the Active Directory infrastructure will create a TGS ticket, encrypting it with the service password, retrieved from the AD database. The only two entities that have the password that could decrypt the message at this point are the domain controller and the service itself.

The domain controller sends the ticket to the user, which is under the control of an attacker. The ticket gets sent to the service, which decrypts it to determine whether the user has been granted permission to the service. This ticket is in memory and can be extracted from there so it can be decrypted (or cracked) offline.

# Knowledge Check
-	Rainbow Table – Includes a collection of chains, where each chain is 16 bytes.
-	John the Ripper – Includes various password crackers into one package, auto-detects password hash types, and includes a customizable cracker.
-	Rainbow Tables – Makes use of the stored precomputed hashes.
-	John the Ripper – Supports both brute force and dictionary attacks.

# Living Off the Land
Making use of tools that are already available on the target system, such as PowerShell cmdlets.

-	Empire is a post-exploitation framework written in PowerShell, meaning this is a set of tools you would use after you have already exploited a system. Empire appears to no longer be support, though you can still grab the source code for it.
-	PowerSploit, another tool which is no longer actively maintained, also provides a number of cmdlets that include functions for code execution. 
-	Learn PowerShell noob.


# Malware

# Malware Types

## Virus

Not all malware is a virus, but all computer viruses are malware. A virus require user intervention to infect a system. The user has to do something to execute the virus. Once that happens, the virus will infect the system, possibly by injecting code into other programs, so when those programs run, the virus still retains control of the infected system.

A computer virus is said to have the same phases that a biological virus has. Viruses have dormant phases, where they are inactive, waiting for a trigger. The triggering phase is when the virus has been trigged by a user action or some other defined event. 

Viruses that wait for a specific time are sometimes called logic bombs. 

A virus may be memory resident. This means that when it infects a system, it remains in memory. This commonly means that it installs itself as part of the operating system, which means it loads into memory when the system boots and remains there until it shuts down. As they are always running, memory-resident viruses can scan, infect, and reinfect as needed. If it is nonresident, the virus has to be executed. 

One nonresident type of virus is a macro virus. This is one that executes as a script as part of a document. Word documents, for example, can include macros, which are short scripts that launch and are executed when the document is opened. This virus could be spread by attaching to the macro and then just sending the document around. Many other document formats support script execution, including the Portable Document Format (PDF), and all can be prone to this sort of virus. 

## Worm

A worm gets launched initially and all subsequent infections are a result of the worm moving from one system to another on its own. This is called self-propagation.

The important thing to keep in mind is that a worm propels itself. It doesn’t require any assistance from the user. This means that it has a way of connecting to remote systems and executing itself on those systems. This is likely a result of a network-facing vulnerability. 

Worm do not necessarily have to be executables. There have been worms that make use of email programs and contact lists to propagate. You may have an HTML email that has script embedded in it. Once the email client renders the HTML, it runs the script, and the script makes use of a vulnerability or some other poorly configured mechanism in the email client. The worm accesses the contact list and sends a copy of itself to everyone in the contact list. This also leads to the potential for reinfection where the malware may have been identified and removed. 

## Trojan

Trojans appear to be something legitimate, but is actually malware, usually a virus. The idea is to trick users into running the software. It could be considered a type of social engineering. 

## Botnet

A botnet can be part of the payload of a virus or a worm and could also be installed by a Trojan horse. When you hear the word botnet, its really referring to a botnet client that is being installed. The botnet is the entire collection of endpoints that have been infected with a particular family of malware. The botnet client is a small piece of software whose purpose is to connect back to command-and-control infrastructure (C&C or C2).

Some modern botnets use a decentralized model for managing the botnet. Rather than a client -server model, where the bot herder controls the entire network from the top, the decentralized botnet is entirely peer-to-peer. Messages may be sent from one endpoint directly to one another. All routing is done within the botnet, much like other peer-to-peer networks. The bot herder is still in control, but there is no infrastructure network to take down.

## Ransomware 

The goal of ransomware is to extort money from a victim. Ransomware is a program that encrypts a portion of a victim’s hard drive, where personal files are stored. In some cases, it may be important business documents. 

In recent years, ransomware has been on the rise. Attackers have discovered that its far more efficient to just demand money from victims than trying to steal information and utilize it.  Traditionally, threat groups have fallen into three categories:
-	Intelligence-Drive Groups: Sometimes this group is referred to as nation states. These are groups that are looking for information such as intellectual property from companies. This intellectual property is used to enhance the market capabilities of state-sponsored businesses.
-	Criminal Organizations: These are groups that are only in it for the money. They are businesses with employees and working hours. These employees may have roles and responsibilities just like you would in a job you had.
-	Hacktivists: There are people who are just trying to make waves. They have a point to make and will do a lot of different things to make it. This may be defacing web pages or performing distributed denial of service attacks.

## Dropper
A dropper is a type of malware that doesn’t commonly come alone. The dropper is used as a starting point. Once it is installed on your system, it starts grabbing other software to install. This may include backdoors, key loggers, botnet clients, Trojans, or other software that is useful to the attacker. 

## Fileless Malware
Typically, malware exists in files on disk. Perhaps the victim visits a website that is hosting malware embedded in the website pages. The malware then executes on the victim computer, leaving files behind that can be detected. Anti-malware programs often do file scanning as a way of detecting the malware to eradicate it. Malware developers recognize the threat posed by anti-malware programs. They may use different techniques to ensure the malware isn’t detected. One of these techniques is to never leave any artifacts on the file system. This results in something called fileless malware.

Fileless malware can make detection more challenging since there is no file that can be compared to a signature in anti-malware programs. It requires the detection of behaviors on the victim system, rather than file-based signatures. 

Persistence becomes a problem with fileless malware, since there is nothing that can be executed using a common startup process. However, there are ways to never write the malware to disk. One of these is to embed a PowerShell script into the Windows Registry and use that PowerShell script to pull other malware onto the victim server, executing it directly into memory. Additionally, the PowerShell script can make use of existing tools on the system to interact with the network for lateral movement. 

## Polymorphic Malware

Anti-malware software often uses signatures to identify malicious software. This could be something like cryptographic hash. Every instance of the file will generate the same cryptographic hash, no matter what system it is on, which makes it a reliable indicator of whether a file is malicious or not. This mean systems with up-to-date anti-malware databases will have the malware detected and removed. It is beneficial for the malware to not have the same cryptographic hash for every instance, so it doesn’t get detected and removed from the system. Custom or targeted malware may be compiled specifically for a target to ensure it looks different to the anti-malware software.

# Knowledge Check

-	Ransomware: Restricts access to a users device or its data until the victim pays the attacker to remove the restriction. 
-	Worm: Spreads from one device to another on its own, not by attaching itself to another file.
-	Dropper: Includes backdoors, key loggers, botnet clients, Trojans, or other software useful to the attacker.
-	Virus: Infects a target computer when an executable file is run.
-	Trojan horse: Downloads onto a computer disguised as a legitimate program.
-	Botnet: Includes a collection of endpoints that have been infected with a particular family of malware. 

# Sniffing

# Packet Capture

-	Process of acquiring network traffic that is addressed to systems other than your own.
-	Headers are the fields that are specific to the protocol. The provide instructions for how the protocol should behave.
-	Data that is being carried from one endpoint to another is called the payload.
-	Wireshark helps to make packet analysis much easier.

## tcpdump

-	Displays packet information on UNIX systems.
-	Default settings display IP header information.

## tshark

-	Included with Wireshark.
-	Similar to tcpdump.

## Wireshark

-	GUI based packet capture program.
-	Can view entire network stack in Wireshark.
-	Provides more details in the summary.
-	Doesn’t just give you a list of frames so you can see who was communicating with what but also provides full protocol decodes.
-	Supports filtering.

## Berkeley Packet Filter

-	Interface to the Data Link layer of a system.
-	Used across many systems and applications, including tcpdump, tshark, and Wireshark.

## Port Mirroring/Spanning
-	Any traffic that passes through one port would be mirrored to another report.

# Knowledge Check

-	Wireshark: A GUI-based packet capture program that provides a way to view the packets easily, moving around the complete capture.
-	tcpdump: A command-line program used to capture traffic and store that traffic in a file that can be opened later on.
-	Port mirroring: An approach to monitoring network traffic that involves forwarding a copy of each packet from one network switch to another.
-	tshark: A network protocol analyzer that capture packet data from a live network, or read packets from a previously saved capture file.
-	BPF: An interface to the Data Link layer of a system and consists of several primitives like host, ether, net, and proto.

# Detecting Sniffers

-	Look on the system that has the interface in promiscuous mode.
-	You will see PROMISC – this indicates the interface is in promiscuous mode, which means the interface is not doing any filtering of MAC addresses.
# Packet Analysis

# Knowledge Check

Indicate if each of the given statements about packet analysis is true or fales:

-	True: It uses a packet analyzer to intercept and log traffic that passes over a digital network or part of a network.
-	False: Expoit-DB is a very good packet analyzer that determines the information that isn’t directly provided.
-	False: Wireshark provides expert information that you can look at all at once from the View menu.
-	True: Wireshark can color frames where it identifies problems in the frame list based on rule sets.

# Spoofing Attacks 

-	Pretending to be a system that you aren’t. 
-	Spoofing attacks allow you to sit in the middle of a conversation between two endpoints.

## ARP Spoofing

-	Address Resolution Protocol has two stages. The first is the request, where a system knows an IP address but doesn’t know the corresponding MAC address. It sends an ARP request asking for the system with the IP address to respond with its MAC address.
-	In theory, anyone could respond to that request with their MAC address to get the requesting system to send the message to the attacker’s address.
-	Can make it even simpler by not waiting for the request to begin and just sending the reply.
## ARP Poisoning 

-	Same thing has ARP spoofing. You are poisoning the ARP cache on target systems with bad entires.

## DNS Spoofing

-	More targeted than an ARP spoofing.
-	Aren’t looking to capture traffic necessarily, instead we are looking tog et a target to come to systems under our controls for specific requests. 
-	Accomplished by intercepting DNS requests and providing responses to the requestor. 
-	Instead of providing legitimate responses, the attacker will use their own addresses.
-	Redirects to an IP address the attacker set up.

## Ettercap

Tool that can be used to capture requests, like DNS requests. 

## DHCP Starvation Attack
-	Attacker sends many DHCPDISCOVER messages to a DHCP server.
-	These messages are sent to the broadcast address 255.255.255.255. 
-	The DHCP server responds with an offer to the client. In this case, the server will keep sending offers, reserving the IP address for that client, expecting an acknowledgement that never comes.
-	At some point, the DHCP server runs out of IP addresses to provide to any legitimate endpoint (DoS).

## sslstrip 

-	Developed to grab SSL messages and trip the encryption from them. 
-	Outdated lol..

# Social Engineering
-	Reciprocity: People will generally feel like they want to or may be obliged to respond to a kindness or favor. You may feel this way if a company gives away free samples. If you get one of these free samples, you be inclined to feel like you should buy the product in response.
-	Commitment: If someone commits to something, either in writing or orally, they are more inclined to follow through on that commitment.
-	Social Proof: Think about social proof as peer influence. If you are someone else doing something, such as using  a product, you will see that it is acceptable to do that. You may therefore be more willing to try the product, or whatever it is you’ve seen.
-	Authority: If you’ve ever been pulled over by the police, you can recognize this one. Even if you haven’t, you may think back to being at school. In general, people are inclined to follow authority figures and do what they say and ask.
-	Liking: If you like someone, you may be more easily swayed by what they think or do.
-	Scarcity: The lack of availability of products increases their perceived value. The perception of increase value makes them more desirable.






