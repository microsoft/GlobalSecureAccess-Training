---
sidebar_position: 200
title: Running GSA POCs
---

## I want to run a Global Secure Access Proof of Concept!



### Kick off
You can use this deck to kick off POCs with customers, walking them through high-level requirements, stakeholders that should be involved, decide on scenarios that should be in scope and agreeing on a timeline.\
[POC Kick off deck](https://github.com/microsoft/GlobalSecureAccess/blob/main/website/content/Security%20Service%20Edge%20-%20PoC%20Kickoff.pptx)


Review the information below to decide the scenarios that will be tested as part of the POC.

This guide assumes you are running a POC in a production environment. Running a POC in a test environment might give you more flexibility.

## Private Access
#### Are you using a VPN today? The best way to start is by testing our "VPN Replacement" scenario.
This gives you the ability to publish all the same resources that users access through the VPN, protected by Microsoft Entra ID.
From that point onwards, you can start "segmenting access" by creating Enterprise Apps that define access to specific resources that only selected users should access. For example, only administrators should be able to RDP servers.

Review the [VPN Replacement](./Entra%20Private%20Access/VPNReplacement.md) section to understand the recommended configuration for this scenario.

#### What devices are you planning on using to test? Users' day to day work devices or separate test devices?
If you plan to use work devices consider testing the "VPN Replacement" scenario so you are able to use Private Access for all your daily work.

Alternatively, if you'd like to only publish certain resources using Private Access, consider you might need to switch to using your VPN for accessing other resources you need during your day.
If you decide to only [publish certain resources using Private Access](./Entra%20Private%20Access/per-appAccess.md), consider how users would authenticate to those resources and if configuring [SSO with Active Directory](./Entra%20Private%20Access/OnPremSSO.md) is required.

## Internet Access

There are several scenarios enabled by Internet Access and Microsoft Access that can be tested as part of a POC.
Alternatively, coexistence with other solutions can be tested using the guidance provided here: [Secure Access with Global Secure Access Partners](https://learn.microsoft.com/entra/global-secure-access/concept-cisco-coexistence)