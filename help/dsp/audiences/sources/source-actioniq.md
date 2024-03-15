---
title: "Convert User IDs from [!DNL ActionIQ] to Universal IDs"
description: "Learn how to enable DSP to ingest your [!DNL ActionIQ] first-party segments."
feature: DSP Audiences
---
# Convert User IDs from [!DNL ActionIQ] to Universal IDs

Use the DSP integration with the [!DNL ActionIQ] customer data platform to convert your hashed email addresses to universal IDs for targeted advertising.

There are <!-- NN --> steps to share data from [!DNL ActionIQ] with DSP:

1. [Create an audience source in DSP](#source-create). 

1. ?

## Step 1: Create an audience source in DSP {#source-create}

1. [Create an audience source](source-create.md) to import audiences to your DSP account or an advertiser account, specifying the [universal ID formats](source-about.md) to which you want to convert your user identifiers.

1. After you create the audience source, share the source code key with the [!DNL ActionIQ] user.

1. After you complete all steps, verify in <!-- Where? Aren't the imported segments available in Audiences > All Audiences, but you have to create/edit a saved audience to see them? They won't show up in Audiences > Segments (which is just for custom segments and CCPA segments you manually create in our UI) Don't you have to  [!UICONTROL Audiences] --> that the segment is populating within 24 hours. Compare the number of universal IDs with the number of original hashed email addresses.

   The translation rate of hashed email addresses to universal IDs should be greater than 90%. For example, if you send 100 hashed email addresses from your customer data platform, they should be translated to more than 90 universal IDs. A translation rate of 90% or less is an issue.
   
   For troubleshooting support, contact your Adobe Account Team or `adcloud-support@adobe.com`.

## Step 2: 

>[!MORELIKETHIS]
>
>* [About Activating Authenticated Segments from Audience Sources](/help/dsp/audiences/sources/source-about.md)
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [Convert User IDs from [!DNL Adobe Real-Time CDP] to Universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convert User IDs from [!DNL Tealium] to Universal IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
