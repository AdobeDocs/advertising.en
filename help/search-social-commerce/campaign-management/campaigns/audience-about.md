---
title: About audiences
description: Learn about options to track, create, and manage [!DNL Google Ads] and [!DNL Microsoft® Advertising] audiences.
exl-id: 34169650-9820-4b7d-9ae6-09ff8a8c6f2e
feature: Search Campaign Management
---
# About managing [!DNL Google Ads] and [!DNL Microsoft® Advertising] audiences in Search, Social, & Commerce

*[!DNL Google Ads] and [!DNL Microsoft® Advertising] only*

The Audiences Library lists all of your [!DNL Google Ads] customer data-based, in-market, and similar audiences and your [!DNL Microsoft® Advertising] remarketing and dynamic remarketing, custom, customer match, in-market, and similar audiences. You can use any of the [!DNL Google Ads] audiences as [!DNL Google Ads] campaign-level and ad group-level targets and exclusions, and you can use any of the [!DNL Microsoft® Advertising] audiences as [!DNL Microsoft® Advertising] campaign-level and ad group-level targets and (dynamic remarketing audiences only) exclusions. You can add or edit a bid adjustment for any audience target.

You can also create and manage audiences using segments or email lists from your existing Adobe Experience Cloud audiences and from various kinds of customer data from your customer relationship management (CRM) system:

* **Adobe audience segments:** Advertisers with opted-in Adobe Audience Manager or Adobe Analytics accounts can create [!DNL Google Ads] customer match audiences from their [!DNL Adobe] segments:

  * (Advertisers with [!DNL Analytics] accounts who don't also have Audience Manager) You can create [!DNL Google Ads] customer match audiences using user IDs from [!DNL Analytics] segments that are shared with Adobe Experience Cloud.
  
  * (Advertisers with Audience Manager accounts) You can create [!DNL Google Ads] customer match audiences using user IDs from Audience Manager segments that have Search, Social, & Commerce as a destination. This may include Adobe Analytics segments that are published to Adobe Experience Cloud and segments created using the Adobe Experience Cloud Audience Library.

  To create customer match audiences, the advertiser's [!DNL Google Ads] account must be [eligible for custom match](https://support.google.com/adspolicy/answer/6299717) and opted in for [user ID segments](https://support.google.com/google-ads/answer/9199250). Also, the advertiser account in Search, Social, & Commerce must be configured to allow the creation of customer match audiences.<!-- For Analytics audiences: Analytics Only Integration. For Audience Manager, Enable CM/CRM option) -->
  
  [!DNL Adobe] segment data and cookie sync files for customer data-based audiences are synced to [!DNL Google Ads] daily.

* **Adobe Campaign email lists:** Your Adobe Account Team can help you set up a workflow to create and update a [!DNL Google Ads] customer match audience from an email list within [!DNL Campaign].

* **Customer data lists:** Advertisers with [!DNL Google Ads] or [!DNL Microsoft® Advertising] accounts that are eligible for customer match can create and update an ad network-specific customer data-based audience <!-- or dynamic remarketing audience -- included in customer data-based audience, at least for [!DNL Google Ads]?--> by uploading a CSV file with primary identifiers.

* **Dynamic remarketing lists:** Advertisers with [!DNL Microsoft® Advertising] accounts can create and manage dynamic remarketing audiences, which you can use to retarget potential customers who have recently interacted with your products in one of multiple ways (such as product viewers or past buyers). Dynamic remarketing audiences require you to use the ad network's JavaScript conversion- and audience-tracking tag on your webpages. Use dynamic remarketing lists with shopping campaigns on the search and audience networks to retarget audiences with product ads, as well as with search campaigns to retarget audiences with text ads and dynamic search ads. <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >Bid modifiers for dynamic remarketing audience targets aren't optimized in portfolios with the "[!UICONTROL Auto-optimize Bid Adjustment Values]" setting.

>[!NOTE]
>
>Search, Social, & Commerce doesn't store any of the customer data you upload or from the [!DNL Adobe] segments used to create or edit a [!DNL Google Ads] or [!DNL Microsoft® Advertising] audience.

>[!MORELIKETHIS]
>
>* [Create [!DNL Google Ads] customer match audiences from [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [Create a [!DNL Google Ads] customer match audience from an Adobe Campaign email list](google-audience-from-campaign-email-list.md)
>* [Manage customer match audiences using customer data lists](audience-from-customer-data-list.md)
>* [Manage dynamic remarketing audiences](audience-dynamic-remarketing-manage.md)
>* [Manage audience targets for campaigns and ad groups](audience-targets-manage.md)
>* [Manage audience exclusions for campaigns and ad groups](audience-exclusions-manage.md)
