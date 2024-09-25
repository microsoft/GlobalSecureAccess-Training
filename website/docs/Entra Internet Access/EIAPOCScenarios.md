---
sidebar_position: 10
title: "POC Scenarios"
---


# Microsoft Entra Internet Access Proof of Concept


The guidance in this article helps you to deploy [Microsoft Entra Internet Access](https://learn.microsoft.com/entra/global-secure-access/concept-internet-access) as a proof-of-concept in your production or test environment. It includes setup and configuring web content filtering. Review the [pre-requisites](../Pre-requisites/ActivateGSA.md) which includes how to scope your configuration and testing for specific test users and groups.

## Deploy and test Microsoft Entra Internet Access

POC scenarios:

- [Create a baseline policy applying to all internet access traffic routed through the service](./BaselineBlock.md)
- [Block a group from accessing websites based on category](./BlockWebCat.md)
- [Block a group from accessing websites based on FQDN](./BlockFQDN.md)
- [Allow a user to access a blocked website](./Exceptions.md)
