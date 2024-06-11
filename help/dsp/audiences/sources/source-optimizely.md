---
title: Convert User IDs from [!DNL Optimizely] to Universal IDs
description: Learn how to enable DSP to ingest your [!DNL Optimizely] first-party segments.
feature: DSP Audiences
---
# Convert User IDs from [!DNL Optimizely] to Universal IDs

*Beta feature*

Use the DSP integration with the [!DNL Optimizely] customer data platform to convert your organization's first-party hashed email addresses to universal IDs for targeted advertising.

1. (To convert email addresses to [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Set up tracking to enable [!DNL Analytics] measurement](#analytics-tracking).

1. [Create an audience source in DSP](#source-create).

1. [Prepare and push the segment data](#push-data).

1. [Compare the number of universal IDs with the number of hashed email addresses](#compare-id-count).

## Step 1: Set up tracking for [!DNL Analytics] measurement {#analytics-tracking}

*Advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

To convert email addresses to [!DNL RampIDs] or [!DNL ID5] IDs, you must do the following:

1. (If you haven't already done so) Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
1. Register with the universal ID partner and deploy universal ID-specific code on your webpages to match conversions from the IDs on desktop and mobile web browsers (but not mobile apps) to view-throughs:
   
   * **For [!DNL RampIDs]:** You must deploy an additional JavaScript tag on your webpages to match conversions from the IDs on desktop and mobile web browsers (but not mobile apps) to view-throughs. Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag from [!DNL LiveRamp] Authentication Traffic Solutions. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

## Step 2: Create an audience source in DSP {#source-create}

1. [Create an audience source](source-manage.md) to import audiences to your DSP account or an advertiser account. You can choose to convert your user identifiers to any of the [available universal ID formats](source-about.md).

   The source settings will include an auto-generated source key, which you'll use to push the segment data.

1. After you create the audience source, share the source code key with the [!DNL Optimizely] user.

## Step 3: Prepare and push the segment data {#push-data}

The advertiser must prepare and push the data with the help of their [!DNL Optimizely] representative.

1. Within [!DNL Optimizely Data Platform], hash the email IDs for the advertiser's audience using the SHA-256 algorithm.

1. Contact the advertiser's [!DNL Optimizely] representative for instructions to push the segment to DSP. Include the following information when you push the segment:

   * **Source Key:** This is the source key created in [Step 2](#source-create).
   
   * **Account Code:** This is the alphanumeric DSP Account Code, which you can find within DSP at [!UICONTROL Settings] > [!UICONTROL Account].

The segments should be available in DSP within 24 hours and 
are refreshed as configured for the advertiser. Regardless of how frequently the segment is refreshed, inclusion in a segment expires after 30 days to ensure privacy compliance, so refresh the audiences by re-pushing them from [!DNL Optimizely] every 30 days or less.

<!--
Are they using the Data Platform web services, another type of API, or a UI? Add a link to instructions, including how to designate DSP as the destination. And where will they input the DSP-specific fields?]
-->

## Step 4: Compare the number of universal IDs with the number of hashed email addresses {#compare-id-count}

After you complete all steps, verify in your audience library (which is available when you create or edit an audience from [!UICONTROL Audiences] > [!UICONTROL All Audiences] or within placement settings) that the segment is available and is populating within 24 hours. Compare the number of universal IDs with the number of original hashed email addresses.

The translation rate of hashed email addresses to universal IDs should be greater than 90%. For example, if you send 100 hashed email addresses from your customer data platform, they should be translated to more than 90 universal IDs. A translation rate of 90% or less is an issue. For more information about how the segment counts can vary, see "[Causes for Data Variances Between Email IDs and Universal IDs](#universal-ids-data-variances)."
   
For troubleshooting support, contact your Adobe Account Team or `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [About First-Party Audience Sources](/help/dsp/audiences/sources/source-about.md)
>* [Manage Audience Sources to Activate Universal ID Audiences](source-manage.md)
>* [Support for Activating Universal IDs](/help/dsp/audiences/universal-ids.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
