---
sidebar_position: 300
---

For running a Global Secure Access POC you will need the following pre-requisites:

* An Microsoft Entra ID tenant
* A user with the Global Secure Access administrator, Application Administrator and Conditional Access Administrator roles.
* At least one test user
* At least one client device you'll use for user testing. To simulate remote access, this device should only have Internet access.
  * Windows 10/11 devices need to be either Microsoft Entra ID Joined or Hybrid Joined.
  * Android must have the Microsoft Defender app installed.

* Paid or trial licenses
  * Microsoft Entra Suite trial licenses https://aka.ms/Microsoft EntraSuiteTrial
  * Get Microsoft Entra Internet Access trial licenses https://aka.ms/InternetAccessTrial
  * Get Microsoft Entra Private Access trial licenses https://aka.ms/PrivateAccessTrial



For testing Private Access scenarios you'll need
* At least one Windows Server 2016 deployed where your private/on-premises resources are. This server must have line of sight to the resources you want to make available through Private Access and access to Microsoft URLs.
* One or more application you would like to make available using Private Access. You should obtain the IP addresses or FQDNS, protocols and ports used by the application.
* Alternatively, if you want to start your journey configuring Private Access as VPN Replacement, you'll need the IP ranges of your corporate server network.

