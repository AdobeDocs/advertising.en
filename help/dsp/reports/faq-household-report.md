---
title: FAQs About Household Reports
description: Learn more about household reach, frequency, and conversion data, including how the household reports are different from other reports and troubleshooting.
exl-id: aaaf6f6d-b133-4cda-8fc6-bd686b3b1ebb
---
# FAQs About Household Reports

## The [!UICONTROL Household Reach & Frequency] Report

### How are [!UICONTROL Household Reach & Frequency] reports different from other custom reports?

The [!UICONTROL Household Reach & Frequency] report measures reach, impression, and frequency across various dimensions at a household level based on IP address. The other custom reports are generated at the device or cookie level.

For example, even if one impression is served to three devices within one household, the Unique Household Reached metric is one.

#### Supported Dimensions

The [!UICONTROL Household Reach & Frequency] report supports the [following dimensions](/help/dsp/reports/report-columns.md): "[!UICONTROL Campaign]," "[!UICONTROL Package]," "[!UICONTROL Placement]," "[!UICONTROL Site/Apps]" (which doesn't provide access to overlap metrics), "[!UICONTROL Media Type]," "[!UICONTROL Feed Type]," "[!UICONTROL Device]," "[!UICONTROL Publisher]," "[!UICONTROL Audience]," "[!UICONTROL Creative Length]," and user-created placement "[!UICONTROL Tags]." |

#### Supported Metrics

The [available metrics](/help/dsp/reports/report-columns.md) include:

* Overlap metrics: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)], and [!UICONTROL Unique Household (Overlap)].

  Overlap metrics are the values that occur only for the reported dimension or combination of dimensions, and not for other dimensions. <!-- For example, it might show the ?? -->

* Non-overlap metrics: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions], and [!UICONTROL Unique Household Reached]

Conversion metrics and custom goals aren't supported.

### What's the difference between the overlap and non-overlap metrics?

The following figure shows three metrics (Unique Household Reached, Incremental Household Reached, and Incremental Household (Overlap)) for three campaigns (A, B, and C).

![Illustration of household overlap metrics](/help/dsp/assets/household-overlap-metrics-illustration.png "Illustration of household overlap metrics")

* Unique Household Reached (Total) provides the Unique Household reached by each of the campaigns or the total area of each of the circles. In the figure, Unique Household Reached by A = Incremental Household Reached by A + (A+B) + (A+C) +(A+B+C)

* Incremental Household Reached is the Unique Household that's been reached only by a campaign. In the figure, Incremental Household Reached by A, B, C are the Incremental Household Reached by A, B, C respectively.

* Incremental Household (Overlap) is the Unique Household reached by the campaign or combination of campaigns. In the figure, the Incremental Household Reached by A, C is A+C.

### Workflow

Follow the normal steps to [create a custom report](report-create.md).

The [!UICONTROL Household Reach & Frequency] report can include only one dimension. It also can include either a) overlap metrics by any dimension except for Site/Apps or b) non-overlap metrics, but not both.

### What are some limitations of the [!UICONTROL Household Reach & Frequency] report?

Reports with overlap metrics output intersections of up to three values. For example, if you use the metric [!UICONTROL Unique Household (Overlap)] for 10 placements, then you can see the unique households reached by individual placements, common households reached by a combination of any two placements, and common households reached by combinations of any three placements. You can't see common households reached by four or more placements.

For dimensions other than campaign, package, or placement, the report supports up to 10 values in each dimension. For example, to generate a [!UICONTROL Unique Household Reached] report for the [!UICONTROL Audience] dimension, the number of unique audiences should be less than or equal to 10. If you include more then 10 unique audiences, then a blank report is generated. 

### Why are the frequency and unique reach values different between my [!UICONTROL Custom] reports and the [!UICONTROL Household Reach & Frequency] report?

These metrics in [!UICONTROL Household] reports are calculated using the actual count of IP addresses, whereas the metrics in the [!UICONTROL Custom] report use estimated numbers calculated using models. However, the discrepancy should be less than 10%.

### How do I configure the report for the [!UICONTROL Placement Tags] dimension?

To create tags for the placement, [open the placement settings](/help/dsp/campaign-management/placements/placement-edit.md) and enter values in the [Placement Tags field](/help/dsp/campaign-management/placements/placement-settings.md).

When a placement includes multiple tags, the report considers the entire string as one tag. The report includes one row for each unique string.

## The [!UICONTROL Household Conversions] Report

### What are the types of attribution methods supported in [!UICONTROL Household Conversions] report?

Two types of attribution methods are supported:

* Unique: Counts the number of times a dimension value (such as a device or placement) was on the path to conversion. 

* MTA (Multi-Touch Attribution):  Distributes the credit of each conversion based on the frequency of occurrence of the dimension value (such as a device or placement) on the path to conversion. For example, if there were total of 10 impressions before conversion, with 8 on CTV and 2 on Mobile, then 80% of the credit (0.8) is given to CTV screens and 0.2 to Mobile.

### How does household conversion reporting differ from CTV view-through reporting in Adobe Analytics?

CTV view-through data in [!DNL Analytics] is powered [!DNL Analytics] tracking, and the household conversion data uses data collected using Adobe Advertising conversion tracking. In addition, the DSP attribution logic in [!DNL Analytics] uses only the last event but household conversion reporting supports two different attribution methods: Unique and MTA.

### Can I view CTV view-through data in both [!DNL Analytics for Advertising] and in custom reports?

Advertisers without [!DNL Analytics for Advertising] can use only the Household Conversion Report for household conversion reporting.

If your organization has [!DNL Analytics for Advertising], use both types of reporting together. While CTV view-through reporting is suitable for broad channel analysis, site behavior, and so on, custom reports provide a granular view (with data broken down by media type, publishers, and so on) to indicate the factors driving conversion rates.

## [!UICONTROL Household Reach & Frequency] and [!UICONTROL Household Conversions] Reports vs. Data from [!DNL Advanced Measurement Services]

For advanced reporting on household-based reach and frequency or conversions, the [[!DNL Strategic Advertising Consulting] team](/help/dsp/introduction/advanced-measurement-services.md) can provide highly customizable reports along with holistic strategic recommendations. For more information about [!DNL Advanced Measurement Services], contact your Adobe Account Team.

### If I'm already using [!DNL Advanced Measurement Services], why should I use the [!UICONTROL Household Reach & Frequency] and [!UICONTROL Household Conversions] reports?

The [!UICONTROL Household Reach & Frequency] and [!UICONTROL Household Conversions] reports empowers clients to pull household-level reach, frequency, and conversion metrics respectively autonomously in real time.

### Can I use both the [!UICONTROL Household Reach & Frequency] and [!UICONTROL Household Conversions] reports and [!DNL Advanced Measurement Services]?

The ideal use case is to use both the [!UICONTROL Household] report and the [!DNL Advanced Measurement Services] reporting and consulting services together. Consider the [!UICONTROL Household] report as transactional, meant to inform day-to-day optimizations, and [!DNL Advanced Measurement Services] as more strategic, meant to inform holistic learnings and takeaways tied to overarching business objectives.

>[!MORELIKETHIS]
>
>* [About Custom Reports](/help/dsp/reports/report-about.md)
>* [Create a Custom Report](/help/dsp/reports/report-create.md)
>* [Edit a Custom Report](/help/dsp/reports/report-edit.md)
>* [Custom Report Settings](/help/dsp/reports/report-settings.md)
>* [Available Report Columns](/help/dsp/reports/report-columns.md)
