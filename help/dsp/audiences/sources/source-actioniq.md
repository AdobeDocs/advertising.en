---
title: "Convert User IDs from [!DNL ActionIQ] to universal IDs"
description: "Learn how to enable DSP to ingest your [!DNL ActionIQ] first-party segments."
feature: DSP Audiences
---
# Convert user IDs from [!DNL ActionIQ] to universal IDs

*Beta feature*

Use the DSP integration with the [!DNL ActionIQ] customer data platform to convert your hashed email addresses to universal IDs for targeted advertising.

There are <!-- NN --> steps to share data from [!DNL ActionIQ] with DSP:

1. [Create an audience source in DSP](#source-create). 

1. ?

## Step 1: Create an audience source in DSP {#source-create}

1. [Create an audience source](source-manage.md) to import audiences to your DSP account or an advertiser account, specifying the [universal ID formats](source-about.md) to which you want to convert your user identifiers.

1. After you create the audience source, share the source code key with the [!DNL ActionIQ] user.

## Step 2: 

## Step 3:

1. Verify in your audience library (which is available when you create or edit an audience from [!UICONTROL Audiences] > [!UICONTROL All Audiences] or within placement settings) that the segment is populating, and compare the number of universal IDs with the number of original hashed email addresses.
   
   The segments should be available in DSP within 24 hours. After DSP receives the segment data, the audience count should be visible within nine (9) hours. For information about acceptable ID translation rates and why the segment counts can vary, see "[Data variances between email IDs and universal IDs](#universal-ids-data-variances)."

Segments are refreshed every 24 hours.

## Troubleshooting

To troubleshoot translation rate and user count issues, see "[Support for activating universal IDs](/help/dsp/audiences/universal-ids.md)."

To troubleshooting issues with the conversion procedure, contact your Adobe Account Team or `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [About first-party audience sources](/help/dsp/audiences/sources/source-about.md)
>* [Manage audience sources to activate universal ID audiences](source-manage.md)
>* [Convert user IDs from [!DNL Adobe Real-Time CDP] to universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convert user IDs from [!DNL Tealium] to universal IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [About audience management](/help/dsp/audiences/audience-about.md)
