---
title: XXX
description: Learn XXX
feature: Integration with Adobe Analytics
---
# Collect Historical Data for AMO IDs and EF IDs for Use in Adobe Customer Journey Analytics

*Advertisers with [!DNL Analytics for Advertising] and Adobe Customer Journey Analytics Only*

If you use reserved variables to capture the [AMO ID and EF ID](ids.md) for your [!DNL Analytics for Advertising] integration, then you can prepare for a future integration between Adobe Advertising and [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview), which is Adobe’s next-generation [!DNL analytics] solution, by copying your reserved variables for the AMO ID and the EF ID into [standard [!DNL eVars]](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/evar) as soon as possible. This will allow the collection of historical data for the AMO IDs and EF IDs as soon as you complete the task.

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## Why Do I Need to Collect Historical Data for Customer Journey Analytics?

Customer Journey Analytics lets you sync data from Adobe Experience Platform into Adobe Analytics Analysis Workspace. Currently, the [!DNL Analytics Data Connector] to Experience Platform doesn't send data for reserved variables from [!DNL Analytics] to Experience Platform. As a result, data for AMO IDs and EF IDs that are captured by reserved variables isn't currently available within Customer Journey Analytics. <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertising is planning a future implementation with Customer Journey Analytics. Once the implementation is released, your [!DNL Analytics for Advertising] integration will still require you to collect view-through data using [!DNL Analytics] tracking, but you'll be able to view your data in both 1\) [!DNL Analytics] <!-- (Analysis Workspace using data from [!DNL Analytics]) --> and 2\) Customer Journey Analytics <!-- (Analysis Workspace using data from Experience Platform)--> if your organization has both products. When the feature is released, Experience Platform will begin to collect data for your AMO ID and EF ID for use in Customer Journey Analytics, but no historical data prior to the release date will exist.

However, you can begin to collect data for your AMO IDs and EF IDs <!-- [!DNL rVars] --> sooner by creating a simple [[!DNL Analytics] processing rule](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules) to copy your AMO IDs and EF IDs <!-- [!DNL rVars] --> into [!DNL eVars] now. Once you create the processing rule, you'll begin to accrue data for your AMO IDs and EF IDs <!-- [!DNL rVars] --> as soon as they track new events. The historical data will then be available within Customer Journey Analytics once the implementation is available.

>[!NOTE]
>
>Processing rules are applied only to new data that's received. They don't work retroactively to collect past data.

## Copy Your Reserved Variables for AMO IDs and EF IDs into [!DNL eVars]

This step is manual and must be completed for each report suite that tracks AMO IDs and EF IDs <!-- [!DNL rVars] --> that you expect to integrate with Adobe Advertising in the future.

1. [Create a processing rule](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules) with the following settings:

   * Select the report suite for which you want to migrate AMO ID and EF ID <!-- [!DNL rVar] --> data to Experience Platform for use by Customer Journey Analytics.

   * For the [!UICONTROL Rule Title], use a descriptive name, such as "Copy AMO ID and EF ID to eVars."

   * In the [!UICONTROL Always Execute] section, add two actions to create the new eVars:
   
     * For the `AMO ID`: ```Overwrite value of <new/unused eVar> with amo.s_kwcid(Context Data)```

     * For the `EF ID`: ```Overwrite value of <new/unused eVar> With amo.ef_id(Context Data)```

   * For the [!UICONTROL Reason for rule], use a descriptive note, such as "AMO ID and EF ID will be transported to AEP via Adobe Analytics Connector."

1. Validate the saved processing rule.

   Once you save the processing rule, the data for the `AMO ID` and the `AMO EF ID` <!-- the existing reserved variables --> should be identical to the data for the two new eVars to which they are copied.
   
   For example, if the new eVar `eVar142` is mapped to `amo.s_kwcid(Context Data)`, then the data for the `eVar142` and the 'AMO ID` should be identical.

For more information about how processing rules are applied, see "[How processing rules work](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about)."

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising]](overview.md)
