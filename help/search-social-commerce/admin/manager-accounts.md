---
title: Manage credentials for ad network manager accounts
description: Learn how to provide credentials for your [!DNL Google Ads] manager accounts.
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
---
# Manage credentials for ad network manager accounts

*[!DNL Google Ads] accounts only*

Provide the credentials for your [!DNL Google Ads] manager accounts to which you want Search, Social, & Commerce to upload cross-account conversions. Use this feature if you want to a) upload [!DNL Adobe]-tracked, cross-account conversion metrics to a [!DNL Google Ads] manager account or b) upload portfolio objectives that include cross-account conversions to [!DNL Google Ads] for hybrid optimization.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

You can add credentials for new manager account records, or reauthenticate an existing manager account.

Once you add credentials for a manager account, the account settings show the associated manager account ID as read-only. In addition, an optional "[!UICONTROL Manager Account for Cross-Account Conversions]" column in the [!UICONTROL Campaigns] > [!UICONTROL Accounts] view shows the manager account ID for each child account and indicates an error when the manager account isn't authenticated. [!UICONTROL Notification Center] includes notifications when a manager account's credentials are missing ([the [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) or when a manager account authentication token expires ([the [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## To add credentials for a new manager account

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Manager Accounts]**.

1. Select **[!UICONTROL Create new manager account]**.

1. Enter login credentials for the manager account.
   
   The **[!UICONTROL Manager Account ID]** and **[!UICONTROL Login Email]** are required. Search, Social, & Commerce automatically captures and stores the account token to use for authentication.
   
   You can optionally include an **[!UICONTROL MCC Account Name]** for identification within Search, Social, & Commerce and the account **[!UICONTROL Password]**. Enter the password when you want to encrypt and save it so that the account manager can refresh tokens as needed.

1. Click **[!UICONTROL Authenticate]**.

1. Click **[!UICONTROL Save]**.

## To reauthenticate an existing manager account

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Manager Accounts]**.

1. Select **[!UICONTROL Reauthenticate existing manager account]**.

1. Select the manager account.

1. Enter login credentials for the manager account.
   
   The **[!UICONTROL Manager Account ID]** and **[!UICONTROL ]Login Email** are required. Search, Social, & Commerce automatically captures and stores the account token to use for authentication.
   
   You can optionally include an **[!UICONTROL MCC Account Name]** for identification within Search, Social, & Commerce and the account **[!UICONTROL Password]**. Enter the password when you want to encrypt and save it so that the account manager can refresh tokens as needed.

1. Click **[!UICONTROL Authenticate]**.

1. Click **[!UICONTROL Save]**.
 
>[!MORELIKETHIS]
>
>* [Enable uploading of objectives to ad networks](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Upload conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md) 
>* [Edit your notification settings](/help/search-social-commerce/notifications/notification-edit.md)
