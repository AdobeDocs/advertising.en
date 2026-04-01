---
title: Set up a programmatic guaranteed deal
description: Learn how to set up a programmatic guaranteed (PG) deal you've negotiated with a publisher.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
TQID: https://experienceleague.adobe.com/z7kz7dnCjgCGmlgDlFvbZXTn8d9-OMEunv-Sm-k6TzY
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
---
# Set up a programmatic guaranteed deal

*[Supported supply side platforms only](programmatic-guaranteed-about.md)*

After you negotiate a programmatic guaranteed (PG) deal with a supported publisher, you can set up the deal within DSP either by using the [!DNL Deal ID Inbox] or by manually entering the deal details.

>[!NOTE]
>
> For PG deals, the publisher handles all budget pacing, budget capping, and targeting. All SSPs that allow PG through DSP confirm that the publisher can set up budget capping.
>
> Setting up programmatic guaranteed deals with publishers on [!DNL FreeWheel] requires extra permissions and steps. See "[Overview of setting up programmatic guaranteed deals in [!DNL FreeWheel]](freewheel-overview.md)" for more information.

## Set up a programmatic guaranteed deal using the [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

The following method is the preferred procedure for [!DNL FreeWheel], [!DNL Google Authorized Buyers], and [!DNL Magnite DV+].

1. [Accept the deal](deal-id-inbox-accept.md).

1. After you save the deal, select the ads (or 1x1 tracking pixel for publisher-managed ads) to use for the deal and create a programmatic guaranteed (PG) default placement, as prompted.

   Creating a default PG placement for the deal is mandatory to deliver 100% of your buy. This type of placement has no targeting so DSP can return a bid to every bid request from the publisher.

   * If you're accepting a single deal, you're automatically redirected to the PG default placement creation workflow.

     All [!DNL FreeWheel] deals are proposed as a single deal.

   * If you're accepting a proposal with multiple PG deal IDs, then identify each PG default placement you need to create. Once you create all required placements, the continue button is enabled.

1. (Optional) Target the PG deal in additional PG or non-PG placements by clicking ![Options menu](/help/dsp/assets/options-menu.png) **> [!UICONTROL Attach new placement]**.

    A deal can target multiple placements that support any combination of media types (such as connected TV, desktop, and audio).   

## Manually set up a programmatic guaranteed deal

Use this method for all other SSPs.

1. [Manually set up the deal ID details](deal-id-create.md).

1. After you save the deal, select the ads (or 1x1 tracking pixels for publisher-managed ads) to use for the deal and create a PG default placement, as prompted.

   Creating a PG default placement for the deal is mandatory to deliver 100% of your buy. This type of placement has no targeting so DSP can return a bid to every bid request from the publisher.

1. (Optional) Target the PG deal in additional PG or non-PG placements by clicking ![Options menu](/help/dsp/assets/options-menu.png) **> [!UICONTROL Attach new placement]**.

    A deal can target multiple placements that support any combination of media types (such as connected TV, desktop, and audio).

>[!MORELIKETHIS]
>
>* [About programmatic guaranteed deals](programmatic-guaranteed-about.md)
>* [Tips for negotiating a programmatic guaranteed deal](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Submit an ad for a programmatic guaranteed deal with [!DNL FreeWheel]](freewheel-submit.md)
>* [Accept a deal in the [!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)
>* [Manually create deal ID details](deal-id-create.md)
>* [SSP partners](ssp-partners.md)
>* [Overview of inventory features in Advertising DSP](inventory-overview.md)
