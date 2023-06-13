---
title: Using Adobe Advertising IDs to Create [!DNL Marketing Channels] Rules
description: Learn how to use Adobe Advertising IDs to create processing rules for [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
---
# Using Adobe Advertising IDs to Create [!DNL Marketing Channels] Processing Rules

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

You can use Adobe Advertising IDs ([AMO ID and EF ID](../ids.md)) to configure [!DNL Marketing Channels] processing rules in Adobe Analytics. Use Adobe Advertising IDs for rules specific to your Adobe Advertising campaigns.

## The AMO ID in Processing Rules

The AMO ID is the primary tracking code used to report Adobe Advertising data within [!DNL Analytics]. The AMO ID is a concatenation of dynamic values managed by Adobe to provide granular reporting within [!DNL Analytics]. It's stored in an [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) or rVar dimension (AMO ID). The AMO ID can be set in [!DNL Analytics] in two ways:

* Click-through tracking: Adobe Advertising sets the `s_kwcid` query string parameter in a link, and [!DNL Analytics] picks up the parameter from the landing page URL when a click-through occurs.
* View-through tracking ([!DNL DSP] Only): The Last Event Service detects a view-through on the server side and sends the AMO ID to [!DNL Analytics]. In this case, the URL doesn't contain a `s_kwcid` parameter.

The dynamic values within AMO IDs indicate the marketing channel that was tracked:

* The prefix in the AMO ID can be used to identify the top-level channel within [!DNL Marketing Channels].

* Character phrases in the body of the AMO ID indicate a more specific campaign type.

* The suffix “vt” is present for [!DNL DSP] view-through traffic and can be used to create separate click-through and view-through [!DNL DSP] channels.

The rest of the AMO ID can be ignored.

| [!UICONTROL AMO ID] | Channel | Rule Logic |
|--------|---------|--------------------|
| AL! (prefix) | [!UICONTROL Paid Search] | Starts With |
| AC! (prefix) | [!UICONTROL DSP] | Starts With |
| !g! (body) | [!UICONTROL Google Search] | Contains |
| !s! (body) | [!UICONTROL Search Partner] | Contains |
| !d! (body) | [!UICONTROL Display Network] | Contains |
| !u! (body) | [!UICONTROL Smart Shopping Campaign] | Contains |
| !ytv! (body) | [!UICONTROL YouTube Video Ad] | Contains |
| !yts! (body) | [!UICONTROL YouTube Search Ad] | Contains |
| !vp! (body) | [!UICONTROL Google Video Partners] | Contains |
| !vt (suffix) | [!UICONTROL DSP View-through] | Ends With |

### Examples of Processing Rules That Use the AMO ID

The [!DNL Marketing Channels] processing rule for the [!UICONTROL Paid Search] channel might look like this:

![Example of a [!UICONTROL Paid Search] rule](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

The [!DNL Marketing Channels] processing rule for the [!UICONTROL YouTube Video Ads] channel might look like this:

![Example of a [!UICONTROL YouTube Video Ads] rule](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Be sure to run your rules in order of specificity. If the above two rules ran in order, the [!DNL YouTube] video ad traffic would all fall under the [!UICONTROL Paid Search] channel because the AMO ID would both start with “AL!” and contain “!ytv!”.

## The EF ID in Processing Rules

The AMO EF ID (EF ID) is the second tracking code used in the [!DNL Analytics for Advertising] integration. Its primary purpose is to track and pass [!DNL Analytics] event data into Adobe Advertising. Every time a click-through or a view-through occurs, a unique EF ID is generated, even if it is the exact same ad for the same visitor. The EF ID is not used in the [!DNL Analytics] reporting user interface because it typically exceeds the 500k unique values per variable limit in [!DNL Analytics], making it unusable for reporting. The Adobe Advertising metrics and metadata are not applied to the EF ID; they are applied only to the AMO ID. The added granularity of tracking is required for campaign optimization in Adobe Advertising, so both IDs are required.

Although the EF ID dimension isn't used directly in [!DNL Analytics] reporting, the EF ID can be useful in creating marketing channels. The EF ID suffix indicates the channel (display or search) and whether the visit was driven by a click-through or a view-through. The delimiter in the EF ID is a colon, rather than the exclamation point in the AMO ID.

| EF ID Suffix | Channel |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Examples of Processing Rules That Use the EF ID

#### Display Click-through Rule

Create a Display click-through marketing channel by capturing only click-throughs. Because the AMO ID is the same for both click-throughs and view-throughs, this rule uses the EF ID variable and the `ef_id` query string parameter.

Sometimes click-throughs are tracked through the URL (the default). In other cases, click-throughs are tracked through the Last Event Service on the server side, and therefore the URL doesn't contain the `ef_id` parameter. The rule therefore checks for conditions in which the EF ID variable or the `ef_id` query string parameter ends with “:d”. Use the "`Any`" operator because you want this rule to be triggered for either condition.

![Example of a display click-through rule](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Display View-through Rule

To create a Display view-through channel, create a rule in which the EF ID ends with “:i”. Because the visitor didn't click the ad, the view-through tracking doesn't include the `ef_id` or `s_kwcid` in the URL, so the rule requires only one condition.

![Example of a display view-through rule](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Fundamentals of [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Why Channel Data Can Vary Between Adobe Advertising and [!DNL Marketing Channels]](mc-data-variances.md)
>* [Using [!DNL Analytics Marketing Channels] with Adobe Advertising Data](mc-ac-data.md)
>* [Video: Using [!DNL Marketing Channels] for Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe Advertising IDs Used by [!DNL Analytics]](/help/integrations/analytics/ids.md)
