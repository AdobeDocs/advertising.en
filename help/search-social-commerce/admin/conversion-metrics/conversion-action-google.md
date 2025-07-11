---
title: Create a conversion action for a [!DNL Google Ads] enhanced conversion for leads
description: Learn how to create a [!DNL Google Ads] conversion action for an enhanced conversion for leads.
feature: Conversions
exl-id: faf4a6de-e82f-4afd-bda5-2602fb45aee5
---
# Create a conversion action for a [!DNL Google Ads] enhanced conversion for leads

*[!DNL Google Ads] accounts only*

You can create conversion actions for [!DNL Google Ads] enhanced conversions for leads to be tracked for individual [!DNL Google Ads] accounts, not conversions tracked at a manager account level.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Conversions]**, which opens the **[!UICONTROL Summary]** tab.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Specify the [conversion action settings](#conversion-action-settings-google).

   1. Select the account, and then select the conversion type: *[!UICONTROL Import conversion]*.

   1. Click **[!UICONTROL Next]**.

   1. Specify the conversion action options.

   1. Click **[!UICONTROL Generate]**.

1. Read information about how to create a tracking tag for the enhanced conversion for leads, and then click **[!UICONTROL Next]**.

   Create the conversion tag and implement it as needed on the websites from which you want to track the conversion metric. For instructions, see the following:
   
   * To use the [!DNL Google] tag, see the [!DNL Google Ads] instructions to "Configure [!DNL Google] tag settings" in "[Set up enhanced conversions for leads with the [!DNL Google] tag](https://support.google.com/google-ads/answer/11347292)."
   
   * To use [!DNL Google Tag Manager], see the [!DNL Google Ads] instructions to "Configure [!DNL Google] tag settings" and "Verify your setup and publish the container" in "[Set up enhanced conversions for leads with [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11021502?#configure)."

1. Click **[!UICONTROL Done].**

Once you create the conversion action and implement a conversion tracking tag, you can upload the offline conversion data that your organization captures and attribute it to the conversion action. See "[Upload offline conversion data for enhanced conversions](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)."

## Conversion action settings {#conversion-action-settings-google}

**[!UICONTROL Select an Account]:** The applicable Google Ads account.

**[!UICONTROL Type of Conversion]:** The type of conversion to track: Select *[!UICONTROL Import conversion]*. All other types are used to create conversion tracking tags (not conversion actions) for other types of conversions.

**[!UICONTROL Conversion Name]:** A unique name for the conversion action.

**\[Conversion Category\]:** The conversion category, such as *Qualified lead* or *Sign-up*.

**\[Action Type\]:** Whether the goal is a *[!UICONTROL Primary action used for bidding optimization]* or a *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** How to measure the [value of each conversion](https://support.google.com/google-ads/answer/13064207):

* *[!UICONTROL Use the same value for each conversion],* which requires you to select a currency and enter the value for each conversion.

* *[!UICONTROL Use a different value for each conversion],* which requires you to select a currency and enter a default value for each conversion. You can change the default value in the tag with a transaction-specific value when you implement the tag on a specific webpage.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [How many conversions to count per click or interaction](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* or *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** The maximum number of days after an ad interaction for which conversions are recorded. For search, display, and shopping campaigns, the window can be from 1-90 days. Select a number or select **[!UICONTROL Custom]** and enter a number.

**[!UICONTROL View Through Conversion Window]:** The maximum number of days after a user views your ads for which view-through conversions are recorded. For search, display, and shopping campaigns, the window can be from 1-90 days. Select a number or select **[!UICONTROL Custom]** and enter a number.

**[!UICONTROL Attribution Model]:** [How much credit each ad interaction gets](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* or *[!UICONTROL Last click]*.

>[!MORELIKETHIS]
>
>* [Upload offline conversion data for enhanced conversions](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Implement [!DNL Google Ads] enhanced conversions for leads](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
