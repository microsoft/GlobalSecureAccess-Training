---
sidebar_position: 200
title: Running GSA POCs
---

I want to run a Global Secure Access POC!

First you need to decide what scenarios you want to test, here are some considerations to help you decide.

This guide assumes you are running a POC in a production environment. Running a POC in a test environment might give you more flexibility.

#### Are you using a VPN today? The best way to start is by testing our "VPN Replacement" scenario.
This gives you the ability to publish all the same resources that users access through the VPN, protected by Entra ID.
From that point onwards, you can start "segmenting access" by creating Enterprise Apps that define access to specific resources that only selected users should access. For example, only administrators should be able to RDP servers.

#### What devices are you planning on using to test? Users' day to day work devices or separate test devices?
If you plan to use work devices consider testing the "VPN Replacement" scenario so you are able to use Private Access for all your daily work.

Alternatively, if you'd like to only publish certain resources using Private Access, consider you might need to switch to using your VPN for accessing other resources you need during your day.
If you decide to only publish certain resources using Private Access, consider how users would authenticate to those resources and if configuring SSO with Active Directory is required.

## TBC