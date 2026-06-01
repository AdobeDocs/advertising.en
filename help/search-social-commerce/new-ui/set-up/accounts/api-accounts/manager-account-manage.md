---
title: (New UI) Manage credentials for Google Ads manager accounts
description: Learn how to set up and manage credentials for Google Ads manager accounts in the new UI.
feature: Search Admin
---
# (New UI) Manage credentials for [!DNL Google Ads] manager accounts

*Beta feature*

*[!DNL Google Ads] accounts only*

Provide credentials for your [!DNL Google Ads] manager accounts to which you want Search, Social, & Commerce to upload cross-account conversions. Use this feature if you want to a) upload [!DNL Adobe]-tracked, cross-account conversion metrics to a [!DNL Google Ads] manager account or b) upload portfolio objectives that include cross-account conversions to [!DNL Google Ads] for hybrid optimization.

You can add credentials for new manager account records or reauthenticate an existing manager account.

Once you add credentials for a manager account, the account settings show the associated manager account ID as read-only. [!UICONTROL Notification Center] includes [notifications](/help/search-social-commerce/new-ui/notifications-manage.md) when a manager account's credentials are missing (the [!UICONTROL Manager Account Missing Error]) or when a manager account authentication token expires (the [!UICONTROL Manager Account Auth Error]).

## Add credentials for a new manager account {#create-manager-account}

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Click **[!UICONTROL +]**.

1. Select the ad network, and then click **[!UICONTROL Next]**.

1. Specify the [manager account settings](#manager-account-settings).

1. Click **[!UICONTROL Authenticate]** and log in using the manager account credentials.

   Search, Social, & Commerce automatically captures and stores the authentication token.

1. In Search, Social, & Commerce, click **[!UICONTROL Save]**.

## Edit manager account details {#edit-manager-account}

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Select the account in either of the following ways:

   * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

   * Hold the cursor over the account name, click **...**, and then click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit).

1. Edit the [manager account settings](#manager-account-settings).

1. Click **[!UICONTROL Re-Authenticate]** and log in using the manager account credentials.

   Search, Social, & Commerce automatically captures and stores the authentication token.

1. In Search, Social, & Commerce, click **[!UICONTROL Save]**.

## Reauthenticate a manager account {#reauthenticate-manager-account}

Reauthenticate a manager account when the OAuth token expires or becomes invalid.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Reauthenticate]**.

1. Log in using the manager account credentials.

   Search, Social, & Commerce automatically captures and stores the new authentication token.

## Manager account settings {#manager-account-settings}

**[!UICONTROL Manager Account ID]:** The unique account ID for the manager account on the ad network.

**[!UICONTROL Mnaager Account Name]:** The name to display for the manager account within Search, Social, & Commerce.

**[!UICONTROL Login Email]:** The email address associated with the manager account login. Required for authentication.

**[!UICONTROL Password]:** (Optional) The password for the account. Enter the password when you want to encrypt and save it so that the account manager can refresh tokens as needed.

>[!MORELIKETHIS]
>
>* [Enable uploading of objectives to ad networks](/help/search-social-commerce/new-ui/goals/objectives/objective-upload-to-networks.md)
>* [Manage notifications](/help/search-social-commerce/new-ui/notifications-manage.md)

<!--
I don't see this yet in new UI:
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
-->
