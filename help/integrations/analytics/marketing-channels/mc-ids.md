---
title: Using Adobe Advertising IDs to Create [!DNL Marketing Channels] Rules
description: Learn how to use Adobe Advertising IDs to create processing rules for [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
---
# Using Adobe Advertising IDs to Create [!DNL Marketing Channels] Processing Rules

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

You can use Adobe Advertising IDs ([AMO ID and EF ID](../ids.md)) to configure [!DNL Marketing Channels] processing rules in Adobe Analytics. Use Adobe Advertising IDs for rules specific to your Adobe Advertising campaigns. The order in which you process the rules determines whether all possible data is captured correctly.

## The AMO ID in Processing Rules

The AMO ID is the primary tracking code used to report Adobe Advertising data within [!DNL Analytics]. The AMO ID is a concatenation of dynamic values managed by Adobe to provide granular reporting within [!DNL Analytics]. It's stored in an [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) or rVar dimension (AMO ID). The AMO ID can be set in [!DNL Analytics] in two ways:

* Click-through tracking: Adobe Advertising sets the `s_kwcid` query string parameter in a link, and [!DNL Analytics] picks up the parameter from the landing page URL when a click-through occurs.

* View-through tracking ([!DNL DSP] Only): The Last Event Service detects a view-through on the server side and sends the AMO ID to [!DNL Analytics]. In this case, the URL doesn't contain a `s_kwcid` parameter.

The dynamic values within AMO IDs indicate the marketing channel that was tracked:

* The prefix in the AMO ID can be used to identify the top-level channel within [!DNL Marketing Channels].

* Character phrases in the body of the AMO ID indicate a more specific campaign type.

* The suffix "vt" is present for [!DNL DSP] view-through traffic and can be used to create separate click-through and view-through [!DNL DSP] channels.

The rest of the AMO ID can be ignored.

| [!UICONTROL AMO ID] | Channel | Rule Logic |
|--------|---------|--------------------|
| !ctv (suffix) | [!UICONTROL DSP Connected TV ViewThrough] | Ends With |
| !d! (body) | [!UICONTROL Display Network] | Contains |
| !g! (body) | [!UICONTROL Google Search] | Contains |
| !s! (body) | [!UICONTROL Search Partner] | Contains |
| !u! (body) | [!UICONTROL Smart Shopping Campaign] | Contains |
| !ytv! (body) | [!UICONTROL YouTube Video Ad] | Contains |
| !yts! (body) | [!UICONTROL YouTube Search Ad] | Contains |
| !vp! (body) | [!UICONTROL Google Video Partners] | Contains |
| !vt (suffix) | [!UICONTROL DSP ViewThrough] | Ends With |
| AL! (prefix) | [!UICONTROL Paid Search] | Starts With |
| AC! (prefix) | [!UICONTROL DSP Display] | Starts With |

### Examples of Processing Rules that Use the AMO ID

The [!DNL Marketing Channels] processing rule for the [!UICONTROL Paid Search] channel might look like this:

![Example of a [!UICONTROL Paid Search] rule](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

The [!DNL Marketing Channels] processing rule for the [!UICONTROL YouTube Video Ads] channel might look like this:

![Example of a [!UICONTROL YouTube Video Ads] rule](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Be sure to run your rules in order of specificity. If the above two rules ran in order, the [!DNL YouTube] video ad traffic would all fall under the [!UICONTROL Paid Search] channel because the AMO ID would both start with "AL!" and contain "!ytv!".

## The EF ID in Processing Rules

The AMO EF ID (EF ID) is the second tracking code used in the [!DNL Analytics for Advertising] integration. Its primary purpose is to track and pass [!DNL Analytics] event data into Adobe Advertising. Every time a click-through or a view-through occurs, a unique EF ID is generated, even if it is the exact same ad for the same visitor. The EF ID is not used in the [!DNL Analytics] reporting user interface because it typically exceeds the 500k unique values per variable limit in [!DNL Analytics], making it unusable for reporting. The Adobe Advertising metrics and metadata are not applied to the EF ID; they are applied only to the AMO ID. The added granularity of tracking is required for campaign optimization in Adobe Advertising, so both IDs are required.

Although the EF ID dimension isn't used directly in [!DNL Analytics] reporting, the EF ID can be useful in creating marketing channels. The EF ID suffix indicates the channel (display or search) and whether the visit was driven by a click-through or a view-through. The delimiter in the EF ID is a colon, rather than the exclamation point in the AMO ID.

| EF ID Suffix | Channel |
|-------|---------|
| :s | [!UICONTROL Paid Search Click-through] |
| :d | [!UICONTROL Display ClickThrough] |
| :i | [!UICONTROL Display ViewThrough] |

### Examples of Processing Rules that Use the EF ID

>[!IMPORTANT]
>
>See "[Order of operations for Marketing Channels rules](#rule-order)" for information about the order in which your rules should be processed.

#### Paid Search Rule

The best practice is to include two conditions with the "Any" operator for a [!UICONTROL Paid Search] rule:

* Cost/click/impression data contains the AMO ID, so include the AMO ID. The AMO ID should start with "AL!" to correctly allocate click/cost/impression data to [!UICONTROL Paid Search].<!-- Is this just called AMO ID there, not s_kwcid=XXX? What's the difference? -->

* The URLs for [!UICONTROL Paid Search] click-throughs always include the `s_kwcid` query string parameter, so include it to ensure proper de-duplication occurs if the visitor navigates back to the landing page. Include "AL!" before the `s_kwcid` to correctly allocate click/cost/impression data to [!UICONTROL Paid Search].

Don't set the channel's value to the AMO ID. Instead, set it to something such as the Referring Domain, Search Engine + Keyword, or Page. (This is relevant for all the [!DNL Marketing Channels]).

<!-- Explain that comment about relevancy -- do I need to repeat this for each rule example?  -->

![Example of a Paid Search rule](/help/integrations/assets/a4adc-mc-rule-paid-search.png)

#### Natural Search Rule

For [!UICONTROL Natural Search], ensure that your [[!UICONTROL Paid Search] detection rules](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/t-paid-search-detection) include the `ef_id` and `s_kwcid` query string parameters. (Typically, this is automatically configured when Advertising Search, Social, & Commerce is integrated into [!DNL Analytics], but verify in case an [!DNL Analytics] administrator changed the logic after the integration was configured.)

Set the rule to "Matches Natural Search Detection Rules" (which is usually the default setting for this channel).

![Example of a Natural Search rule](/help/integrations/assets/a4adc-mc-rule-natural-search.png)

#### Display ClickThrough Rule

Create a Display ClickThrough marketing channel by capturing only click-throughs. Because the AMO ID is the same for both click-throughs and view-throughs, this rule uses the EF ID variable and the `ef_id` query string parameter.

Sometimes click-throughs are tracked through the URL (the default). In other cases, click-throughs are tracked through the Last Event Service on the server side, and therefore the URL doesn't contain the `ef_id` parameter. The rule therefore checks for conditions in which the EF ID variable or the `ef_id` query string parameter ends with ":d". Use the "`Any`" operator because you want this rule to be triggered for either condition.

![Example of a first Display ClickThrough rule](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Display ClickThrough Rule #2

For the second Display ClickThrough rule, set **AMO ID starts with "AC!"**. This second rule exists to capture the click/cost/impression data for the Display channel that comes in directly from Adobe Advertising to [!DNL Analytics]. This data is attributed to an AMO ID but doesn't include an URL with the `ef_id` query string, so these hits aren't connected with an AMO EF ID, which is what the first Display ClickThrough rule captures.

![Example of a second Display ClickThrough rule](/help/integrations/assets/a4adc-mc-rule-display-ct2.png)

#### Display ViewThrough Rule

To create a Display ViewThrough channel, create a rule in which the EF ID ends with ":i". Because the visitor didn't click the ad, the view-through tracking doesn't include the `ef_id` or `s_kwcid` in the URL, and the rule requires only one condition.

![Example of a Display ViewThrough rule](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

## Display CTV ViewThrough Rule

To track [!DNL DSP] connected TV (CTV) view-throughs, create a rule where the AMO ID ends with `"!ctv"`. Because the visitor didn't click the ad, the view-through tracking doesn't include the `ef_id` or `s_kwcid` in the URL, and the rule requires only one condition.

![Example of a Display CTV ViewThrough rule](/help/integrations/assets/a4adc-mc-rule-display-ctv-vt.png)

### Natural Referring Domains Rule

(Optional) The best practice is to add an "Is First Page of Visit" condition with the "Any" operator to the standard [!UICONTROL Natural Referring Domains] rule. While this rule is optional, it can help prevent the edge case of natural referrers being set when the user clicks the back button to return to the landing page.

![Example of a Natural Referring Domains rule](/help/integrations/assets/a4adc-mc-rule-natural-referring-domains.png)

## Order of operations for Marketing Channels rules {#rule-order}

![alt text](image.png)

* Put [!UICONTROL Paid Search] *before* [!UICONTROL Natural Search]. Otherwise, paid search data may be allocated to natural search.

* Put the first [!UICONTROL Display ClickThrough] *before* [!UICONTROL Natural Referring Domains] and [!UICONTROL Natural Social].

* When you use [!UICONTROL CTV view-throughs], put it *before* [!UICONTROL Display ViewThroughs]. Otherwise, CTV view-throughs will be captured as Display ViewThroughs.

* Put [!UICONTROL Display ViewThroughs] *after* other channels but before [!UICONTROL Internal] and [!UICONTROL Direct] because it's possible that a view-through and a non-[!DNL Advertising] click-through can occur in the same landing event. For example, a visitor may sees an Adobe Advertising ad, get an impression, and then go to the site through [!UICONTROL Natural Search].

  The best practice is to prioritize the other channels (except [!UICONTROL Internal] and [!UICONTROL Direct]) over view-throughs.

* Some advertisers may opt to prioritize [!UICONTROL Display ViewThroughs] over [!UICONTROL Natural Referring Domains]. Do this by swapping the processing order of the two rules.

* The **second** [!UICONTROL Display ClickThrough] rule is there to catch the click/cost/impression data that comes in directly from Adobe Advertising to [!DNL Analytics]. Since this data is only attributed to an AMO ID, these hits aren't connected with an AMO EF ID. If you don't set this rule, all click/cost/impression data falls under the [!UICONTROL Direct] channel, which is the default channel for any data that doesn't match a [!DNL Marketing Channel]. This rule must come *after* the view-through rule or it will pick up any view-throughs.

>[!MORELIKETHIS]
>
>* [Fundamentals of [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Why Channel Data Can Vary Between Adobe Advertising and [!DNL Marketing Channels]](mc-data-variances.md)
>* [Using [!DNL Analytics Marketing Channels] with Adobe Advertising Data](mc-ac-data.md)
>* [Video: Using [!DNL Marketing Channels] for Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe Advertising IDs Used by [!DNL Analytics]](/help/integrations/analytics/ids.md)
