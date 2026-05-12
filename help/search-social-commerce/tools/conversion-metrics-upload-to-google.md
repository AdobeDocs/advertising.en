---
title: Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]
description: Learn how to upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads].
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
TQID: https://experienceleague.adobe.com/ayxUfDgkrnPz0s-pFAdkmvYy94Il5szQHl6lYg8DpF8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]

*Advertisers with [!DNL Google Ads] accounts and Adobe Advertising conversion tracking only*

Search, Social, & Commerce can optionally upload to [!DNL Google Ads] all conversion metrics it tracks for [!DNL Google Ads] campaigns that use the Adobe Advertising conversion tracking service. This option doesn't make the conversions available for hybrid optimization. If you want to use your Adobe conversions for hybrid optimization, see "[Enable uploading of objectives to ad networks](objective-upload-to-networks.md)."

Daily uploads include the tracked `gclid` value, the conversion value defined using the advertiser-level attribution model, and the timestamp. If the attribution model is updated, then the next upload uses the new model, but past data isn't updated to use the new model.

>[!NOTE]
>
>The uploads don't include conversion metrics uploaded to Adobe Advertising from feed files.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Tools] > [!UICONTROL Conversion Upload Setup]**.

1. Select the check box next to **[!UICONTROL Upload Conversions to Google Ads]**.

1. (Advertisers doing business in the European Economic Area (EEA) or United Kingdom (UK); optional) If you've collected consent from EEA and UK users to upload their data for advertising purposes, then select the check box next to **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Click **[!UICONTROL Save]**.

1. (If your conversions are tracked at a manager account level) [Add credentials for your manager account](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Enable uploading of objectives to ad networks](objective-upload-to-networks.md)
