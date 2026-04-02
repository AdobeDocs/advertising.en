---
title: Implement [!DNL Microsoft Advertising] enhanced conversions for offline conversions
description: Learn about the workflow for setting up [!DNL Microsoft Advertising] enhanced conversions for offline conversions.
feature: Search Campaign Management, Conversions
exl-id: 44937db7-9e80-4a5d-85c7-5bd5febc3b96
TQID: https://experienceleague.adobe.com/GLFczqDqV8HE5hUZt8ORAlQMNy4OqQTtMdaHoYoN10U
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
# Implement [!DNL Microsoft Advertising] enhanced conversions for offline conversions

*[!DNL Microsoft Advertising] accounts only*

[[!DNL Microsoft Advertising] enhanced conversions](https://help.ads.microsoft.com/#apex/ads/en/60178) allow you to map users to offline conversions using your first-party conversion data. Use enhanced conversions in environments in which click IDs are unavailable, such as to track telephone or email sales that result from website leads.

Within Search, Social, & Commerce, you can:

* View your existing enhanced conversions for offline conversions.

  Search, Social, & Commerce syncs your existing enhanced conversions daily at 05:00 in the advertiser's time zone.

* Upload first-party, offline conversion data to map to your existing enhanced conversion goals.

* Include your enhanced conversions as metrics within reports and as weighted metrics within objectives for optimization.

To use this feature, complete the following steps.

1. Follow all prerequisites in the [!DNL Microsoft Advertising] help on "[Enhanced conversions](https://help.ads.microsoft.com/#apex/ads/en/60178)."

1. [Set up an enhanced conversion goal within [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/60178).

1. As often as needed, upload first-party data, including hashed email addresses or telephone numbers, to attribute to the conversion for a specified account. You can complete this step from within either [Search, Social, & Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) or within [!DNL Microsoft Advertising].

   * Within Search, Social, & Commerce, you can download a template in [!DNL Microsoft Excel] format, enter your conversion data and save the file locally, and then upload the edited file.
   
     All uploaded data is synced in real-time to [!DNL Microsoft Advertising].

   * For more information about uploading data within [!DNL Microsoft Advertising], see the section "Set up Enhanced conversions for offline conversions" in the [!DNL Microsoft Advertising] help on "[Enhanced conversions](https://help.ads.microsoft.com/#apex/ads/en/60178)."

>[!MORELIKETHIS]
>
>* [Upload offline conversion data for enhanced conversions](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
