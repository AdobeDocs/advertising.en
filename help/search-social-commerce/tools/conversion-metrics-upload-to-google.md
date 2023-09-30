---
title: Upload conversion metrics to [!DNL Google Ads]
description: Learn how to upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads].
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
---
# Upload conversion metrics to [!DNL Google Ads]

*Advertisers with [!DNL Google Ads] Accounts Only*

Search, Social, & Commerce can optionally upload to [!DNL Google Ads] all conversion metrics it tracks for [!DNL Google Ads] campaigns that use the Adobe Advertising conversion tracking service and conversion metrics synced from Adobe Analytics. This option doesn't make the conversions available for hybrid optimization. If you want to use your Adobe conversions for hybrid optimization, see "[Enable uploading of objectives to ad networks](objective-upload-to-networks.md)."

Daily uploads include the tracked `gclid` value, the conversion value defined using the advertiser-level attribution model, and the timestamp. If the attribution model is updated, then the next upload uses the new model, but past data isn't updated to use the new model.

>[!NOTE]
>
>The uploads don't include conversion metrics uploaded to Adobe Advertising from feed files.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Tools] > [!UICONTROL Conversion Upload Setup]**.

1. Select the check box next to **[!UICONTROL Upload Conversions to Google Ads]**.

1. Click **[!UICONTROL Save]**.

1. (If your conversions are tracked at a manager account level) [Add credentials for your manager account](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Enable uploading of objectives to ad networks](objective-upload-to-networks.md)
