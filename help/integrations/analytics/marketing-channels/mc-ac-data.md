---
title: Using [!DNL Marketing Channels] with Adobe Advertising Data
description: Learn how to use Adobe Advertising data in [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
---
# Using [!DNL Analytics Marketing Channels] with Adobe Advertising Data

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

By using both Adobe Advertising and [!DNL Analytics Marketing Channels] reports, you can gain valuable insight into how your digital media influences site activity.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

The following illustration shows how Adobe Advertising and [!DNL Marketing Channels] track the individual visits that comprise one visitor's journey. Adobe Advertising reports in [!DNL Analytics] are limited to only paid display, search, social, and commerce channel advertising trafficked through Adobe Advertising, using the AMO ID. However, [!DNL Marketing Channels] tracks all channels configured in the [!DNL Marketing Channels] Processing Rules.

![How Adobe Advertising and [!DNL Marketing Channels] track the individual visits in a visitor's journey](/help/integrations/assets/a4adc-mc-sample-journey2.png)

In the first visit, the user entered the website through an email campaign, executed ten page views, and then left. In the second visit, the user entered the site via a display ad, executed ten page views, and then left. In the third visit, the user entered the site via natural search, executed five page views, executed a $250 conversion, and the left. Notice the difference in tracking between [!DNL Marketing Channels] and Adobe Advertising. The only channel that Adobe Advertising tracks in this journey is [!UICONTROL Display]. Adobe Advertising tracks the [!UICONTROL Display] channel visit and attributes the subsequent engagement data (such as page views) and conversions back to that advertisement's influence. [!DNL Marketing Channels], on the other hand, gives a full view of all channels.

Because the AMO ID persists through the visitor’s journey, you can use the AMO ID data to see how Adobe Advertising influences other marketing channels. The AMO ID [persists for 60 days by default](/help/integrations/analytics/overview.md), but you can configure the persistence as needed.

## How to Combine Adobe Advertising and Marketing Channels Data to Analyze Media Performance

Within [!DNL Analytics], you can combine the Adobe Advertising persisting paid advertising data and the [!DNL Marketing Channels] comprehensive visit data to better analyze your media performance so you can better influence the customer journey.

The following analysis uses the Adobe Advertising data to show different versions of how a display advertisement impacts site conversion. All three columns use the same conversion metrics, but each column tells a different story:

* Column 1 looks at the AMO ID data that's persistent across the visitor’s journey. Column 1 indicates that 641 Applications Starts were, at one point, linked with an Adobe Advertising ad, either through a view-through or a click-through event. This view doesn't take any other [!DNL Marketing Channels] attribution into consideration.

* In the [!DNL Marketing Channels] data set, however, the 641 Applications Starts are attributed to other marketing channels. The last two columns take the 641 Applications Starts and limit the data to the [!UICONTROL Display Click-Through] and [!UICONTROL Display View-Through] channels, showing the conversions that occur in a last touch attribution model.

![example of how a display ad impacts site conversion](/help/integrations/assets/a4adc-mc-display-impact.png)

You can take this analysis one step further. You can break down the Adobe Advertising row further by marketing channel to see where the Adobe Advertising conversions are attributed to the 641 Applications Starts. You already know that five of those conversions are attributed to a last touch Display Click-through and 19 are attributed to a last touch Display View-through. That still leaves 617 Applications Starts attributed to other marketing channels. You can drag and drop the Last Touch Channel dimension on top of the Advertising DSP line item to reveal the channel attribution for the rest of the Applications Starts and show the cross-channel impact of the Display channel.

![how to add the Last Touch Channel dimension](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Now you can see how the remaining Applications Starts are attributed. Email is given credit for 357 last touch Applications Starts for which an AMO ID persisted. Using this type of analysis, you can see the impact that Adobe Advertising display ads had across all channels. With only one data set and attribution model, this type of insight wouldn't be available.

![example of the cross-channel impact of the Display channels](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

You can improve the analysis further by using a Stack Graph set to "100% stacked" to show trended data over time. This visualization makes it easier to monitor which last touch marketing channels are more heavily impacted by your display marketing campaigns.

![example of the trended cross-channel impact of the Display channels](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Fundamentals of [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Using Adobe Advertising IDs to Create [!DNL Marketing Channels] Processing Rules](mc-ids.md)
>* [Why Channel Data Can Vary Between Adobe Advertising and [!DNL Marketing Channels]](mc-data-variances.md)
>* [Video: Using [!DNL Marketing Channels] for Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Overview of [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
