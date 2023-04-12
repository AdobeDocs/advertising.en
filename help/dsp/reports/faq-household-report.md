---
title: FAQs About the [!UICONTROL Household] Report
description: Learn more about the [!UICONTROL Household] report, including how it's different from other reports and troubleshooting.
---
# FAQs About the [!UICONTROL Household] Report

## How are [!UICONTROL Household] reach and frequency reports different from other custom reports?

The [!UICONTROL Household] report measures reach, impression, and frequency across various dimensions at a household level based on IP address. The other custom reports are generated at the device or cookie level.

For example, even if one impression is served to three devices within one household, the Unique Household Reached metric is one.

### Supported Dimensions

The [!UICONTROL Household] report supports the [following dimensions](/help/dsp/reports/report-columns.md): [!UICONTROL Campaign] **[is this Campaign Name, like other reports?]**<!-- name? -->,[!UICONTROL Package] **[is this Package Name, like other reports?]**<!-- name? There's another dimension called Package Name -->, [!UICONTROL Placement] **[is this Placement Name, like other reports?]**<!-- name? There's another dimension called Placement Name -->, [!UICONTROL Site/Apps] (which doesn't provide access to overlap metrics), [!UICONTROL Media Type], [!UICONTROL Feed Type], [!UICONTROL Device], [!UICONTROL Publisher], [!UICONTROL Audience], [!UICONTROL Creative Length], and user-created [!UICONTROL Tags] **[is this Placement Tags, like other reports?]**.|

### Supported Metrics

The [available metrics](/help/dsp/reports/report-columns.md) include:

* Overlap metrics: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)], and [!UICONTROL Unique Household (Overlap)].

  Overlap metrics are the values that occur only for the reported dimension or combination of dimensions, and not for other dimensions. <!-- For example, it might show the ?? -->

* Non-overlap metrics: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions], and [!UICONTROL Unique Household Reached]

Conversion metrics and custom goals aren't supported.

## What's the difference between the overlap and non-overlap metrics?

 **[I need to clean up this and add the image]**
<!-- finish this, including image -->

Consider three metrics: Unique Household, Incremental Household, and Incremental Household (Overlap). 

Let us consider three campaigns -- A, B, C. 

Unique Household Reached (Total) provides the Unique Household reached by each of the campaigns or the total area of each of the circles. 
For example: Unique Household Reached by A = Incremental Household Reached by A + (A+C) + (A+B) +(A+B+C)

Incremental Household Reached is the Unique Household that's been reached only by a campaign. Eg: Incremental Household Reached by A, B, C are the Incremental Household reached by A, B, C respectively. 

Incremental Household (Overlap) is the Unique Household reached by the campaign or combination of campaigns. Eg: Incremental Household reached by A, C is A+C. 

## Workflow

Follow the normal steps to [create a custom report](report-create.md).

The [!UICONTROL Household] report can include only one dimension. It also can include either a) overlap metrics by any dimension except for Site/Apps or b) non-overlap metrics, but not both.

## What are some limitations of the [!UICONTROL Household] report? 

Reports with overlap metrics can include combinations of up to three values **[What are you combining here? And why "up to three" but "maximum of ten?"]**<!-- not sure what this means. Can't you include only one dimension? So what does "combination" mean? -->, with a maximum of ten total values, per dimension. For example, if you use the Placement Name dimension, then the overlap report can be generated for up to ten placements. If your dimension includes more than ten values, then a blank report is generated. 

This restriction will be removed in a future release.

In the meantime, create a separate report for each unique dimension or for overlap reports. 

## Why is my report blank? 

Reports with overlap metrics may be blank when the dimension has more than ten distinct values. For example, if you use the [!UICONTROL Placement Name] dimension, and more than ten placements are selected for the report, then the report isn't populated. **[OR are the metric values not populated?]**<!-- or are the metric values not populated? -->

## Why are the frequency and unique reach values different between my [!UICONTROL Custom] reports and the [!UICONTROL Household] report?

These metrics in [!UICONTROL Household] reports are calculated using the actual count of IP addresses, whereas the metrics in the [!UICONTROL Custom] report use estimated numbers calculated using models. However, the discrepancy should be less than 10%.

## How do I configure the report for the [!UICONTROL Placement Tags] dimension?

To create tags for the placement, [open the placement settings](/help/dsp/campaign-management/placements/placement-edit.md) and enter values in the [Placement Tags field](/help/dsp/campaign-management/placements/placement-settings.md).
 
When a placement includes multiple tags, the report considers the entire string as one tag. The report includes one row for each unique string.

## [!UICONTROL Household] Report vs. Data from [!DNL Advanced Measurement Services]

For advanced reporting on household-based reach and frequency, the [[!DNL Strategic Advertising Consulting] team](/help/dsp/introduction/advanced-measurement-services.md) can provide highly customizable reports along with holistic strategic recommendations. For more information about [!DNL Advanced Measurement Services], contact your Adobe Account Team.

### If I'm already using [!DNL Advanced Measurement Services], why should I use the [!UICONTROL Household] report?

The [!UICONTROL Household] report empowers clients to pull household-level reach and frequency metrics autonomously in real time.

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
