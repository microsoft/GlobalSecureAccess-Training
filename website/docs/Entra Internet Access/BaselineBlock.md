---
sidebar_position: 20
title: "Block access using Baseline profile"
---

## POC scenario: Create a baseline policy applying to all internet access traffic routed through the service

Microsoft Internet Access baseline policy allows to configure filtering policies that apply to all traffic without linking to a Conditional Access policy. 
You can use the baseline profile to block web categories that no user in the organization should be allowed to browse, for example inappropriate sites.

Complete the following tasks to create this baseline policy to block an FQDN:

- Configure a block rule for a risky web category by [creating a web filtering policy](#create-a-web-filtering-policy).
- Group and prioritize your web filtering policies by [configuring the baseline profile](#configure-the-baseline-profile).
- Use your test user to [attempt to access the blocked site](#attempt-to-access-blocked-sites) to confirm application of your rule.
- [View activity in the traffic log](#view-activity-in-the-traffic-log).

### Create a web filtering policy

1. In the **Microsoft Entra admin center**, go to **Global Secure Access** \> **Secure** \> **Web content filtering policies** \> **Create policy** \> **[Configure Global Secure Access content filtering](https://learn.microsoft.com/entra/global-secure-access/how-to-configure-web-content-filtering)**.

1. On **Create a web content filtering policy** \> **Basics**, provide the following details.
   * **Name**: Baseline Internet Access block rule.
   * **Description**: Add a description.
   * **Action**: Block.

2. Select **Next**.
3. On **Create a web content filtering policy** \> **Policy Rules**, select **Add Rule**.
4. In the **Add Rule** dialog box, provide the following details.
   * **Name**: Baseline blocked web categories.
   * **Destination type:** webCategory.
   * **Search**: Select a few risky categories, confirm they are in the Selected items list.
5. Select **Add**.
6. On **Create a web content filtering policy** \> **Policy Rules**, confirm your selections.
7. Select **Next**.
8. On **Create a web content filtering policy** \> **Review**, confirm your policy configuration.
9. Select **Create policy**.
10. To confirm policy creation, view it in the **Manage web content filtering policies** list.

### Configure the baseline profile

1. In the **Microsoft Entra admin center**, go to **Global Secure Access** \> **Secure** \> **Security profiles**. Select **Baseline profile**.
2. Click **Edit Profile**, and complete the following information on the **Basics** page.
   * **Profile name**: Baseline Internet Access Block Profile.
   * **Description:** Add a description.
   * **State**: enabled.
3. Select the **Link policies** page.
4. Select **Link a policy**. Select **Existing policy**.
   * In the **Link a policy** dialog box, select **Policy name** and select **Baseline Internet Access block rule**.
   * **Priority**: 100.
   * **State**: Enabled.
5. Select **Add**.
6. On **Link policies**, confirm **Baseline Internet Access Block Rule** is in the list.
7. Close the baseline profile.

### Attempt to access blocked sites

1. Sign in to the test device where you installed the global secure access (GSA) agent.
2. To confirm blocked access, attempt to open the FQDN you blocked. It can take up to 20 minutes for the policy to apply to your client device.


### View activity in the traffic log

1. In the **Microsoft Entra admin center** \> **Global Secure Access** \> **Monitor**, select [**Traffic logs**](https://learn.microsoft.com/entra/global-secure-access/how-to-view-traffic-logs). If needed, select **Add filter**. Filter when **User principal name** contains *testuser* and **Action** set to **Block**.
2. Observe the entries for your target FQDN that show traffic as blocked and then allowed. There may be a delay of up to 20 minutes for entries to appear in the log.
