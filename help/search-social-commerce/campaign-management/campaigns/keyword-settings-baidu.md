---
title: "[!DNL Baidu] keyword settings"
description: Reference the settings for [!DNL Baidu] keywords.
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/uMU0oAkL8rmsOIMXYR8qgp9-upe2qWIK-ev1YtPQUb4
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
# [!DNL Baidu] keyword settings

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** The keywords. The maximum length per keyword is 30 single-byte or 15 double-byte characters 

You can enter or paste up to 2000 keywords. Separate multiple keywords with commas, or enter them on separate lines. Use the following syntax:

* `keyword` for broad match
* `"keyword"` for phrase match
* `[keyword]` for exact match

>[!NOTE]
>
>* [!DNL Baidu] allows only one match type per keyword per ad group. For example, Ad Group 1 can't include both `"keyword"` and `[keyword]`.
>* You can create negative keywords from the [!UICONTROL Keywords] > [!UICONTROL Negatives] view and in the ad group and campaign settings.
>* Changing a [!DNL Baidu] keyword deletes the existing keyword and creates a new one with a new keyword ID. Changing the match type, however, doesn't delete the existing keyword.

**[!UICONTROL Status]:** The display status of the keyword: *Active* or *Paused*. The default for new keywords is *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL Options

**[!UICONTROL Base URL]:** (Campaigns with keyword-level tracking only; optional) The landing page URL to which users are taken when they click your ad. It can include
third-party redirection and tracking code. If you enter a value, it overrides the base URL for the ad.

Once you save the record, the base URL includes any append parameters configured for the campaign or account.

If you use the Adobe Advertising conversion tracking service and the campaign settings include using the [!UICONTROL EF Redirect] and adding tracking at the keyword level, then Search, Social, & Commerce automatically adds its own click-tracking code.

>[!MORELIKETHIS]
>
>* [Manage keywords](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
