# Create a DSP custom goal from Adobe Analytics eVars and props

<!-- Title:  Verify if this creates custom goals, or if it just makes them available in Search, where you can add them to objectives, which are used as custom goals. Reword title accordingly. Something like "Make Adobe Analytics eVars and props available for DSP package optimization" ? better wording -->

<!-- single "an eVar or prop?" or can each event include multiple? -->

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

*Advertisers with Advertising DSP only* <!-- Is this really for DSP only, or are the metrics also available for Search users in Portfolios > Objectives, and would Search users be likely to use them? If Search also, then change all language below. -->

You can use custom goals to optimize DSP packages based on Adobe Analytics site data that best fit your brand’s objectives. Custom goals are automatically built from success event metrics, including conversions and traffic metrics.<!-- it said "success event dimensions, but dimensions aren't conversions or site engagement metrics, are they?? --> You can also configure your own custom optimization goals based on your existing [!DNL Analytics] [eVars](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) and [props](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) by funneling eVar- and prop-level data into a custom success event.

<!--If you need assistance, contact adcloud_support@adobe.com.-->
<!-- Do we want to offer that? Shouldn't they just talk to their Account Team? -->

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

      * For the condition that must be met, specify the required eVar or prop. <!-- only one, or can you use multiple? -->
   
        You can configure additional levels of granularity as needed to ensure that the most accurate events are created.
     
      * For the action, select **Set Event** and select the placeholder event.

   1. In [!DNL Analytics] [!DNL Analysis Workspace], [create a project](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) and pull the new event into a freeform table to ensure that data is populating for the eVar or prop metric. 

To enable the new metric as a custom goal for optimization, contact your Adobe Account Team.<!-- Are the metrics automatically visible in Search and available for objectives, or does something have to be done on the backend to enable them? -->

