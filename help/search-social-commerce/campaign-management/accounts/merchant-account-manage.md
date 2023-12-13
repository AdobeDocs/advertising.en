---
title: Manage merchant accounts
description: Learn how to set up and manage account details for a merchant center account.
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
---
# Manage merchant accounts

*Agency account manager, Adobe account manager, and administrator user roles only*

Search, Social, & Commerce can download and display product data each day for any of an advertiser's Google Merchant Center or Microsoft Merchant Center accounts. In addition, Search, Social, & Commerce can automate ad creation based on the contents of the merchant account.To work directly with product data in Search, Social, & Commerce, you must create a corresponding account record containing the account access credentials and with access *enabled*. 

>[!NOTE]
>
>You can't remove a merchant account record. You can disable access to an account by changing the account type to *disabled*.

## Create merchant account details {#create-merchant-account}

*Agency account manager, Adobe account manager, and administrator user roles only*

To view product data and generate tracking templates for a merchant account, and to create ads based on the data, you must create a corresponding account record containing the account access credentials and with access to the account *enabled*.

>[!NOTE]
>
>To create an actual account on the merchant network, go to the network's website.

1. In the main menu, click **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**, which opens to the [!UICONTROL Accounts] tab.

1. In the toolbar above the data table, click **[!UICONTROL Create Account]**.

1. Specify the [merchant account settings](#merchant-account-settings):

   1. In the [!UICONTROL Product Source] menu, select the merchant center.

   1. (Required for [!DNL Google Ads] accounts; optional for [!DNL Microsoft Advertising] accounts) Allow Search, Social, & Commerce to access the account using the [[!DNL OAuth] authorization protocol](https://oauth.net/2/):

      1. ([!DNL Microsoft Advertising] accounts only) Select **[!UICONTROL oAuth]**.

      1. Click **[!UICONTROL Enable Connection]**.

      1. (If you're not logged in to the advertiser's account) Log in to the advertiser's account. The best practice is to use the credentials for content API access to the merchant center account.

      1. In the request for access/permission screen, click the button to confirm permission.

      1. Copy the authentication string in the pop-up window that opens, and paste the string into the **[!UICONTROL oAuth Token]** field.

      1. Specify the other account settings.

1. Click **[!UICONTROL Save]**.

   Attribute data for all products in the account is available in Search, Social, & Commerce after the next daily sync process (about 06:00 in the user's local time zone). You then can use the product data to automate ad creation using inventory feeds.

## Edit merchant account details {#edit-merchant-account}

*Agency account manager, Adobe account manager, and administrator user roles only*

If account credentials change or you want to stop retrieving and using data for a merchant account, then edit the account details. 

>[!NOTE]
>
>To edit an actual account on the merchant network, go to the network's website.

1. In the main menu, click **[!UICONTROL Search] \> [!UICONTROL Campaigns] \> [!UICONTROL Products]**, which opens to the [!UICONTROL Accounts] tab.

1. Next to the account name, click ![View/edit settings](/help/search-social-commerce/assets/settings.png "View/edit settings").

1. Edit the [merchant account settings](#merchant-account-settings).

1. Click **[!UICONTROL Save]**.

>[!NOTE]
>
>Search, Social, & Commerce must synchronize the new account data with that on the merchant network. This happens automatically once a day at about 06:00 in the user's local time zone.

## Disable access to a merchant account {#disable-merchant-account}

*Agency account manager, Adobe account manager, and administrator user roles only*

When you disable a merchant account, Search, Social, & Commerce doesn't log in to the account and therefore doesn't retrieve updated product data. Data collected while the account was enabled is still stored, and existing ads created using product data aren't updated, paused, or deleted according to the feed template and feed data settings.

1. In the main menu, click **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** , which opens to the [!UICONTROL Accounts] tab.

1. Next to the account name, click ![View/edit settings](/help/search-social-commerce/assets/settings.png "View/edit settings").

1. Change the [!UICONTROL EF Account Type] to **[!UICONTROL Disabled]**.

1. Click **[!UICONTROL Save]**.

## Merchant account settings {#merchant-account-settings}

>[!NOTE]
>
>Only agency account manager, [!DNL Adobe] account manager, and administrator user roles can configure merchant account settings.

**[!UICONTROL Product Source]:** The merchant network. You can't change the value for an existing account. 

**[!UICONTROL OAuth Token]:** ([!DNL Google Merchant Center] accounts only) The account's token to authorize logins using the [[!DNL OAuth] authorization protocol](https://oauth.net/2/). 

**[!UICONTROL Auth Type]:** ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] only) Whether to authorize logins to the account using:

* *[!UICONTROL Client login]:* To use the client's login.

* *[!UICONTROL oAuth]* (the default): To use the [[!DNL OAuth] authorization protocol](https://oauth.net/2/).

**[!UICONTROL Access Key]:** ([!DNL Microsoft Merchant Center] only) The access key for the developer account to use.

**[!UICONTROL Account Name]:** The name displayed for the account within Search, Social, & Commerce. 

**[!UICONTROL Login]:** The login name or ID for the account. 

**[!UICONTROL Password]:** The password for the account. 

**[!UICONTROL Confirm Password]:** The password for the account. 

**[!UICONTROL EF Account Type]:** Whether Search, Social, & Commerce will access the account:

* *[!UICONTROL Enabled]* (the default): Search, Social, & Commerce can log in to the account to retrieve product data.

* *[!UICONTROL Disabled]:* Search, Social, & Commerce doesn't log in to the account and therefore doesn't retrieve updated product data. Data collected while the account was enabled is still stored, and existing ads created using product data aren't updated, paused, or deleted according to the feed template and feed data settings.

**[!UICONTROL Account ID]:** The merchant account ID. If you have only one account with the specified login information, then this value is optional. 

**[!UICONTROL Time Zone]:** The advertiser's time zone. Use the same time zone configured for the advertiser's Search, Social, & Commerce account information (which is set when the account is created). You can't change the value for an existing account. 

>[!MORELIKETHIS]
>
>* [About ad network accounts](ad-network-account-about.md)
>* [Manage ad network accounts](ad-network-account-manage.md)
