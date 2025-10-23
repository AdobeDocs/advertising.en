---
title: Manage retargeting pixels
description: Learn how to create and implement retargeting pixels to use as targets for ad experiences.
feature: Creative Pixels
exl-id: dcd13c5a-315d-4380-99f9-6dbab3e1e1be
---
# Manage retargeting pixels

<!-- Note to self: These aren't segments -- we don't create a pool of users. -->

You can create a retargeting pixel to identify visitors to an advertiser's landing pages or conversion pages using user cookies or universal IDs. The pixel tracks the most recent event that the visitor performs on a page and captures specific attributes that the page is tracking for those visitors. Once you create the pixel, generate a pixel tag to insert in the relevant webpages to begin tracking visitors.<!-- Note to self: surfer id=cookie or universal ID -->

You can then use the pixel as the target for any creative within an ad experience to show ads only to users with specified attributes who previously visited the webpages associated with the pixel. For example, you could target visitors who look at red shoes in size 10, if the webpages track those attribute values.<!-- better example? Make sure they match attribute examples below --> The experience-level targets are applied in conjunction with your DSP's targeting options; hierarchical targeting behavior may vary by DSP.

Retargeting profiles are stored for 180 days.

Example pixel:

```
<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--Insert ID5_PARTNER_ID--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--"></script>
```

>[!NOTE]
>
> * [!DNL Creative] supports universal IDs only for Advertising DSP.
>* You can also use your first-party audiences from Adobe Audience Manager and Adobe Analytics as [creative targets for your experiences](/help/creative/experiences/experience-settings-targeting.md).
>* When you use an experience as an ad within an Advertising DSP placement, you can target the placement to all audiences available to you in DSP. You can also [create custom audience segment tags](/help/dsp/audiences/custom-segment-create.md) to track all visitors to specific landing pages and then use those segments as creative targets for a placement. Advertising DSP applies ad-level targeting on top of (not instead of) placement-level targeting.
>* Website visitors who have opted out of tracking for ad targeting do not receive ads with personalized creative content based on audience segment or re-targeting profile.

## Create a retargeting pixel

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Above the data table, click **[!UICONTROL Creative]**, and then select > **[!UICONTROL Retargeting Pixel]**.

1. Specify the [retargeting pixel settings](#retargeting-pixel-settings).

1. Click **[!UICONTROL Save]**.

1. [Generate the pixel tag](#retargeting-pixel-generate) to provide to the advertiser or website contact.

   The retargeting pixel tag must be the last action on the page.<!-- verify here and below -->

   The advertiser's IT department or other group may need to schedule, or be informed about, the tag deployment.

## Edit a retargeting pixel

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Hold the cursor over the pixel name and click **[!UICONTROL Edit]**.

1. Edit the [retargeting pixel settings](#retargeting-pixel-settings).

1. Click **[!UICONTROL Save]**.

1. [Generate the pixel tag](#retargeting-pixel-generate) to provide to the advertiser or website contact so that they can replace the original tag.

   The retargeting pixel tag must be the last action on the landing page.

   The advertiser's IT department or other group may need to schedule, or be informed about, the tag deployment.

## Generate a tag for a retargeting pixel {#retargeting-pixel-generate}

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Hold the cursor over the pixel name and click **[!UICONTROL Generate Tag]**.

1. Click **[!UICONTROL Copy to Clipboard]** to copy the tag to your computer's clipboard, from which you can paste the text into a file to save.

1. In the pixel tag, specify a value for each attribute in both the `<img src>` and the `<script src>` sections by replacing each "`Insert <attribute>`" with a value. Specify an ID5 partner ID if the tag captures a universal ID.

   If you add additional attributes manually, include URL encoding. 

   For example, if you included the attributes "category," "color," and "size" and capture ID5 universal IDs, then the pixel tag includes the following parameters: `&ut1=--Insert category--&ut2=--Insert color--&ut3=--Insert size--` and `&id5pid=--Insert ID5_PARTNER_ID--`. To target users who select red sandals in size 10, change the parameters in both the image tag and script tag to `&ut1=sandals&ut2=red&ut3=10`, and also enter your ID5 partner ID in the script tag, such as `&id5pid=0123456789`.

   `<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--0123456789--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--"></script>`

1. Provide the completed pixel tag to the advertiser or website contact, together with a list of the relevant landing pages in which to insert it.

   The retargeting pixel tag must be the last action on the landing page.
   
   The advertiser's IT department or other group may need to schedule, or be informed about, the tag deployment.

## Delete a retargeting pixel

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Hold the cursor over the pixel name and click **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Delete]**.

## Retargeting pixel settings {#retargeting-pixel-settings}

**[!UICONTROL Pixel Name]:** The name of the pixel. **Note:** The pixel tag includes the pixel ID (`pxId=<ID>`), not the pixel name.

**[!UICONTROL Advertiser]:** (Read-only for existing pixels) The advertiser for which the pixel is tracked.

**[!UICONTROL Attribute 1]:** An attribute to include in the pixel tag, such as "SKU," "category," "size," or other attributes of the page or the product displayed on the page. Specify a value for the attribute in the pixel tag before you insert it in the relevant webpages.

When you target ad experiences to users exposed to the pixel, the targeting settings specify the attribute values that must be present to display the creatives.

**[!UICONTROL Attribute 2]**, **[!UICONTROL Attribute 3]**, **[!UICONTROL Attribute 4]**, **[!UICONTROL Attribute 5]:** (Optional) Additional attributes to include in the pixel tag. Specify a value for each additional attribute in the pixel tag before you insert it in the relevant webpages.

When you target ad experiences to users exposed to the pixel, the targeting settings specify the attribute values that must be present to display the creatives.

**[!UICONTROL Advanced]** > **[!UICONTROL Universal IDs]:** (New pixels only; optional) Types of universal IDs for the pixel tag to track:

* *[!UICONTROL ID5]:* The pixel tag tracks [!DNL ID5] IDs. No fees are incurred for impressions delivered to universal IDs.

* *[!UICONTROL Ramp ID]:* The pixel tag tracks [!DNL Ramp IDs]. No fees are incurred for impressions delivered to universal IDs.

To use this feature, you or another user in the DSP account must accept the terms of service agreement for using universal IDs once before you can use universal IDs for a new ID type. For customers with managed service contracts, your Adobe Account Team will get your consent and accept the terms on your organization's behalf. To read the terms, click **[!UICONTROL Terms of Service]**. To accept the terms, scroll to the bottom of the terms and click **[!UICONTROL Accept]**.

>[!MORELIKETHIS]
>
>* [Targeted ad experience settings](/help/creative/experiences/experience-settings-targeting.md)
>* [About ad experiences](/help/creative/experiences/experience-about.md)
