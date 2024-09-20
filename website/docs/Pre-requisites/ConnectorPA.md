---
sidebar_position: 5
title: "Private Network Connector"
---


Connectors are lightweight agents that sit on a server in a private network and facilitate the outbound connection to the Global Secure Access service. Connectors must be installed on a Windows Server that has access to the backend resources and applications. 
You can organize connectors into connector groups, with each group handling traffic to specific applications. 

For a POC, avoid placing connectors on DMZ networks, instead consider placing the connector/s servers on a network location close to the resources you are planning to make available through Private Access.


Follow the steps in this article to plan and deploy your connectors in preparation for testing Private Access:

[Understand the Microsoft Entra private network connector](https://learn.microsoft.com/en-us/entra/global-secure-access/concept-connectors)

[How to configure private network connectors for Microsoft Entra Private Access and Microsoft Entra application proxy](https://learn.microsoft.com/en-us/entra/global-secure-access/how-to-configure-connectors)


