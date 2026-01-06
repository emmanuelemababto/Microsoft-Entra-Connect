On-Prem Active Directory Synchronization with Microsoft Entra ID

# Aim of the Lab
To configure Microsoft Entra Connect and synchronize on-premises Active Directory identities to Microsoft Entra ID, establishing a functional hybrid identity environment. 

# Tools Used

Windows Server 2019

Active Directory Domain Services (AD DS)

Microsoft Entra ID

Microsoft Entra Connect Sync

VirtualBox

# Steps Performed

Installed and configured Active Directory Domain Services on Windows Server.

Created a Microsoft Entra ID tenant and administrative account.

Installed Microsoft Entra Connect using Express Settings.

Authenticated to Microsoft Entra ID using a tenant-native Global Administrator account.

Connected Entra Connect to on-premises AD DS using Enterprise Administrator credentials.

Continued setup without matching UPN suffixes to verified domains for lab configuration.

Resolved configuration issues related to permissions, TLS 1.2, DNS, and system time synchronization.

Completed Entra Connect configuration and verified successful identity synchronization.

# Importance of the Lab

This lab demonstrates how hybrid identity is implemented in real environments and highlights the dependencies between Active Directory, Microsoft Entra ID, networking, authentication, and system configuration.


# Screenshoots


Creating a domain controller <img width="960" height="504" alt="creating a domain controler" src="https://github.com/user-attachments/assets/87812d41-fe95-473e-b978-925843aa3797" />

<img width="960" height="504" alt="domain controller is active" src="https://github.com/user-attachments/assets/719efce2-789a-4f79-92d8-0e505e1aa74e" />


<img width="960" height="504" alt="we need sigin in with a tenant id  inorder to setup entra connect" src="https://github.com/user-attachments/assets/f7608951-b9a8-405c-94a5-e5d1da21893c" />

<img width="960" height="504" alt="adding dc to enta-connect" src="https://github.com/user-attachments/assets/d3d29ad8-e7ba-4c68-be97-952663bbb3d0" />


<img width="960" height="504" alt="domain controller is active" src="https://github.com/user-attachments/assets/a59f77a4-7154-42ab-a5ba-1097b53159c7" />


<img width="960" height="504" alt="downloading entra connect" src="https://github.com/user-attachments/assets/08ddfb22-09a8-41ca-8264-a6782787920a" />



created  a new user called biilyjean <img width="960" height="504" alt="added a user billyjean  to this active directory" src="https://github.com/user-attachments/assets/38a67929-51be-4920-924e-09044c19d2d7" />

<img width="960" height="504" alt="sync my domain with Entra Connect " src="https://github.com/user-attachments/assets/53e0aa57-014d-4921-afc6-b19f3578cbc5" />

<img width="960" height="504" alt="configuration was successful" src="https://github.com/user-attachments/assets/ef758535-2e1b-45a8-af2e-688b9b91a339" />

user in the on prem domain is active in entra id <img width="960" height="514" alt="the user we created in our on pre active directory is present in entra id" src="https://github.com/user-attachments/assets/e71a1564-4192-45c6-90a6-8ac15a662c85" />



# Lessons Learned

Microsoft Entra Connect requires accurate system time and TLS 1.2 to function correctly.

Global Administrator access is required during the initial setup of Entra Connect.

Azure DNS settings do not apply to locally hosted virtual machines.

Proper DNS resolution and outbound internet connectivity are critical for hybrid identity deployments.

Troubleshooting hybrid IAM environments requires both identity and system-level knowledge.
