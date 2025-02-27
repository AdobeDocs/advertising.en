---
title: Available macros for tracking URLs
description: Reference the macros that you can add to your landing page URLs, tracking URLs, and third-party creatives.
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
---
# Available macros for tracking URLs

*Closed beta*

<!-- More feature metadata??? -->

You can include any of the following macros in your third-party creatives, in third-party tracking URLs for your experiences, and in landing page URLs for your own use.

Some of the available macros, or their equivalents, are automatically included in experience tags.

<!-- Later: 

| Macro | Description | Automatically in experience tags for Advertising DSP? | Automatically in experience tags for [!DNL Google Campaign Manager 360]? |
| --- | --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Tracks and reports the campaign ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ebuy!` |
| `${TM_SITE_ID_NUM}` | Tracks and reports the site ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%esid!` |
| `${TM_PLACEMENT_ID_NUM}` | Tracks and reports the placement ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%epid!` |
| `${TM_AD_ID_NUM}` | Tracks and reports the ad ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%eaid!` |
| `${TM_CREATIVE_ID_NUM}` | Tracks and reports the creative ID from the DSP | N/A | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ecid!` |
| `${TM_SESSION_ID}` | Tracks and reports the impression ID from the DSP. If a value isn't returned, Advertising Creative generates one. | Yes | &mdash; |
| `${TM_ACC_EXPERIENCE_ID}` | Tracks and reports the Advertising Creative experience ID | &mdash; | &mdash; |
| `${TM_ACC_CREATIVE_ID}` | Tracks and reports the Advertising Creative creative ID | &mdash; | &mdash; |
| `${TM_RANDOM}` | A random number between 1 and 1000000 | &mdash; | &mdash; |
| `${TM_TIMESTAMP}` | The Unix Timestamp (in seconds) | &mdash; | &mdash; |
| `${TM_CLICK_URL_URLENC}` | (For third-party ads from vendors who require URL encoding) The encoded click redirect URL, which enables ad servers to track and count ad clicks. When the ad is served and the user clicks on it, the macro is activated, and the click is recorded and counted for reporting purposes. | Yes | &mdash; |

-->

| Macro | Description | Automatically in experience tags for Advertising DSP? |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Tracks and reports the campaign ID from the DSP | Yes |
| `${TM_SITE_ID_NUM}` | Tracks and reports the site ID from the DSP | Yes |
| `${TM_PLACEMENT_ID_NUM}` | Tracks and reports the placement ID from the DSP | Yes |
| `${TM_AD_ID_NUM}` | Tracks and reports the ad ID from the DSP | Yes |
| `${TM_CREATIVE_ID_NUM}` | Tracks and reports the creative ID from the DSP | N/A |
| `${TM_SESSION_ID}` | Tracks and reports the impression ID from the DSP. If a value isn't returned, Advertising Creative generates one. | Yes |
| `${TM_ACC_EXPERIENCE_ID}` | Tracks and reports the Advertising Creative experience ID | &mdash; |
| `${TM_ACC_CREATIVE_ID}` | Tracks and reports the Advertising Creative creative ID | &mdash; |
| `${TM_RANDOM}` | A random number between 1 and 1000000 | &mdash; |
| `${TM_TIMESTAMP}` | The UNIX® Timestamp (in seconds) | &mdash; |
| `${TM_CLICK_URL_URLENC}` | (For third-party ads from vendors who require URL encoding) The encoded click redirect URL, which enables ad servers to track and count ad clicks. When the user clicks the ad, the macro is activated, and the click is recorded and counted for reporting purposes. | Yes |

>[!MORELIKETHIS]
>
>* [Add standard creatives to a creative library](/help/creative/creative-libraries/creative-add-standard.md#creative-add-third-party)
>* [Standard creative settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party)
>* [Targeted experience settings](/help/creative/experiences/experience-settings-targeting.md)
>*[Nontargeted experience settings](/help/creative/experiences/experience-settings-no-targeting.md)
