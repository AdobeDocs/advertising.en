# Create a DSP Custom Goal from Adobe Analytics eVars and Props

<!-- not using original title: Optimize Adobe Advertising DSP Campaigns With Analytics eVars and Props -->

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

*Advertisers with Advertising DSP only* <!-- Is this for DSP only, or also for Search? If Search also, then change all language below. -->

You can use custom goals to optimize DSP packages based on Adobe Analytics site data that best fit your brand’s objectives. Custom goals are automatically built from success event metrics.<!-- dimensions aren't conversions or site engagement metrics, are they?? --> You can also configure your own custom optimization goals based on [!DNL Analytics] [eVars](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) and [props](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html).

To funnel eVar- and prop-level data into a custom success event, first create a placeholder event. Then create a processing rule to apply to incoming data.

Reach out to adcloud_support@adobe.com for more information.

1. In [!DNL Analytics], create a placeholder success event](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   Use the following additional parameters:
   
   **Type:** `Counter``
   **Polarity:**  either `Up is Good` or `Up is Bad``
   **Visibility:** `Visible Everywhere``
   **Unique Event Recording:** `Always Record Event``
   **Participation:** `Enabled``

   You don't need to place the newly created event on your brand’s website because it will use existing data that's already captured.

1. Create a processing rule in [!DNL Analytics]:

   >[!NOTE]
   >
   >Only [!DNL Analytics] account administrators can create processing rules unless they've granted permission to non-administrators.

   1. [Create a processing rule](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en), using the following configuration:

      * For the condition that must be met, specify the required eVar or prop. <!-- only one, or can you use multiple? -->
   
        You can configure additional levels of granularity as needed to ensure that the most accurate events are created.
     
      * For the action, select **Set Event** and select the placeholder event.

   1. In [!DNL Analytics] [!DNL Analysis Workspace], [create a project](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html and pull the new event into a freeform table to ensure that data is populating for the eVar or prop metric. 

To enable the new metric as a custom goal for optimization, contact your Adobe Account Team.<!-- Are the metrics automatically available as custom goals in Search, or does something have to be done on the backend to enable them? -->

