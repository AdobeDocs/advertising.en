---
title: Implement conversion tracking using Adobe Experience Platform Tags
description: Learn about setting up Adobe Advertising conversion-tracking tags using Adobe Experience Platform Tags.
feature: Search Tracking
---
# Implement conversion tracking for Search, Social, & Commerce using Adobe Experience Platform Tags

You can set up conversion tracking using tags in Adobe Experience Platform (formerly known as Adobe Experience Platform Launch).

<!-- You can use tags in Adobe Experience Platform (formerly known as Adobe Experience Platform Launch) to track conversions for Search, Social, & Commerce. -->

<!--Clarify if this is for Advertising conversion tracking tags or if it's for AEP tracking tags. -->

The following tasks are required to configure conversion tracking tags for Search, Social, & Commerce from the Experience Platform user interface or from the Experience Platform Data Collection user interface. For full information and instructions for configuring tags, see the Experience Platform Tags Guide, beginning with the "[Tags overview](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home)" and "[Quickstart guide](https://experienceleague.adobe.com/en/docs/experience-platform/tags/get-started/quick-start)."

1. Install the Adobe Advertising [Extension](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/extensions/overview):

   1. From the applicable property, open the extension catalog and select **Adobe Advertising**.
   
   1. From the pulldown menu, select **SSC** (for Search, Social, & Commerce).

   1. In the **SSC UserID** field, enter the numeric user ID for your  organization's Search, Social, & Commerce account.

      If you don't know your user ID, contact your Adobe Account Team.

   1. Click **Save**.

1. Create a new rule (such as "form_completes") to trigger the Search, Social, & Commerce conversion tag:

   1. In the Event Configuration section:
   
      1. Select the following values:
   
         **Extension:** `Core`
      
         **Event Type:** `Library Loaded (Page Top)`
      
      1. Click **Keep Changes**.

   1. In the Condition Configuration section:
   
      1. Specify the following values:
   
         **Logic Type:** `Regular`
      
         **Extension:** `Core`

         **Condition Type:** `Path Without Query String`
         
         **Return true if path equals:** The path where the conversion should be tracked (for example, `/form_complete`).
      
      1. Click **Keep Changes**.

   1. In the Action Configuration section:
   
      1. Specify the following values:
      
         **Extension:** `Adobe Advertising`

         **Action Type:** `AMO Measurement`
         
         **Conversion Property Name:** The name of the conversion property (for example, `form_completes`).

         **Value:** The numeric value of the conversion property (for example `1` to track form_completes), or choose an existing [data element](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements).
      
      1. Click **Keep Changes**.

   1. Save the rule.
   
1. Publish the changes.
