---
title: Manage customer match audiences using customer data lists
description: Learn how to create and edit [!DNL Google Ads] and [!DNL Microsoft Advertising] customer match audiences from your customer data lists.
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
---
# Manage [!DNL Google Ads] and [!DNL Microsoft Advertising] customer match audiences using customer data lists

You can create [!DNL Google Ads] and [!DNL Microsoft Advertising] customer match audiences from your customer data lists. You can also update any [!DNL Google Ads] or [!DNL Microsoft Advertising] customer match audience except for [!DNL Google Ads] audiences created from an [!DNL Adobe] audience.

## Create a customer match audience from a customer data list

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts that are eligible for customer match only*

You can create a [!DNL Google Ads] or [!DNL Microsoft Advertising] customer data-based list from a data file that you generate from your customer relationship management (CRM) system.

For [!DNL Microsoft Advertising] accounts, the file can include email addresses. For [!DNL Google Ads] accounts, the file can include email addresses, mailing addresses, or telephone numbers; user IDs; or mobile device IDs from your CRM.

>[!NOTE]
>
>Search, Social, & Commerce doesn't store any of the customer data you upload or from the [!DNL Adobe] segments used to create or edit a [!DNL Google Ads] or [!DNL Microsoft Advertising] audience.

1. Generate a file with the customer data in the required format.

   First and last names, email addresses, and telephone numbers must be hashed using the SHA-256 algorithm. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> For [!DNL Google Ads] audiences, see the [!DNL Google Ads] documentation on "[Formatting guidelines for uploading hashed data](https://support.google.com/google-ads/answer/7476159)" for a list of permitted contact information fields and requirements. For [!DNL Microsoft Advertising] audiences, see the [!DNL Microsoft Advertising] documentation on [preparing customer match lists](https://help.ads.microsoft.com/#apex/ads/en/56921). You can optionally download a [!DNL Microsoft Excel] template for contact information.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Audiences] > [!UICONTROL Library]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network and the account name, and then click **[!UICONTROL Continue]**.

1. Specify the audience information:

   1. In the [!UICONTROL Data Source] menu, select **[!UICONTROL Customer List]**.
   
   1. Enter the **[!UICONTROL Audience Name]**.
   
   1. Upload the file:
   
      1. Select the [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]*, or *[!UICONTROL Mobile Device IDs]*.

         The User IDs option is available only to [!DNL Google Ads] advertisers in the U.S. who are opted in for [user ID segments](https://support.google.com/google-ads/answer/9199250)

      1. (Mobile device ID lists only) Select the **[!UICONTROL OS Type]** (*[!UICONTROL Android&trade;]* or *[!UICONTROL iOS]*), and enter the **[!UICONTROL App ID]**.
      
         The App ID is a unique identifier that the mobile operating system uses to allow your application to connect to the Google Play or Apple App Store:
         
         * ([!DNL Android&trade;] apps) The [!DNL Android&trade;] package name within [!DNL Google Play], identified by "`id=<package_name>`."
         
           For example, in `https://play.google.com/store/apps/details?id=com.example.game`, the package name is com.example.game.
           
         * ([!DNL iOS] apps) The application ID within the [!DNL iTunes App Store], identified by "`<idNNNNNNNNN>`" at the end of the URL. It's also available in the [!DNL iOS Developer Console].
         
           For example, in `https://itunes.apple.com/us/app/id284882215`, the ID is id284882215.

         Your development team has access to the [!UICONTROL App ID] for the relevant platform.

      1. In the [!UICONTROL Select File] field, click **[!UICONTROL Choose File]** and select the file on your network or device.

      1. Select the check box to indicate that you agree with the terms of the [!DNL Adobe] and ad network privacy policies.

      1. (Advertisers creating [!DNL Google Ads] audiences who do business in the European Economic Area (EEA) or United Kingdom (UK); optional) If you've collected consent from EEA and UK users to upload their data for advertising purposes, then select the check box next to **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

      [!DNL Google Ads] ignores any data for EEA and UK users with an unspecified consent status. This may lead to data discrepancy and performance issues.

      1. Click **[!UICONTROL Upload File]**.

   1. Specify the number of **[!UICONTROL Membership Days]**, which is the number of days a user's cookie stays in the audience.
   
     Use the length of time for which you expect your ad to be relevant to the user. Customer lists don't expire unless you enter a value.

1. Click **[!UICONTROL Post]**.

>[!NOTE]
>
>* The ad network may take up to 24 hours to process the file.
>* See [[!DNL Google Ads] documentation on how customer match works and limitations](https://support.google.com/displayvideo/answer/9539301).

## Edit a Customer Match Audience Using a Customer Data List

You can update any [!DNL Google Ads] or [!DNL Microsoft Advertising] customer match audience except for [!DNL Google Ads] audiences created from an [!DNL Adobe] audience. You can upload data to add, to delete, or to replace all existing data for the audience.

The data must be the same type as the original customer list (email addresses, mailing addresses, telephone numbers, user IDs, or mobile device IDs for a specific app on a specific mobile operating system). 

1. Generate a file with the customer data in the required format for the existing data type.

  First and last names, email addresses, and telephone numbers must be hashed using the SHA-256 algorithm. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> For [!DNL Google Ads] audiences, see the [!DNL Google Ads] documentation on "[Formatting guidelines for uploading hashed data](https://support.google.com/google-ads/answer/7476159)" for a list of permitted contact information fields and requirements. For [!DNL Microsoft Advertising] audiences, see the [!DNL Microsoft Advertising] documentation on [preparing customer match lists](https://help.ads.microsoft.com/#apex/ads/en/56921. You can optionally download a [!DNL Microsoft Excel] template for contact information.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Audiences] > [!UICONTROL Library]**.

1. Select the check box next to the audience to edit.

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png).

1. Select the action: *[!UICONTROL Add]* (to add the uploaded data to the existing data, unless it already exists), *[!UICONTROL Delete]* (to delete the uploaded data from the existing data, when it already exists), or *[!UICONTROL Replace]* (to delete all existing data and replace it with the uploaded data).

1. Upload the file:

   1. In the [!UICONTROL Select File] field, click **[!UICONTROL Choose File]** and select the file on your network or device.
   
   1. Select the check box to indicate that you agree with the terms of the [!DNL Adobe] and ad network privacy policies.
   
   1. Click **[!UICONTROL Upload File]**.

1. Click **[!UICONTROL Post]**.

>[!NOTE]
>
>The ad network may take a while to process updates to an audience.

>[!MORELIKETHIS]
>
>* [About audiences](audience-about.md)
>* [Create [!DNL Google Ads] customer match audiences from [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [Create a [!DNL Google Ads] customer match audience from an Adobe Campaign email list](google-audience-from-campaign-email-list.md)
>* [Manage dynamic remarketing audiences](audience-dynamic-remarketing-manage.md)
