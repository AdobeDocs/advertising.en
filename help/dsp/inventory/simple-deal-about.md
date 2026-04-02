---
title: About [!UICONTROL Simple Ad Serving]
description: Learn about [!UICONTROL Simple Ad Serving] deals using event-tracking pixels.
feature: DSP Simple Ad Serving
exl-id: 327a2c93-d729-42e1-856f-f0e05efab7ca
TQID: https://experienceleague.adobe.com/w4KFePatd7CZ1xC8dd1CItl88-6myAZw8TuatHzHnRI
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
    internal-label: DSP Ads
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
---
# About [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] provides guaranteed, non-decisioned ad delivery and reporting for a specified publisher and a single ad type using a single, dedicated placement. Use [!DNL Simple Ad Serving] when your publisher can't execute your deal via deal IDs. All targeting, budget pacing and capping, and frequency capping is handled by the publisher. Execute these deals via event-tracking pixels.

With [!UICONTROL Simple Ad Serving], each ad is served directly by the publisher (site serve), and DSP provides an event-tracking pixel to send to the publisher, who must implement the pixel and traffic the DSP ads. Depending on the inventory type, the event pixels measure impression, click-through, and video played events.

The following ad types are available:

* desktop standard pre-roll
* tablet and mobile standard pre-roll
* connected TV standard pre-roll
* display
* audio

You can create a [!UICONTROL Simple Ad Serving] deal in the [!UICONTROL Inventory] > [!UICONTROL Deals] view. DSP automatically generates a placement with the subtype "[!DNL Simple ad serving]" for the ad. The placement targets the deal but doesn't allow additional targeting, budget, or frequency capping. You can edit only some of the deal settings, such as the deal name, CPM, impressions, and flight dates.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] placements don't comply with the account's usable funds or the campaign and package budgets. However, spend is tracked and counted toward those budgets. Even when the CPM is $0, event data is always tracked.

>[!MORELIKETHIS]
>
>* [Create a [!UICONTROL Simple Ad Serving] deal](simple-deal-create.md)
>* [Edit [!UICONTROL Simple Ad Serving] deal settings](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] settings](simple-deal-settings.md)
>* [View a detailed report for a deal](/help/dsp/inventory/deal-view-report.md)

<!--
 add back when reimplemented:
>* [View event-tracking pixels for a [!UICONTROL Simple Ad Serving] deal](simple-deal-show-pixels.md)
-->
