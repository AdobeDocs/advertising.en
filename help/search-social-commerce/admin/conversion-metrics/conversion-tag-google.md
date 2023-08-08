---
title: Create a conversion tag for [!DNL Google Ads]
description: Learn how to create a [!DNL Google Ads] conversion tag.
---
# Create a conversion tag for [!DNL Google Ads]

You can create conversion tags for new conversions to be tracked for individual [!DNL Google Ads] accounts, not tracked at a manager account level.

To generate conversion tags for existing conversions, use the ad network's editor.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Specify the [conversion tag settings](#conversion-tag-settings-google).

   1. Select the account, and then select the conversion type.

   1. Click **[!UICONTROL Next]**.

   1. Specify the conversion options.

   1. Click **[!UICONTROL Generate]**.

1. Copy the conversion tag and implement it on the websites from which you want to track the conversion metric.

   See "Installing the [!DNL Google] tag" in the [!DNL Google Ads] help to "[2. Set up your Google tag](https://support.google.com/google-ads/answer/12215519)."

1. Click **[!UICONTROL Done].**

Once you add the tags to your website and they begin firing, [!DNL Google Ads] records conversions on the website. Search, Social, & Commerce syncs the conversions daily. For more information about the data that's synced, see "[[!DNL Google Ads] conversion data in Search, Social, & Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Conversion tag settings {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** The applicable Google Ads account.

**[!UICONTROL Type of Conversion]:** The type of conversion to track: *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]*, or *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]:** A unique name for the conversion metric.

<!--  Add in later, when we officially release this

**\[Goal Category\]:** The conversion goal. The available goals vary by conversion type. For *[!UICONTROL Calls to a phone number on your website]* and *[!UICONTROL Clicks to your number on your mobile website]*, "[!UICONTROL Phone Call Lead]" is selected by default.

-->

**\[Action Type\]:** Whether the goal is a *[!UICONTROL Primary action used for bidding optimization]* or a *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** How to measure the [value of each conversion](https://support.google.com/google-ads/answer/3419241):

* *[!UICONTROL Use the same value for each conversion],* which requires you to select a currency and enter the value for each conversion.

* *[!UICONTROL Use a different value for each conversion],* which requires you to select a currency and enter a default value for each conversion. You can change the default value in the tag with a transaction-specific value when you implement the tag on a specific webpage.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [How many conversions to count per click or interaction](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* or *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** The maximum number of days after an ad interaction for which conversions are recorded. For search, display, and shopping campaigns, the window can be from 1-90 days. Select a number or select **[!UICONTROL Custom]** and enter a number.

**[!UICONTROL View Through Conversion Window]:** The maximum number of days after a user views your ads for which view-through conversions are recorded. For search, display, and shopping campaigns, the window can be from 1-90 days. Select a number or select **[!UICONTROL Custom]** and enter a number.

**[!UICONTROL Attribution Model]:** [How much credit each ad interaction gets](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*, *[!UICONTROL Last click]*, *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]*, or *[!UICONTROL Position based]*.

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] conversion data in Search, Social, & Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
