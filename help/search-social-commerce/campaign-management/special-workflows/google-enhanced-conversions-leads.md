---
title: Implement [!DNL Google Ads] enhanced conversions for leads
description: Learn about the workflow for setting up [!DNL Google Ads] enhanced conversions for leads.
feature: Search Campaign Management, Conversions
exl-id: b708c9f2-2962-45d9-8780-4e96ef2ae8f7
---
# Implement [!DNL Google Ads] enhanced conversions for leads

*[!DNL Google Ads] accounts only*

[[!DNL Google Ads] enhanced conversions for leads](https://support.google.com/google-ads/answer/9888656) allow you to map users to offline conversions using your first-party conversion data. Use enhanced conversions for leads in environments in which click IDs are unavailable, such as to track telephone or email sales that result from website leads.

Within Search, Social, & Commerce, you can:

* View your existing enhanced conversions for leads.

  Search, Social, & Commerce syncs your existing enhanced conversions for leads daily at 05:00 in the advertiser's time zone.

* Create enhanced conversions for leads.

* Upload first-party, offline conversion data to map to your enhanced conversions for leads.

* Include your enhanced conversions for leads as metrics within reports and as weighted metrics within objectives for optimization.

To use this feature, complete the following steps. The steps to create conversion tracking tags and to create conversion actions can optionally be reversed.

1. Within [!DNL Google Ads], opt in to enhanced conversions for leads:

   1. Open the account's conversion settings.

   1. Select the option for enhanced conversions for leads and accept the terms of service.
   
   1. Select whether to use a [!DNL Google] tag or [!DNL Google Tag Manager] to create the conversion tag.


1. Configure and implement a [!DNL Google] tag for the conversion action.

   For instructions, see the [!DNL Google Ads] help to create tags for enhanced conversions for leads [using a [!DNL Google] tag](https://support.google.com/google-ads/answer/11021502) or [using [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11347292).

1. Create a conversion action for the enhanced conversion for leads within either [Search, Social, & Commerce](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) or [Google Ads](https://support.google.com/google-ads/answer/12216226).

   For the **Type of Conversion,** select *Import Conversion* or *Import.*

1. As often as needed, upload first-party data, including hashed email addresses or telephone numbers, to attribute to the conversion for a specified account. You can complete this step from within either [Search, Social, & Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) or using [!DNL Google Data Manager].   
   
   * Within Search, Social, & Commerce, you can download a template in [!DNL Microsoft Excel] format, enter your conversion data and save the file locally, and then upload the edited file. The template includes columns to indicate if user consent was given for uploading data to [!DNL Google] for advertising purposes and for ad personalization purposes.
   
     All uploaded data is synced in real-time to [!DNL Google Ads].

   * For more information about uploading data using [!DNL Google Data Manager], see "[About Data manager](https://support.google.com/google-ads/answer/14639041)."

>[!MORELIKETHIS]
>
>* [Create a conversion action for a [!DNL Google Ads] enhanced conversion for leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Upload offline conversion data for enhanced conversions](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
