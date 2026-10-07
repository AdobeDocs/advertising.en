---
title: Manage [!DNL ChatGPT Ads] conversational ad accounts
description: Learn how to create and manage accounts for [!DNL ChatGPT Ads] chat card ads, a beta feature that places ads inside AI assistant conversations.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Manage [!DNL ChatGPT Ads] conversational ad accounts

*Beta feature*

Through Adobe DSP's integration with [!DNL OpenAI Ads], you can run [!DNL ChatGPT Ads] chat card ads, which appear inside [!DNL ChatGPT] conversations. For this feature, DSP creates an ad account and buys media on your organization's behalf. You won't be able to access the ad account from ads.openai.com. Use this feature to test AI media without establishing a direct relationship with [!DNL ChatGPT Ads].

You'll manage your conversational ad accounts &mdash; including its campaigns, ad groups, and ads &mdash; separately from your regular DSP campaigns, which are structured differently. You'll also [view performance data for [!DNL ChatGPT Ads] campaigns, ad groups, and ads](campaign-manage.md#campaign-views-about) separately from your DSP campaigns.

The following determines eligibility for this feature:

* **Link to an advertiser in Search, Social, & Commerce:** Your DSP advertiser must be linked to an Adobe Search, Social, & Commerce advertiser. To link an advertiser, contact your Adobe Account Team.

* **Existing [!DNL Search, Social, & Commerce] customers:** If your advertiser already uses [!DNL Search, Social, & Commerce], then [create and manage its [!DNL ChatGPT Ads] campaigns in Search, Social, & Commerce](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md) instead of in DSP.

* **Restricted industries:** Advertisers in restricted categories (for example, finance or healthcare) can't create conversational ad accounts or campaigns.

If the selected advertiser isn't eligible, then the [!UICONTROL Accounts] and [!UICONTROL Campaigns] tabs indicate the reason. You can still switch to a different advertiser using the advertiser selector.

## About the [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts] view {#accounts-view-about}

The [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts] tab lists the [!DNL OpenAI] accounts for the selected advertiser. Information for each account includes:

**[!UICONTROL Status]:** Whether the account is currently serving ads: *Active* or *Paused*. You can't change an account's status; contact your Adobe Account Team if you want to pause or reactivate an account.

**[!UICONTROL Review status]:** The [!DNL OpenAI] review state: *Under Review*, *Approved*, or *Disapproved*. Hold the cursor over the status for the reason, if one is available.

**[!UICONTROL Active campaigns]:** The number of currently active campaigns in the account.

**[!UICONTROL Cost]:** The account's total spend.

### Available actions

* [View account limits](#account-limits)

* [Create an account](#account-create)

* [Edit an account](#account-edit)

## View account limits {#account-limits}

An account limit caps an account's total spend over a specific date range. You can view an account's limits, but only your Adobe Account Team can create, edit, or remove the limits.

1. In the main menu, click **[!UICONTROL Conversational Ads Beta]**.

1. On the **[!UICONTROL Accounts]** tab, hold the cursor over the account row and click **[!UICONTROL ...] > [!UICONTROL View account limit]**.

The [!UICONTROL Account limits] page lists each limit for the account:

**[!UICONTROL Name]:** The name of the limit.

**[!UICONTROL Amount]:** The total spend cap for the limit period.

**[!UICONTROL Period]:** The date range the limit applies to.

**[!UICONTROL Status]:** *Active*, *Upcoming*, or *Completed*.

**[!UICONTROL Spent]:** The amount spent so far within the limit period.

>[!NOTE]
>
>You can't edit or remove completed limits, and limit periods for the same account can't overlap.

## Create a [!DNL ChatGPT Ads] conversational ad account {#account-create}

Each advertiser can have up to two [!DNL ChatGPT Ads]  accounts.

1. In the main menu, click **[!UICONTROL Conversational Ads Beta]**.

1. Do one of the following:

   * (Your first account only) On the welcome screen, click **[!UICONTROL Create an Account]**.

   * On the **[!UICONTROL Accounts]** tab, select an advertiser, and then click **[!UICONTROL Create Account]**.

1. Specify the [account settings](#account-settings).

1. Select the **[!UICONTROL I agree to the Terms and Conditions]** checkbox.

1. Click **[!UICONTROL Create account]**.

New accounts are created in a paused state while [!DNL OpenAI] reviews them. DSP activates the account once it's approved.

## Edit a [!DNL ChatGPT Ads] conversational ad account {#account-edit}

You can edit an account's legal business name and website after you create it.

1. In the main menu, click **[!UICONTROL Conversational Ads Beta]**.

1. On the **[!UICONTROL Accounts]** tab, hold the cursor over the account row and click **[!UICONTROL ...] > [!UICONTROL Edit account]**.

1. Edit the **[!UICONTROL Legal Business Name]** and/or **[!UICONTROL Advertiser Website]**. For more information about the fields, see "[Account settings](#account-settings)."

1. Click **[!UICONTROL Save changes]**.

>[!IMPORTANT]
>
>Saving changes restarts [!DNL OpenAI]'s review for the account. The account won't serve ads again until the account is re-approved.

## Return to the DSP main menu

* Above the main menu, click **[!UICONTROL Back to DSP]**.

### [!DNL ChatGPT Ads] conversational ad account settings {#account-settings}

**[!UICONTROL Legal Business Name]:** The business name for the account, which is displayed in DSP.<!-- Just for display in DSP? -->

**[!UICONTROL Advertiser Website]:** The URL of the advertiser's website, beginning with `http://` or `https://`.

**[!UICONTROL Currency]:** (Read-only) The currency used for the account. The currency for your DSP user account is used.

**[!UICONTROL Timezone]:** (Read-only) The timezone used for the account. The timezone for your DSP user account is used.

**[!UICONTROL Favicon]:** An image file to use as the website favicon for the account<!-- How is this used within this context? -->. The browser displays the favicon in various places, such as the address bar, tab, or bookmarks. The file must be in JPG, PNG, or WEBP format and a minimum of 256x256 pixels.

To upload an icon, click **[!UICONTROL Upload favicon]**, and then locate and select a file on your device or network.

**[!UICONTROL I agree to the Terms and Conditions]:** A check box to indicate that you agree to all legal terms. Select the check box to create an account or update the account settings.

>[!NOTE]
>
>You're billed for usage at the end of the month with your other invoices. For billing questions, contact your Adobe Account Team.

>[!MORELIKETHIS]
>
>* [Manage conversational ad campaigns](campaign-manage.md)
