---
title: Set up data collection, data transfer, and reporting
description: Learn how to set up data collection, data transfer, and reporting.
feature: Integration with Adobe Customer Journey Analytics
exl-id: a955e2b0-ea1b-4b5c-937b-f8c66603cd36
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

### Collect and send data from Adobe Advertising to Experience Platform Edge Network as a dataset   

1. In Experience Platform, [define a manual schema](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) for the data you want to collect using the Experience Data Model (XDM).

   * In the [!UICONTROL Schema Details], select **[!UICONTROL Experience Event]** as the base class for the schema to capture site events. Name your schema and click **[!UICONTROL Finish]**.
   
   * In the left panel, add the field group `[Adobe Advertising Cloud ExperienceEvent Full Extension](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension)` to add fields specific to Adobe Advertising. At a minimum, include the conversionDetails object with the `trackingCode` and `trackingIdentities` properties, which include the [AMO ID and EF ID](ids.md). The other fields are optional.
   
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

### Send your organization's website data to your Experience Platform datastream

1. Use Experience Platform [tags](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) (formerly known as [!DNL Launch]) to generate a JavaScript tag to send your organization's website data to the datastream.
   
   * Create a tag property, which is the container for the tag configuration.
   
   * For your property, [install the extension "Adobe Experience Platform Web SDK"](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) from the extensions catalog.
   
     This extension sends data from your web properties to Experience Cloud via the Experience Platform Edge Network.
     
     Don't use the Adobe Advertising extension.

   * Create a [custom Web SDK build](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build):
   
     * In the [!UICONTROL Custom build components] section, enable the **Advertising** component.
     
       This component includes all JavaScript code needed for Adobe Advertising in the tag. It also adds an "Advertising" setting in tag rules (which are optional) to define how advertising data is used for attribution measurement.
       
       You can optionally enable additional components as needed.
       
     * In the [!UICONTROL SDK Instances] section:
     
       * In the [!UICONTROL Datastreams] settings, select the datastream to use for each of your web environments (production, staging, development).
       
       * (Organizations with Adobe Advertising DSP only) In the [[!UICONTROL Adobe Advertising] settings](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#general), enable **[!UICONTROL Adobe Advertising DSP]** to permit view-through tracking and specify the advertisers for which to enable view-through tracking. You can optionally collect IDs from universal IDs.
         
       * Save the build.
        
   * (Optional) [Create rules](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) as needed to determine when Web SDK should send data to the Edge Network.
   
     * For `[sendEvent](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/action-types#send-event)` actions, use the [[!UICONTROL Advertising] setting](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising) to define how advertising data is used for attribution measurement. This setting is helpful when the rule includes a sequence of multiple actions and is available only when you've selected the "[!UICONTROL Advertising]" component for the custom build component.
   
   * Create [data elements](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) as needed to map variables on your website to the structure of the XDM schema you created previously.

1. [Publish the tag](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) to a test environment in which you can iterate on the development of tags.
      
1. Validate delivery of the datasets, and then [publish the tag to your live production environment](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

   Your organization's IT department or other group may need to schedule, or be informed about, the tag deployment.

## Create a connection to your Experience Platform datasets in Customer Journey Analytics {#dataset-connection}

Follow these steps to pull Adobe Advertising data from your Experience Platform datasets into Customer Journey Analytics. Your organization's site administrator for Customer Journey Analytics can perform these tasks.

1. In Customer Journey Analytics, [create a connection](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) that includes your Experience Platform datasets and schema.

   **Note:** Currently, you must send data for all DSP and Search, Social, & Commerce accounts to a single Experience Platform instance and sandbox.
   
   * Add your Experience Platform event (metrics) dataset, summary (metrics) dataset, and dimensions (classifications/metadata) dataset.

     Your team created the event dataset, and Adobe Advertising created the summary and dimensions datasets based on your event dataset.
     
     You can optionally include additional datasets as needed.

   * Map the dimensions dataset to the events dataset:

     1. Open the settings for the dimension dataset.
     
        The heading on the settings page is "[!UICONTROL Lookup Dataset]," which indicates that you can join your dimensions dataset with one of your metric-specific datasets.
   
     1. In the [!UICONTROL Adobe Advertising Dimensions] section, map the dimensions dataset to the events dataset:
      
        1. For the [!UICONTROL Key] field, select the field to use as the key for the dimensions dataset: `Adobe Advertising ID` (which is same as the `trackingCode` field in the schema).
      
        1. For the [!UICONTROL Matching key] field, select the field to use as the matching key for the events dataset. The available field names include the dataset name in parentheses. For example, if you're mapping your dimensions dataset to your events dataset, select `Tracking Code (Event datasets)`.
        
        Later, you'll also map the events dataset to the summary dataset when you set up your data view(#cja-data-views).

1. After a couple of hours, verify that the data is available in Customer Journey Analytics.

   1. In Customer Journey Analytics, go to **[!UICONTROL Connections]** and select your connection.

   1. In the list of data sets displayed, verify that the "[!UICONTROL Number of Records]" report shows that data was added.

## Set up data views in Customer Journey Analytics {#cja-data-views}

In Customer Journey Analytics, create one or more data views to define the metrics and dimensions for reporting. A web analyst can perform these tasks.

1. In Customer Journey Analytics, [create a data view](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview).

1. Configure the view to include the following information.

   * If you have an Adobe Analytics account, use the [!UICONTROL Time Zone] for your [!DNL Analytics] account in the [!UICONTROL Calendar] section of the [!UICONTROL Configure] tab.
   
   * On the [!UICONTROL Components] tab:
   
     * Add your dimensions, events, and summary datasets.
     
     * Choose metrics from your events (metrics) dataset and your dimensions (classifications/metadata) dataset to include in the data view.
     
       You already joined these two datasets in the connection that you created in the [last procedure](#dataset-connection).
     
     * Join the events dataset to the summary dataset, which isn't yet joined to anything:
     
       * For each dimension with summary data that you want to be available in Customer Journey Analytics, [create a derived field](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/derived-fields).

         For example, to view summary data for campaigns, create a derived field for the dimension `Adobe Advertising Campaign`.
         
         You'll link the two datasets using the matching key `trackingCode` (which is the schema field for the Adobe Advertising ID).
       
         * In the [!UICONTROL Lookup] section of the derived rule builder:
         
           * For the **[!UICONTROL Value]** field, select "[!UICONTROL Tracking Code]" from the metrics summary dataset.

           * For the **[!UICONTROL Lookup dataset]** field, select the dimensions dataset (such as "Adobe Advertising Classification").

           * For the **[!UICONTROL Matching Key]** field, select "[!UICONTROL Tracking Code]" from the classification dataset.

           * For the **[!UICONTROL Values to return]** field, select the dimension (such as "[!UICONTROL Adobe Advertising Campaign]")" from the classification dataset.
         
         The derived field name is appended with "(DF)", such as `Adobe Advertising Campaign(DF)`. 
         
       * For each derived field:
       
         * In the [!UICONTROL Included components] section, add the derived field.
         
           Two names are now listed for the same dimension (for example, "Adobe Advertising Campaign(DF)" (the derived field) and "Adobe Advertising Campaign" (the field in the summary dataset)).

         * Select the dimension in the summary dataset (such as "Adobe Advertising Campaign") and edit the settings for the dataset.

           The settings open on the right.

           * In the the Summary Data Group section, select the option to **[!UICONTROL Create grouping]**.

           * For the **[!UICONTROL Dimension]** field, select the derived field (which is appended with "(DF)," such as "Adobe Advertising Campaign(DF)").
         
           * Select the option to **[!UICONTROL Hide in reporting]**, which hides the derived field name in Workspace.

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
