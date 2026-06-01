---
title: (New UI) Create a conversion action for a [!DNL Google Ads] enhanced conversion for leads
description: Learn how to create a [!DNL Google Ads] conversion action for an enhanced conversion for leads.
feature: Conversions
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
    internal-label: Conversion tracking
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
    internal-label: Conversions
---
# (New UI) Create a conversion action for a [!DNL Google Ads] enhanced conversion for leads

*Beta feature*

*[!DNL Google Ads] accounts only*

You can create conversion actions for [!DNL Google Ads] enhanced conversions for leads to be tracked for individual [!DNL Google Ads] accounts, not conversions tracked at a manager account level.

Once you create the conversion action and implement a conversion tracking tag, you can [upload the offline conversion data that your organization captures](conversions-upload-offline-enhanced-conversions.md) and attribute it to the conversion action.

Support isn't available for [!DNL Microsoft Advertising] accounts.

## Create a conversion action

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Conversions]**.

1. Above the data table, click **[!UICONTROL Set up Conversion]**.

1. Specify the [conversion action settings](#conversion-action-settings-google).

   1. Select the [!UICONTROL Setup Method] *[!UICONTROL Create Conversion]*.
   
   1. Select the account, and then select the conversion type: *[!UICONTROL Import conversion]*.

   1. Click **[!UICONTROL Next]**.

   1. Specify the conversion action options.

   1. Click **[!UICONTROL Review and Save]** to review the settings.

   1. Click **[!UICONTROL Generate]**.

1. Read information about how to create a tracking tag for the enhanced conversion for leads, and then click **[!UICONTROL Next]**.

   You must create the conversion tag and implement it as needed on the websites from which you want to track the conversion metric. You'll also need to enable enhanced conversions for leads and agree to customer data terms and conditions. For instructions, see the [!DNL Google Ads] instructions to "[Configure the [!DNL Google] tag for enhanced conversions for leads](https://support.google.com/google-ads/answer/11021502)."

   If you want to track transaction-specific-conversion values, [customize your event snippet](https://support.google.com/google-ads/answer/6095947).

1. Click **[!UICONTROL Close].**

## Conversion action settings {#conversion-action-settings-google}

### Set-up Path section

**[!UICONTROL Setup Method]:** The type of action: *[!UICONTROL Create Conversion]*

**[!UICONTROL Platform]:** The ad network: *[!UICONTROL Google]*.

### Conversion Details section

**[!UICONTROL Select Account]:** The applicable [!DNL Google Ads] account.

**[!UICONTROL Type of conversions]:** The type of conversion to track: Select *[!UICONTROL Import conversion]*. All other types are used to create conversion tracking tags (not conversion actions) for other types of conversions.

### Conversion Settings section

**[!UICONTROL Conversion Name]:** A unique name for the conversion action.

**[!UICONTROL Goal Category]:** The conversion category, such as *Qualified lead* or *Sign-up*.

**[!UICONTROL Preferred Action optimization]:** Whether the goal is a *[!UICONTROL Primary action used for bidding optimization]* or a *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Conversion Value]:** How to measure the [value of each conversion](https://support.google.com/google-ads/answer/13064207):

* *[!UICONTROL Use the same value for each conversion],* which requires you to select a currency and enter the value for each conversion.

* *[!UICONTROL Use different values for each conversion],* which requires you to select a currency and enter a default value for each conversion. You can change the default value in the tag with a transaction-specific value when you implement the tag on a specific webpage.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [How many conversions to count per click or interaction](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* or *[!UICONTROL One (Recommended for leads, sign-ups and other conversions for which only the first interaction is valuable)]*.

**[!UICONTROL Click-Through Conversion Window]:** The maximum number of days after an ad interaction for which conversions are recorded. For search, display, and shopping campaigns, the window can be from 1-90 days. Select a number or select **[!UICONTROL Custom]** and enter a number.

**[!UICONTROL View-Through Conversion Window]:** The maximum number of days after a user views your ads for which view-through conversions are recorded. For search, display, and shopping campaigns, the window can be from 1-90 days. Select a number or select **[!UICONTROL Custom]** and enter a number.

**[!UICONTROL Attribution Model]:** [The attribution model that determines how much credit each ad interaction gets](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* or *[!UICONTROL Last click]*.

>[!MORELIKETHIS]
>
>* [(New UI) Upload offline conversion data for enhanced conversions](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Upload offline conversion data for enhanced conversions](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Implement [!DNL Google Ads] enhanced conversions for leads](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
