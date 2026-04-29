---
title: Overview of setting up PG deals in [!DNL FreeWheel]
description: Learn about the prerequisites and extra steps necessary to run ads for programmatic guaranteed deals with publishers on [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: b9c60248-8104-42ef-8afb-2f9db67b33b0
TQID: https://experienceleague.adobe.com/8ovkE7w5qXW7Csibxy-PyHvUud0wwrhdSTulQP7bIeM
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
# Overview of setting up programmatic guaranteed deals in [!DNL FreeWheel] 

Setting up programmatic guaranteed deals with publishers on [!DNL FreeWheel] requires extra permissions and steps.

>[!PREREQUISITES]
>
>Work with your Adobe Account Team to ensure that your [!DNL DSP] account has the following permissions:
>
>* Permission to use the [!DNL FreeWheel] programmatic guaranteed workflow, which is required to submit an ad for a programmatic guaranteed deal to [!DNL FreeWheel].
>
>* (If you work with UK publishers who require a [!DNL Clearcast] clock number with each ad) Permission to include clock numbers in your ads.

## Workflow

1. Create an ad with the media type specified in the deal.

   For some UK publishers, you must include a [!DNL Clearcast] clock number with your ad.

1. [Accept the deal ID](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) that you've already negotiated with a publisher on [!DNL FreeWheel] using the Deal ID Inbox.

   After you accept the deal, follow the prompts to 1) select the ad to use for the deal and 2) create a programmatic guaranteed default placement to serve the ad.

1. [Submit the ad to [!DNL FreeWheel]](freewheel-submit.md)

    The ad must be submitted and approved before it runs.

1. [Check the ad submission status](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Accept a deal in the [!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)
>* [Submit an ad for a programmatic guaranteed deal to [!DNL FreeWheel]](freewheel-submit.md)
>* [Check the status of ads for a [!DNL FreeWheel] PG deal](freewheel-check-status.md)
>* [Error codes for [!DNL FreeWheel] ad submissions](freewheel-error-codes.md)
