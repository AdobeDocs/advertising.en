---
title: About programmatic guaranteed deals
description: Learn about programmatic guaranteed (PG) deals and which SSPs are certified to provide them.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 47c89d8a-f45f-4fcb-84a6-031f7d7f580f
TQID: https://experienceleague.adobe.com/LJPeIv8z6DiQS-eCe8obWgKkWi5onwpBadIgElLzkXw
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
subfeature_v2:
  - id: ac506c20-96f2-48f6-9096-77706e336bda
    internal-label: DSP Private Inventory
  - id: fae3ff5f-9a75-4de1-a100-c90dd8268528
    internal-label: DSP Deal IDs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
---
# About programmatic guaranteed deals

A programmatic guaranteed (PG) deal is a guaranteed buy directly with a publisher via a deal ID (rather than via ad server tags). PG is more flexible for you and your publisher to manage, and it provides more transparency than regular tag buys. Billing and reporting are consolidated through DSP, which saves you time.

## Features of a PG deal

* The deal is always billed through DSP.
* The deal has a fixed price and quantity.
* The publisher or supply side platform (SSP) handles all budget pacing, budget capping, and any targeting.
* Typically, the deal has a higher priority in publisher’s ad server.
* Bid requests aren't exclusive to a single deal or buyer.
* Multiple types of video are supported on a single deal ID.
* Publisher-managed ads are accepted via [!DNL Google Authorized Buyers] SSP.
* The SSPs and publishers have delivery SLAs.

PG deals require a PG default placement and ads (or a 1x1 pixel for publisher-managed ads) so DSP can return a request to each bid request and fulfill delivery SLAs with the SSPs. Once you set up the mandatory PG default placement, you can also target the PG deal in other placements.

## SSPs certified for PG deals in DSP

* [!DNL Ambient Digital]
* [!DNL FreeWheel]
* [!DNL Google Authorized Buyers]
* [!DNL Magnite CTV] (formerly [!DNL Telaria])
* [!DNL Magnite DV+] (formerly [!DNL Rubicon])
* [!DNL OpenX]
* [!DNL SpotX]

>[!MORELIKETHIS]
>
>* [Tips for negotiating a programmatic guaranteed deal](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Set up a programmatic guaranteed deal](programmatic-guaranteed-set-up.md)
>* [SSP partners](ssp-partners.md)
>* [Overview of inventory features in Advertising DSP](inventory-overview.md)
