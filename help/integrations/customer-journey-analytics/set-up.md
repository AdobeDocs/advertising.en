---
title: Set up data collection, data transfer, and reporting  
description: Learn how to set up data collection, data transfer, and reporting.
feature: Integration with Adobe Customer Journey Analytics
---
# Set up data collection, data transfer, and reporting

*Beta feature*

The following tasks are required to view Advertising Cloud data in Customer Journey Analytics.

1. (Your organization's web analyst; optional) [Collect historical data for AMO IDs and EF IDs](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}.

   This step is applicable only for advertisers with [!DNL Analytics for Advertising].

1. (Your organization's site administrator for Adobe Experience Platform) [Set up data collection in Experience Platform and implement conversion tracking tags](#data-collection).

1. (Your organization's site administrator for Customer Journey Analytics) [Create a connection to your Experience Platform datasets in Customer Journey Analytics](#dataset-connection).

1. (Your organization's web analyst) [Set up data views in Customer Journey Analytics](#cja-data-views).

1. (Your organization's web analyst) [Set up reports and visualizations in Customer Journey Analytics Workspace](#cja-reports).

The following sections include the detailed procedures, which include the tasks and settings required for the integration but do not explain all features available within the workflows. See the linked resources for full information.

## Set up data collection in Adobe Experience Platform and on your website {#data-collection}

The following tasks are required to set up data collection in Experience Platform and implement conversion tracking tags. Your organization's site administrator for Experience Platform can perform these tasks, but your organization's IT department may need to help with deploying tracking tags.

1. Collect and send data from Adobe Advertising to Experience Platform Edge Network as a dataset:   

   1. In Experience Platform, [define a manual schema](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) for the data you want to collect using the Experience Data Model (XDM).

      * In the [!UICONTROL Schema Details], select **[!UICONTROL Experience Event]** as the base class for the schema to capture site events. Name your schema and click **[!UICONTROL Finish]**.
      
      * In the left panel, add the field group `Adobe Advertising Cloud ExperienceEvent Full Extension` to add fields specific to Adobe Advertising.<!-- Add link once published --> At a minimum, include the conversionDetails object with the `trackingCode` and `trackingIdentities` properties, which include the [AMO ID and EF ID](ids.html). The other fields are optional.
      
      * (Optional) Add additional field groups as needed to connect additional data fields to Adobe Advertising data.

      **Note:** You can create multiple schemas, but you can use only one schema per dataset and per datastream, which you'll create in the following steps.

   1. [Create a dataset](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create) based on the schema to store and manage the collection of event data. 

      * Choose the option to **[!UICONTROL Create dataset from schema]** and select your schema.
   
        Adobe Advertising creates additional datasets for the related summary metrics data (such as conversion values) and lookup data (dimensions/classification metadata, such as Adobe Advertising campaign name) based on your event dataset. Data for the datasets is populated in Experience Platform daily.

   1. [Create a datastream](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) for the schema. 
   
      * For the [!UICONTROL Mapping schema] setting, select your schema.

      * Add and enable the services `Adobe Advertising` and `Adobe Experience Platform` to the datastream.

        These services enable the Edge Network to store the dataset and to route it to Adobe Advertising.

      * For the [!UICONTROL Event dataset] setting, select your dataset.

        Each datastream can insert data into only one dataset.

1. Send your organization's website data to your Experience Platform datastream:

   1. Use Experience Platform [tags](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) (formerly known as [!DNL Launch]) to generate a JavaScript tag to send your organization's website data to the datastream.
   
      * Create a tag property, which is the container for the tag configuration.
         
      * For your property, [install the extension "Adobe Experience Platform Web SDK"](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) from the extensions catalog.
      
        This extension sends data from your web properties to Experience Cloud via the Experience Platform Edge Network.
        
        Don't use the Adobe Advertising extension.

      * Create a custom Web SDK build:
         
        * In the [!UICONTROL Custom build components] section, enable the **Advertising** component.
        
          This component includes all JavaScript code needed for Adobe Advertising in the tag. It also adds an "Advertising" setting in tag rules (which are optional) to define how advertising data is used for attribution measurement.
        
          You can optionally enable additional components as needed.
      
        * In the [!UICONTROL SDK Instances] section:
        
          * In the [!UICONTROL Datastreams] settings, select the datastream to use for each of your web environments (production, staging, development).
           
          * (Organizations with Adobe Advertising DSP only) In the [!UICONTROL Adobe Advertising] settings:
           
            * Enable the **[!UICONTROL Adobe Advertising DSP]** setting to enable view-through tracking.

            * Specify the advertisers for which to enable view-through tracking.

            * (Optional) Enter your organization's ID5 partner ID to collect IDs.

            * (Optional) Enter the path for your organization's [!DNL LiveRamp RampID] JavaScript code (ats.js) to collect IDs.

          * Save the build.
        
      * (Optional) [Create rules](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) as needed to determine when Web SDK should send data to the Edge Network.

        * For the [!UICONTROL Advertising] setting, define how advertising data is used for attribution measurement. This setting is helpful when the rule includes a sequence of multiple actions and is available only when you've selected the "[!UICONTROL Advertising]" component for the custom build component. Options include:
        
          *Automatic:* Allows advertising data to be used for measuring ad attribution on the current `sendEvent` action based on data in the cache. In this case, the ad exposure event fires when it gets the chance, and it may not be available for the current event. For example, if you fire a purchase checkout event and no ad exposure data is available in the cache, then the checkout event isn’t attributed to the ad exposure.
          
          *Wait:* Delays the execution of the call until the advertising data is successfully retrieved from the server and resolved, which ensures accurate attribution measurement. For example, you might want to wait for the ad exposure event to resolve before you fire a purchase checkout event. **Note:** Resolving IDs may take a few seconds depending on the browser and ID type. Use this option if the current `sendEvent` action can accommodate a few seconds of delay.
          
          *Disabled:* (The default) Excludes advertising data from the request that you're firing, making it unavailable for attribution or related tracking.
          
          *Provide a data element:* Use a data element to include or exclude advertising data during page load. Resolved values for the data element can include `automatic`, `wait`, and `disabled`. See the next step.

        If you don't use a rule to configure a `sendEvent` action, then advertising data is sent as a separate Advertisement enrichment event. 
   
      * Create [data elements](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) as needed to map variables on your website to the structure of the XDM schema you created previously.

   1. [Publish the tag](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) to a test environment in which you can iterate on the development of tags.
      
   1. Validate delivery of the datasets, and then [publish the tag to your live production environment](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

      Your organization's IT department or other group may need to schedule, or be informed about, the tag deployment.

## Create a connection to your Experience Platform datasets in Customer Journey Analytics {#dataset-connection}

Follow these steps to pull Adobe Advertising data from your Experience Platform datasets into Customer Journey Analytics. Your organization's site administrator for Customer Journey Analytics  can perform these tasks.

*Coming soon*

## Set up data views in Customer Journey Analytics {#cja-data-views}

In Customer Journey Analytics, create one or more data views to define the metrics and dimensions for reporting. A web analyst can perform these tasks.

*Coming soon*

## Set up reports and visualizations in Customer Journey Analytics Workspace {#cja-reports}

In Customer Journey Analytics Workspace, follow these steps to configure reports and visualizations. A web analyst can perform these tasks.

1. [Create a project](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) in Workspace to build reports and visualizations based on the dimensions and metrics configured within the data view.

1. (If you have data from [!DNL Google Ads] or [!DNL Microsoft Advertising]) Create a report of publisher-tracked conversions using fields for ad network-specific metrics, which are grouped as `googleConversions` and `microsoftConversions`.

>[!MORELIKETHIS]
>
>* [Overview](overview.md)
>* [Prerequisites](prerequisites.md)
>* [Adobe Advertising IDs Used by [!DNL Customer Journey Analytics]](ids.md)
>* [Adobe Advertising metrics and dimensions in Customer Journey Analytics](advertising-data-in-cja.md)
>* [Collect Historical Data for AMO IDs and EF IDs for Use in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Customer Journey Analytics Guide](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [User guide for Adobe Analytics users](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
