---
title: FAQs About the [!UICONTROL Household] Report
description: Learn more about the [!UICONTROL Household] report, including XXXXXXXXXX.
---
# FAQs About the [!UICONTROL Household] Report

## How are [!UICONTROL Household] reach and frequency reports and different from other custom reports?

The [!UICONTROL Household] report measures reach, impression, and frequency across various dimensions at a household level based on IP address. The other custom reports are generated at the device or cookie level.

For example, if one impression is served to three devices in the household, then the [!UICONTROL Household] report shows three (3) impressions and a frequency of three (3), but the Unique Household Reached metric is one (1).

The [!UICONTROL Household] report supports the following dimensions: 
[!UICONTROL Campaign]<!-- name? -->,[!UICONTROL Package]<!-- name? There's another dimension called Package Name -->, [!UICONTROL Placement]<!-- name? There's another dimension called Placement Name -->, [!UICONTROL Site/Apps], [!UICONTROL Media Type], [!UICONTROL Feed Type], [!UICONTROL Device], [!UICONTROL Publisher], [!UICONTROL Audience], [!UICONTROL Creative Length], and user-created [!UICONTROL Placement Tags].|

The available metrics include:

* Overlap metrics: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)], and [!UICONTROL Unique Household (Overlap)].

* Non-overlap metrics: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions], and [!UICONTROL Unique Household Reached]

## What's the difference between the overlap and non-overlap metrics?

<!-- finish this, including image -->

Consider three metrics: Unique Household, Incremental Household, and Incremental Household (Overlap). 

Let us consider three campaigns -- A, B, C. 

Unique Household Reached (Total) provides the Unique Household reached by each of the campaigns or the total area of each of the circles. 
Eg: Unique Household Reached by A = Incremental Household Reached by A + (A+C) + (A+B) +(A+B+C)

Incremental Household Reached is the Unique Household that have been reached only by a campaign. Eg: Incremental Household Reached by A, B, C are the Incremental Household reached by A, B, C respectively. 

Incremental Household (Overlap) is the Unique Household reached by the campaign or combination of campaigns. Eg: Incremental Household reached by A, C is A+C. 

## Workflow

Follow the normal steps to [create a custom report](report-create.md).

The [!UICONTROL Household] report can include only one dimension. They also can include either overlap metrics or non-overlap metrics, but not both.

## What are some limitations of the [!UICONTROL Household] report? 

Reports with overlap metrics can include combinations of up to three values<!-- not sure what this means. Can't you include only one dimension? So what does "combination" mean? -->, with a maximum of 10 total values, per dimension. For example, if you use the Placement Name dimension, the overlap report can be generated for up to 10 placements. If your dimension includes more than 10 values, a blank report is generated. 

This restriction will be removed in a future release.

In the meantime, create a separate report for each unique dimension or for overlap reports. 

## Why am I receiving a blank report? 

Reports with overlap metrics may be blank when the dimension has more than 10 distinct values. For example, if you use the [!UICONTROL Placement Name] dimension, and more than 10 placements are selected for the report, then the report isn't populated. 

## Why are the frequency and unique reach values different between my [!UICONTROL Custom] reports and the [!UICONTROL Household] report?

These metrics in [!UICONTROL Household] reports are calculated using the actual count of IP addresses, whereas the metrics in the [!UICONTROL Custom] report use estimated numbers calculated using models. However, the discrepancy should be less than 5%. 

## How do I configure the report for the [!UICONTROL Placement Tags] dimension?

[Open the placement settings](/help/dsp/campaign-management/placements/placement-edit.md) and use the [Placement Tags field](/help/dsp/campaign-management/placements/placement-settings.md) to create tags for the placement.
 
When a placement includes multiple tags, the report considers the entire string as one tag.

## [!UICONTROL Household] Report vs. Data from [!DNL Advanced Measurement Services]

For advanced reporting on household-based reach and frequency, the [[!DNL Strategic Advertising Consulting] team](/help/dsp/introduction/advanced-measurement-services.md) can provide highly-customizable reports along with holistic strategic recommendations. For more information about [!DNL Advanced Measurement Services], contact your Adobe Account Team.

### If I'm already using [!DNL Advanced Measurement Services], why should I use the [!UICONTROL Household] report?

The [!UICONTROL Household] report empowers clients to pull household-level reach and frequency metrics autonomously and in real-time.

### Does the [!UICONTROL Household] report replace [!DNL Advanced Measurement Services]?

No, [!DNL Advanced Measurement Services] reports and consulting services continue to be essential for brands seeking more expansive, customizable reporting as well as strategic insights and recommendations.

### Can I use both the [!UICONTROL Household] report and [!DNL Advanced Measurement Services]? 

The ideal use case is to use both the [!UICONTROL Household] report and the [!DNL Advanced Measurement Services] reporting and consulting services together. Consider the [!UICONTROL Household] report as transactional, meant to inform day-to-day optimizations, and [!DNL Advanced Measurement Services] as more strategic, meant to inform holistic learnings and takeaways tied to overarching business objectives.

>[!MORELIKETHIS]
>
>* [About Custom Reports](/help/dsp/reports/report-about.md)
>* [Create a Custom Report](/help/dsp/reports/report-create.md)
>* [Edit a Custom Report](/help/dsp/reports/report-edit.md)
>* [Custom Report Settings](/help/dsp/reports/report-settings.md)
>* [Available Report Columns](/help/dsp/reports/report-columns.md)
