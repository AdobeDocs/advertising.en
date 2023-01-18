---
title: '[!DNL Adobe] [!DNL Audience Analytics] for Adobe Advertising Customers'
description: Learn how to use [!DNL Adobe] [!DNL Audience Analytics] for advertising use cases
feature: Integration with Adobe Audience Manager
exl-id: e05ba560-d3d5-4024-b1ba-956e878a2578
---
# [!DNL Adobe] [!DNL Audience Analytics] for Adobe Advertising Customers

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) is an integration between Adobe Audience Manager and Adobe Analytics that allows Audience Manager customers to send segments to [!DNL Analytics] for enriched insights about site activity. 

Adobe Advertising customers can benefit by using [!DNL Audience Analytics]. The integration allows you to:

* Send Adobe Advertising exposure data directly to [!DNL Analytics] to determine the impact of upper funnel activity on downstream site activity.

* Determine the marketing channels and site entry points from upper funnel exposure ads.

* Layer the integration with [!DNL Analytics for Advertising] to incorporate third-party demographic segments from [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) with [!DNL Analytics for Advertising] data for more insights about user profiles. 

    [!DNL Audience Marketplace] provides access to third-party data feeds with “Activation” subscription models, which allow buyers to send data to a destination. If the data is used within an [!DNL Analytics] destination, then activation fees aren't applied.
  
* (Advertisers with Advertising DSP) Add additional exposure segments for holistic journey management insights.

    Advertising DSP can send exposure data to Audience Manager as actionable signals through the implementation of either Adobe Experience Platform or Audience Manager impression-tracking pixels. Forwarding the same data to [!DNL Analytics] enables advanced data analysis. See "[Overview of Adobe Advertising Media Data Integration with Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)" for more information.
  
For more information about [!DNL Audience Analytics], including its prerequisites and workflow, see "[Audience Analytics overview](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)."

## Examples of How to Use [!DNL Audience Analytics] Data with Adobe Advertising Data

The following are examples of how you can use the combined data within [!DNL Analytics] [!DNL Analysis Workspace].

### See the Impact of Upper Funnel Activity on Downstream Activity

Use Audience Manager exposure segments to see the impact of upper funnel site activity on downstream site activity. Include Adobe Advertising or third-party macro IDs in your tracking pixels to track the impact on a detailed level, from the campaign level down to the level of the site on which the user was exposed.

Main benefits: 

* Track exposure by funnel/ad types and use [!DNL Audience Analytics] to determine entry rates and overlap with the next phase of the customer journey.

* Determine the impact of upper funnel activity on downstream site activity.

* Connect [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> and [!DNL Audience Analytics] data <!-- (which includes the user's last exposure event) --> to determine a holistic journey to the site.
 
The following are examples of reports that you can create in [!DNL Analysis Workspace].

![See the impact of upper funnel activity on downstream site activity](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)
 
### Use [!DNL Audience Analytics] Third-Party Segment Data for User Profile Analysis

Use third-party Audience Manager segments for a richer analysis of how users are interacting with your site. You can use the information to determine new third-party audiences for which to activate media, based on how profiles from the third-party segments engage with key performance indicators for the media campaigns' sites.

>[!TIP]
> Use the Audience Manager `Audiences ID` and `Audiences Name` dimensions throughout [!DNL Analytics], like any other dimensions that [!DNL Analytics] collects.

The following are examples of reports that you can create in [!DNL Analysis Workspace].

![Using third-party segments to enrich user profile analysis](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe Advertising Integrations with Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
