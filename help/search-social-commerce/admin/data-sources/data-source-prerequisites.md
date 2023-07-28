---
title: Prerequisites for configuring a [!DNL Google Analytics] data source
description: Learn about the steps that you must complete before you configure a [!DNL Google Analytics] data source.
role: User, Admin
exl-id: cbb2ad6d-8494-4fa4-928c-238b25bda3a6
feature: "Search Admin, Search Data Sources"
---
# Prerequisites for configuring a [!DNL Google Analytics] data source

Before you can set up a [!DNL Google Analytics] data source, you must establish the Search, Social, & Commerce query string parameter "ef_id" as the primary key to pass data from [!DNL Google Analytics] to Search, Social, & Commerce. Set up the primary key for each [!DNL Google Analytics] account and property combination for which you want sync data. Other people in your organization may need to complete these tasks; see below for more information.

If the landing page URLs for your ads or keywords don't already include Search, Social, & Commerce redirects, then add them first.

## Prerequisite 1: Implement a Search, Social, & Commerce token ("ef_id" query string parameter) in the landing page URLs for all applicable advertising accounts

On each paid search click for the relevant campaigns, a unique `ef_id` must be generated and appended to the landing page URL as a query string, such as `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, where `&ef_id=abcde:123456789:s` is the append symbol, `ef_id` key, and `ef_id` value. To include an ef_id, the relevant ad network accounts and campaigns must have the [!UICONTROL Tracking Type] "[!UICONTROL EF Redirect]" and the [!UICONTROL Redirect Type] "[!UICONTROL Token]."

For existing accounts and campaigns, the ef_id is probably already implemented.

If the ef_id isn’t included, ask your Adobe Account Team for assistance.

When all prerequisites are completed, the `ef_id` is used as the primary key to pass data from [!DNL Google Analytics] to Search, Social, & Commerce.

## Prerequisite 2: Capture the Search, Social, & Commerce token ("ef_id" query string parameter) in a custom dimension for each relevant [!DNL Google Analytics] property

Repeat the following tasks for each [!DNL Google Analytics] account and property combination for which you want to sync data. See [[!DNL Google Analytics] documentation on creating and implementing custom dimensions](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) for help with these tasks.

1. In [!DNL Google Analytics], create a custom dimension named "`ef_id`". Set the scope of the dimension to [!DNL User], and set the dimension to active.

   >[!NOTE]
   >
   >This prerequisite requires edit permission for the relevant properties.

1. Update your [!DNL Google Analytics] tracking code to capture the value of the ef_id query string parameter when it's present in the landing page URL and store it in the ef_id custom dimension. 
 
   >[!NOTE]
   >
   >The ef_id should be only in landing page URLs.

   For example, if the landing page URL is `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`, then the value of the ef_id dimension in [!DNL Google Analytics] is `abcde:123456789:s`.

   >[!NOTE]
   >
   >This prerequisite should be completed by a qualified developer.

>[!MORELIKETHIS]
>
>* [About syncing [!DNL Google Analytics] conversion metrics](data-source-about.md)
>* [Configure a [!DNL Google Analytics] view as a data source](data-source-configure.md)
>* [Edit a [!DNL Google Analytics] data source](data-source-edit.md)
>* [Pause syncing of a data source](data-source-pause.md)
>* [Reauthenticate a [!DNL Google Analytics] data source](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] data source settings](data-source-settings.md)
>* [Appendix - Available [!DNL Google Analytics] metrics](data-source-ga-metrics.md)
