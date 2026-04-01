---
title: About account-level and advertiser-level blocked sites lists
description: Learn more about the blocked sites list for an account or advertiser.
role: User, Admin
exl-id: e147159b-54f2-492b-8dbc-054b97897fa6
TQID: https://experienceleague.adobe.com/qCoAB-qGFmDI7N3bHPOI2TukZB2HVode2SFVo4G3l-Y
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
---
# About account-level and advertiser-level blocked sites lists

You can edit the blocked sites list used for the entire DSP account and additional lists for individual advertisers in the account.

Blocked sites lists define sets of targets to exclude for your placements. Each list can consist of top-level website domains and any level of sub-domains (such as example.com, my.example.com, or my.new.example.com) and mobile app IDs or package names (such as com.example.app123).

Advertiser-level lists override account-level lists.

>[!NOTE]
>
>* Account-level and advertiser-level blocked site lists are applied in addition to the DSP [globally blocked site list](/help/dsp/introduction/features/brand-safety-media-quality.md#global-blocked-sites), which include sites deemed unsafe for ads.
>* Users can also add targeted sites to any placement.
>* Blocked sites lists always override targeted sites lists. If a placement both excludes and includes the same target for an ad, then the target is excluded.

>[!MORELIKETHIS]
>
>* [Edit an account-level or advertiser-level blocked sites list](/help/dsp/admin/blocked-sites-list-edit.md)
>* [Brand safety and media quality](/help/dsp/introduction/features/brand-safety-media-quality.md)
>* [Placement settings](/help/dsp/campaign-management/placements/placement-settings.md)
