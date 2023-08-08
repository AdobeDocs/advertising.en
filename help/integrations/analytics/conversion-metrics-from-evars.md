---
title: 
description: 
feature: Integration with Adobe Analytics
---
# Create conversion metrics from Adobe Analytics eVars and props

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

You can use success event metrics to optimize DSP packages and Search, Social, & Commerce campaigns based on Adobe Analytics site data that best fits your brand’s objectives. You can configure custom success event metrics based on your existing [!DNL Analytics] [eVars](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) and [props](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) by funneling eVar- and prop-level data into an event. Other [!DNL Analytics] metrics, including standard, custom, and reserved conversion metrics and traffic metrics, are automatically available in DSP and Search, Social, & Commerce.

Most of the following tasks must be performed by an [!DNL Analytics] administrator or other user. If you need assistance, contact your technical support team (DSP users: `adcloud_support@adobe.com`; Search, Social, & Commerce users: `<Your Search, Social, & Commerce user account>@support.efrontier.com`).

1. In [!DNL Analytics], [create a placeholder success event](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   Use the following additional parameters:
   
   **Type:** `Counter`

   **Polarity:**  either `Up is Good` or `Up is Bad`

   **Visibility:** `Visible Everywhere`

   **Unique Event Recording:** `Always Record Event`

   **Participation:** `Enabled`

   You don't need to implement the new event on your brand’s website because it uses existing data that's already captured.

1. Create a processing rule in [!DNL Analytics]:

   >[!NOTE]
   >
   >Only [!DNL Analytics] account administrators can create processing rules unless they've granted permission to non-administrators.

   1. [Create a processing rule](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en), using the following configuration:

      * For the condition that must be met, specify the required eVars or props.
      
        You can configure additional levels of granularity as needed to ensure that the most accurate events are created.
        
        >[!TIP]
        >
        >The best practice is to use only one eVar or prop.
     
      * For the action, select **Set Event** and select the placeholder event.

   1. In [!DNL Analytics] [!DNL Analysis Workspace], [create a project](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) and pull the new event into a freeform table to ensure that data is populating for the eVar or prop metric. 

1.  Contact your Adobe Account Team to sync the new metric into Adobe Advertising.

After the metric is available, can use it to create an objective, which you can then assign to a Search, Social, & Commerce portfolio or use as a [custom goal](/help/dsp/optimization/custom-goal-about.md) for a DSP package.

For more information about creating objectives, see the Optimization Guide chapter on "Objectives," which is available from within Search, Social, & Commerce.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Data in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
<!--
>* [](/help/search-social-commerce/admin/conversion-metrics/ ????????)
-->