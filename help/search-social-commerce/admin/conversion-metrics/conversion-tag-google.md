---
title: Create a conversion tag for [!DNL Google Ads]
description: Learn how to create a [!DNL Google Ads] conversion tag.
exl-id: 322be2d5-0d66-4d0c-a17a-619a1f6c0644
---
# Create a conversion tag for [!DNL Google Ads]

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Specify the [conversion tag settings](#conversion-tag-settings-google).

   1. Select the account, and then select the conversion type.

   1. Click **[!UICONTROL Next]**.

   1. Specify the conversion options.

   1. Click **[!UICONTROL Generate]**.

After you create the tag, copy it and implement it on the websites from which you want to track the conversion metric. See "Installing the Google tag" in the Google Ads help to "[2. Set up your Google tag](https://support.google.com/google-ads/answer/12215519)."

Once you implement the tag on your website and the tag is fired, [!DNL Google Ads] starts recording conversions on the website. Adobe Advertising syncs the conversion as 3 corresponding conversions – Count, Value and Cross-Device. The display name convention is as follows:
Count – CT_<Conversion Name in Google>
Value - <Conversion Name in Google>
Cross-Device - XD_<Conversion Name in Google>

## Conversion tag settings {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** The applicable Google Ads account.

**[!UICONTROL Type of Conversion]:** The type of conversion to track: *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]*, or *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]:** A unique name for the conversion metric.

**\[Goal Category\]:** The conversion goal. The available goals vary by conversion type. For *[!UICONTROL Calls to a phone number on your website]* and *[!UICONTROL Clicks to your number on your mobile website]*, "[!UICONTROL Phone Call Lead]" is selected by default.

**\[Action Type\]:** Whether the goal is a *[!UICONTROL Primary action used for bidding optimization]* or a *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** How to measure the [value of each conversion](https://support.google.com/google-ads/answer/3419241): *[!UICONTROL Use the same value for each conversion]*, *[!UICONTROL Use a different value for each conversion]*, or *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*.

**[!UICONTROL Count]:** [How many conversions to count per click or interaction](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* or *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** The maximum number of days after an ad interaction for which conversions are recorded. For search, display, and shopping campaigns, the window can be from 1-90 days. Select a number or select **[!UICONTROL Custom]** and enter a number.

**[!UICONTROL View Through Conversion Window]:** The maximum number of days after a user views your ads for which view-through conversions are recorded. For search, display, and shopping campaigns, the window can be from 1-90 days. Select a number or select **[!UICONTROL Custom]** and enter a number.

**[!UICONTROL Attribution Model]:** [How much credit each ad interaction gets](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*, *[!UICONTROL Last click]*, *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]*, or *[!UICONTROL Position based]*.

