---
title: "[!DNL Adobe] [!DNL Audience Analytics] for Adobe Advertising customers"
description: Learn how to use [!DNL Adobe] [!DNL Audience Analytics] for advertising use cases
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
TQID: https://experienceleague.adobe.com/XFaacUNElL25w5SMS5fzWkfRwnXr2WxhsBLe3sTccg4
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: f2860a4b-f905-4545-bead-1bbc92564592
    internal-label: Advertising integrations
subfeature_v2:
  - id: d1e2786d-1070-4f97-93d7-f5b95de25b2b
    internal-label: Audience Manager integration
  - id: d9510790-d834-436d-8423-8d69cd50464a
    internal-label: DSP Ads
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---
# [!DNL Adobe] [!DNL Audience Analytics] for Adobe Advertising customers

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) is an integration between Adobe Audience Manager and Adobe Analytics that allows Audience Manager customers to send segments to [!DNL Analytics] for enriched insights about site activity. 

Adobe Advertising customers can benefit by using [!DNL Audience Analytics]. The integration allows you to:

* Send Adobe Advertising exposure data directly to [!DNL Analytics] to determine the impact of upper funnel activity on downstream site activity.

* Determine the marketing channels and site entry points from upper funnel exposure ads.

* Layer the integration with [!DNL Analytics for Advertising] to incorporate third-party demographic segments from [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) with [!DNL Analytics for Advertising] data for more insights about user profiles. 

  [!DNL Audience Marketplace] provides access to third-party data feeds with "Activation" subscription models, which allow buyers to send data to a destination. If the data is used within an [!DNL Analytics] destination, then activation fees aren't applied.

* (Advertisers with Advertising DSP) Add additional exposure segments for holistic journey management insights.

  Advertising DSP can send exposure data to Audience Manager as actionable signals through the implementation of either Adobe Experience Platform or Audience Manager impression-tracking pixels. Forwarding the same data to [!DNL Analytics] enables advanced data analysis. See "[Overview of sending DSP media exposure data to Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)" for more information.

For more information about [!DNL Audience Analytics], including its prerequisites and workflow, see "[Audience Analytics overview](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)."

## Examples of how to use [!DNL Audience Analytics] data with Adobe Advertising data

The following are examples of how you can use the combined data within [!DNL Analytics] [!DNL Analysis Workspace].

### See the impact of upper funnel activity on downstream activity

Use Audience Manager exposure segments to see the impact of upper funnel site activity on downstream site activity. Include Adobe Advertising or third-party macro IDs in your tracking pixels to track the impact on a detailed level, from the campaign level down to the level of the site on which the user was exposed.

Main benefits: 

* Track exposure by funnel/ad types and use [!DNL Audience Analytics] to determine entry rates and overlap with the next phase of the customer journey.

* Determine the impact of upper funnel activity on downstream site activity.

* Connect [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> and [!DNL Audience Analytics] data to determine a holistic journey to the site.

<!-- (which includes the user's last exposure event) -->

The following are examples of reports that you can create in [!DNL Analysis Workspace].

![See the impact of upper funnel activity on downstream site activity](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Use [!DNL Audience Analytics] third-party segment data for user profile analysis

Use third-party Audience Manager segments for a richer analysis of how users are interacting with your site. You can use the information to determine new third-party audiences for which to activate media, based on how profiles from the third-party segments engage with key performance indicators for the media campaigns' sites.

>[!TIP]
> Use the Audience Manager `Audiences ID` and `Audiences Name` dimensions throughout [!DNL Analytics], like any other dimensions that [!DNL Analytics] collects.

The following are examples of reports that you can create in [!DNL Analysis Workspace].

![Using third-party segments to enrich user profile analysis](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe Advertising integrations with Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
