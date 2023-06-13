---
title: Integration with Adobe Experience Cloud solutions and services
description: Learn about Search, Social, & Commerce integrations with Adobe Experience Cloud solutions and services.
exl-id: e8b521f5-f426-4c50-9df4-361a047c9ff0
---
# Integration with Adobe Experience Cloud solutions and services

Advertising Search, Social, & Commerce is integrated with the following [!DNL Adobe] products.

* [Tags from Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) &mdash; You can use the [Adobe Advertising Cloud Extension](https://exchange.adobe.com/apps/ec/100155) for Adobe Experience Platform to create Adobe Advertising conversion tracking tags, as well as third-party tracking tags, for your ad landing pages. (You can also [create conversion tracking tags directly within Search, Social, & Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md).) Contact your Adobe Account Team or implementation team for information to include in your tags.

* Adobe Analytics &mdash; (Opt-in feature) Adobe Advertising and [!DNL Analytics] are integrated in the following ways: 

  * Adobe Advertising and [!DNL Analytics] seamlessly share data. [!DNL Analytics] can send site engagement and conversion data daily to Search, Social, & Commerce, where the data is available for ad optimization and for reporting. Also, Adobe Advertising can send ad traffic data &mdash; including impressions, clicks, and cost &mdash; from your ad networks daily to [!DNL Analytics], where the data is available in all reporting tools.
  
    See "[Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md)" for more information about [!DNL Analytics] support for each ad network and ad type. See also "[Overview of [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}" for more information about the data exchange.
  
    To exchange data, both Adobe Advertising and [!DNL Analytics] must be initially configured. Contact your Adobe Account Team for more information about the initial setup.
  
    >[!NOTE]
    >
    >By default, the [!DNL Analytics] metrics aren't visible in Search, Social, & Commerce screens. You must explicitly [make the metrics available in campaign management views, portfolios, and reports](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) after the [!DNL Adobe] implementation team has configured selected standard or custom events to pass into Adobe Advertising. You can optionally change the displayed metric names (without changing them in [!DNL Analytics]). You can make metrics viewable in the UI and rename metrics from [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. 

  * Advertisers with [!DNL Analytics] but not Audience Manager can [create [!DNL Google Ads] customer match audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) from [!DNL Analytics] segments that are shared with Adobe Experience Cloud. To be eligible, an advertiser must implement the [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) and deploy a tag on its websites. You can then use the audiences in [!DNL Google Ads] campaigns as campaign-level or ad group-level [targets](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) or [exclusions](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* Adobe Audience Manager segments &mdash; (Opt-in feature) You can [create [!DNL Google Ads] customer match audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) from Audience Manager segments that have Search, Social, & Commerce as a destination. This may include [!DNL Analytics] segments that are published to Adobe Experience Cloud and segments that are created using the Adobe Experience Cloud Audience Library. You can then use the audiences in [!DNL Google Ads] campaigns as campaign-level or ad group-level [targets](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) or [exclusions](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

  See "[Adobe Advertising Integrations with Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)" for more information.

* Adobe Target &mdash; You can implement click-through signal sharing between Search, Social, & Commerce and [!DNL Target], set up an A/B test activity in [!DNL Target] for your ads, and then use [!DNL Analytics] Analysis Workspace to view the test data.

* Adobe Campaign &mdash; You can [create and update a [!DNL Google Ads] customer match audience using an email list within [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Adobe Experience Cloud Notifications &mdash; (When you're logged in through Adobe Experience Cloud) From the notifications link ([Alert Notifications](/help/search-social-commerce/assets/notifications-panel.png "Alert Notifications")) at the top of each page, you can view all Adobe Experience Cloud system updates, posts, mentions, and assets shared. Contact your Adobe Account Team for information about access to Adobe Experience Cloud.
