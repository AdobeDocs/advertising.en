---
title: Create and Implement a Custom Segment
description: Learn how to create and implement a custom segment to track users exposed to ads or users who visit your webpages.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
---
# Create and Implement a Custom Segment

You can collect your own first-party audience data by creating and implementing a custom DSP segment. You can use the segment to track a) users exposed to ads from desktop and mobile devices and b) users who visit specific webpages. You can later retarget users in the segment with additional ads or prevent users in the segment from receiving additional ads.

>[!NOTE]
>
>To track users IDs from consumer opt-out-of-sale requests on your website, per the California Consumer Privacy Act (CCPA), create a [CCPA opt-out-of-sale segment](ccpa-opt-out-segment-create.md).

## Prerequisites for Segments to Track ID5 IDs

*Beta feature* 

* Before you generate a segment to track users associated with ID5 IDs, sign an agreement with [!DNL ID5] and get your organization's partner ID. Contact your Adobe Account Team for instructions.

* For measurement in Adobe Analytics, you must:

  1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md), and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.

  1. Add the following parameter to your webpages before or within the the [JavaScript code required for [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) &mdash; anywhere before the last event service is initialized.

     ```window.id5PartnerId=Your_ID5_PartnerID;```
     
     Example:

     ```
     <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
     <script>
       window.id5PartnerId=Your_ID5_PartnerID;
            if("undefined" != typeof AdCloudEvent)
                AdCloudEvent('IMS ORG Id','rsid');
     </script>
     ```

   1. Use any browser debugging tool to verify that each call is initiated to the domain `lasteventf-tm.everesttech.net` and contains the parameter `_les_id5` with an encrypted ID5 ID as its value.

## Create and Implement a Custom Segment

1. Create the segment:

    1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

    1. Above the data table, click **[!UICONTROL Create]**.

    1. Enter a unique **[!UICONTROL Segment Name]**.

    1. For the **[!UICONTROL Segment Type]**, select *[!UICONTROL Custom]*.

    1. Enter the **[!UICONTROL Lookback Window]**, which is the number of days a user's cookie stays in the segment.

       The default window is 45 days. Enter a value from one (1) to 365.

    1. Click **[!UICONTROL Advanced]** to expand the advanced settings, and then select the types of user identifiers that the segment tag tracks:

       * *[!UICONTROL Cookies]:* (The default) The segment tag tracks cookies.

       * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* The segment tag tracks [!DNL ID5] IDs. No fees are incurred for impressions delivered to universal IDs.

         **[!UICONTROL Terms of Service]:** The terms of service agreement for using universal IDs. You or another user in the DSP account must accept the terms once before you can use universal IDs for a new ID type. For customers with managed service contracts, your Adobe Account Team will get your consent and accept the terms on your organization's behalf. To read the terms, click **>**. To accept the terms, scroll to the bottom of the terms and click **[!UICONTROL Accept]**.
    
    1. Click **[!UICONTROL Save]**.

1. Copy and implement tags to track the segment, as needed:

    1. Return to **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

    1. Hold the cursor over the segment row and click **[!UICONTROL Get Pixel]**.

        * To track desktop and mobile visitors to a webpage:

            1. Copy the page view tracking tag, which is labeled "[!UICONTROL Desktop or mobile websites]."

            1. (Tags for segments that track [!DNL ID5] IDs) In the copied tag, replace `ID5_PARTNER_ID` with the partner ID that [!DNL ID5] assigned to your organization.
            
               For example, if your ID5 partner ID is `abcde` and the generated segment tag is
               
               ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```
               
               then replace `ID5_PARTNER_ID` with `abcde` within the tag to get the following:
               
               ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```
               
               Your organization received the partner ID when it signed an agreement with [!DNL ID5]. If you don't know your partner ID, contact your Adobe Account Team.
               
               This step isn't necessary for tags to track [!DNL ID5] IDs for users exposed to an ad unit on desktop or mobile devices.

            1. Provide the tag to the advertiser or website contact for deployment.

               The advertiser's IT department or other group may need to schedule, or be informed about, the tag deployment.

        * To track users exposed to an ad unit on desktop or mobile devices:

            1. Copy the impression tracking tag, which is labeled "[!UICONTROL Desktop or mobile ads]."
            
            1. Add the tag to either the [!UICONTROL Pixel] tab for each relevant ad or to the [!UICONTROL Event Pixels] section of the [[!UICONTROL Tracking] settings for each relevant placement](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Once a tracking tag is implemented, you can use the segment in the audience targets or exclusions for any placement.

>[!TIP]
>
>Keep track of the segment size as users are tracked.

>[!MORELIKETHIS]
>
>* [About Audience Management](audience-about.md)
>* [Edit Segment Information](segment-edit.md)
>* [Delete a Segment](segment-delete.md)
>* [View Tracking Pixels for a Segment](segment-view-pixels.md)
>* [Share or Stop Sharing a Segment](segment-share.md)
>* [Create and Implement a [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Create a Reusable Audience](reusable-audience-create.md)
>* [Available Third-party Data Providers](third-party-data-providers.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
