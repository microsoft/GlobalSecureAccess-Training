---
sidebar_position: 20
title: "Segmenting Access"
---

After configuring the VPN Replacement scenario providing broad access to on-premises resources, you are in a position to start segmenting access.
Segmenting access allows the organization to provide specific network access based on used needs. 
Here is an example of network access segmentation made possible by Private Access: 

* Only users in the Finance team need access to the Web server finance.contoso.local, hosted by a single web server at 10.1.1.100:443
* Only the Wintel admins need access to perform remote administration via RDP, so they are allowed access to 10.1.1.100:3389

### Segmentation strategy

Here are the steps to segment access from Quick Access configured to provide broad access to resources:
1. Create a new Enterprise Application that defines access to the application or resource you want to segment access for. Private Access allows overlapping segments between Quick Access and Enterprise Apps. Segments defined on Enterprise Apps are given higher priority to those defined on Quick Access.
2. Assign your newly created Enterprise App to the users that should be allowed to access.
3. Allow for a minimum of 15 minutes so your configuration changes are delivered to GSA clients.
4. As a best practice, remove the segments that have been defined on your newly created Enterprise App from your Quick Accesses segment configuration. This might require breaking IP subnets into smaller ranges such as the exclusion is possible.

![](image-2.png)

This deck walks through strategies for segmenting access after configuring Private Access as VPN replacement.\
[Private Access Segmentation Strategy](https://github.com/microsoft/GlobalSecureAccess/blob/main/website/content/PA%20-%20Segmentation%20Strategy.pptx)
