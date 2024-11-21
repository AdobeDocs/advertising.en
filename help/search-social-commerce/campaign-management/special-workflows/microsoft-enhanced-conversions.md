---
title: Implement [!DNL Microsoft Advertising] enhanced offline conversions
description: Learn about the workflow for setting up [!DNL Microsoft Advertising] enhanced offline conversions.
feature: Search Campaign Management, Conversions
---
# Implement [!DNL Microsoft Advertising] enhanced offline conversions

<!-- EDIT ALL -- COPIED FROM GGL FILE -->

*[!DNL Microsoft Advertising] accounts only*

[[!DNL Microsoft Advertising] enhanced offline conversions](https://help.ads.microsoft.com/#apex/ads/en/60178) allow you to map users to offline conversions using your first-party conversion data. Use enhanced offline conversions in environments in which click IDs are unavailable, such as to track telephone or email sales that result from website leads.

You must create your enhanced conversions within [!DNL Microsoft Advertising].

Within Search, Social, & Commerce, however, you can:

* View your existing enhanced conversions.

  Search, Social, & Commerce syncs your existing enhanced conversions daily at 05:00 in the advertiser's time zone.

* Upload first-party, offline conversion data to map to your enhanced conversions.

* Include your enhanced conversions as metrics within reports and as weighted metrics within objectives for optimization.

To use this feature, complete the following steps. The steps to create conversion tracking tags and to create conversion actions can optionally be reversed.

1. Within [!DNL Microsoft Advertising], opt in to enhanced conversions xxxxxxx


1. Configure and implement a [!DNL Microsoft Advertising] tag for the conversion action.

   For instructions, see the [!DNL Microsoft Advertising] help to create tags xxxxxxx []().

1. Create a conversion action for the enhanced conversion within [Microsoft Advertising]().

   For the **Type of Conversion,** select *Import Conversion* or *Import.*

1. As often as needed, upload first-party data, including hashed email addresses or telephone numbers, to attribute to the conversion for a specified account. You can complete this step from within either [Search, Social, & Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) or using [!DNL Microsoft Advertising].<!-- verify --> <!-- Is there an MS equivalent? -->
   
   * Within Search, Social, & Commerce, you can download a template in [!DNL Microsoft Excel] format, enter your conversion data and save the file locally, and then upload the edited file.
   
     All uploaded data is synced in real-time to [!DNL Microsoft Advertising].

   * <!-- Is there an MS equivalent? -->For more information about uploading data using [!DNL Google Data Manager], see "[About Data manager](https://support.google.com/google-ads/answer/14639041)."<!-- Is there an MS equivalent? -->

>[!MORELIKETHIS]
>
>* [Upload offline conversion data for enhanced conversions](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
