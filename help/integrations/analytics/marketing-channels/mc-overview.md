---
title: Fundamentals of [!DNL Marketing Channels]
description: Learn key information about [!DNL Analytics Marketing Channels] that [!DNL Analytics for Advertising] users should understand.
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
---
# Fundamentals of [!DNL Analytics Marketing Channels]

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

This page explains key information about [!DNL Analytics Marketing Channels] that [!DNL Analytics for Advertising] users need to understand.

For full documentation on [!DNL Marketing Channels], see "[Get Started with [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html)."

## Overview of [!DNL Marketing Channels]

[!DNL Marketing Channels] are a key feature of Adobe Analytics. [!DNL Marketing Channels] reports show how customers arrive to your website over the reporting window and how each channel impacts revenue or on-site behavior.

Consider the following example of a cross-visit journey. Each visit to your website is indicated by the marketing channel from which the visitor entered. The first visit, also referred to as the First Touch Channel, is Email. Display on visit two is a participating channel, and Natural Search is considered the Last Touch Channel. If you use [!UICONTROL Last Touch Attribution] within [!UICONTROL Attribution IQ], Natural Search would receive full credit for the $250 conversion event. Using the Experience Cloud ID Service, you can tie these individual visits together to reveal one journey by a single visitor.

![Example cross-visit conversion journey in Marketing Channels](/help/integrations/assets/a4adc-mc-sample-journey.png)

By using [!UICONTROL Marketing Channels] Processing Rules, you can create sets of logic to determine the channels that drive traffic and to track each channel as users comes to your site. For example, the [!UICONTROL Email] channel would be indicated by a unique tracking code generated upon click that, when logged by Adobe Analytics, would categorize the visit as originating from an email marketing campaign.

## Processing Rules and How Marketing Channels are Set

Each time a user comes to a website, they do so through a URL that they either clicked or directly typed into the address bar. When the user enters the website, [!DNL Analytics] tracks information that can be used to determine the channel that drove the visit.

Often, marketers append query string parameter tracking codes to channel URLs to help track the impact of the channel on their site. You can configure [!DNL Marketing Channels] processing rules to listen for specific tracking parameters and values to determine the channel without any additional tracking. For example, if all email campaign URLs follow the format `www.adobe.com?cid=email…` (where the URL contains the query string parameter and value `cid=email`), then you can create a rule to listen for this tracking code and to bucket the visit in the [!UICONTROL Email] channel.

Other channels don't have trackable URL paths and need further logic for identification. For example, [!UICONTROL Earned Social], in which a user clicks a link that another user shared organically on a social network, is an important channel to track. However, the marketer has no way to append a query string parameter tracking code to the URL that's shared. In this case, you could create a processing rule to listen for the referring domain of social networks of interest and the absence of paid tracking codes to determine the channel. The visits that meet these requirements would then be tracked as Earned Social within the Marketing Channels report.

Adobe recommends working with your analytics team to build a comprehensive set of [!DNL Marketing Channels] processing rules to track all channels that are pertinent to your business. Doing so allows you to create powerful attribution reporting.

To understand how Adobe Advertising can contribute to the signals necessary to create custom marketing channels, see "[Using Advertising IDs to Create [!DNL Marketing Channels] Rules](mc-ids.md)."

>[!MORELIKETHIS]
>
>* [Using Adobe Advertising IDs to Create [!DNL Marketing Channels] Processing Rules](mc-ids.md)
>* [Why Channel Data Can Vary Between Adobe Advertising and [!DNL Marketing Channels]](mc-data-variances.md)
>* [Using [!DNL Analytics Marketing Channels] with Adobe Advertising Data](mc-ac-data.md)
>* [Video: Using [!DNL Marketing Channels] for Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Overview of [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
