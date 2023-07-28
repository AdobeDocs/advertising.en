---
title: Change the transaction properties available in management views and reports
description: Learn how to make transaction properties available in your management views and reports.
exl-id: a8f3a2d6-4203-42db-96cd-faf02d20d247
feature: "Search Admin, Search Transaction Properties"
---
# Change the transaction properties available in management views and reports

When Adobe Advertising tracks a [transaction property](/help/search-social-commerce/glossary.md#s-t) for an advertiser, it's initially excluded from portfolio objectives, reports, and management views. To make a property visible, you must explicitly make it available, and then optionally change the default
display name, which is the name that's shown. The only exception is that conversions tracked by [!DNL Google Ads], [!DNL Google Analytics], and [!DNL Microsoft® Advertising] universal event tracking tags are automatically available and visible.

Similarly, you can hide a property from portfolio objectives, reports, and management views. When you hide a property that previously was visible, it's removed from any derived metrics that contain the property.

From the list of properties that are available, each user with access to the advertiser's data can customize the properties they see for management views and reports, including or omitting specific properties as they choose.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties]**.

   All transaction properties that have been gathered for the advertiser, and any different names that have been specified for display, are listed.

1. (Optional) Filter the list:

   * To search for a specific property name or display name, click ![Search](/help/search-social-commerce/assets/search.png "Search"), enter the word or string in the input field, and then press the **[!DNL Enter]** key.
   
     You can search for strings that appear anywhere within the phrase (such as the first letter or the last three letters), and the search terms aren't [case-sensitive](/help/search-social-commerce/glossary.md#c-d).
     
   * To search for properties by their availability in management views and reports, click ![Filter](/help/search-social-commerce/assets/filter.png "Filter"), and select the filter **[!UICONTROL Show in UI and Reports]**. Then select either **[!UICONTROL Show]** (to view the properties available to include in reports and management views) or **[!UICONTROL Hide]** (to view the properties not available in reports and management views).

1. Change the properties available for management views and reports:

   * To show or hide a single property, click the switch in the **[!UICONTROL Show in UI and Reports]** column to change the setting.
   
   * To show or hide multiple properties, do the following:
   
     1. Select the check box next to each property.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

     1. In the toolbar above the data table, click ![Show](/help/search-social-commerce/assets/show.png "Show") to show the properties or ![Hide](/help/search-social-commerce/assets/hide.png "Hide") to hide the properties.
     
     1. (To hide properties) In the confirmation message, click **[!UICONTROL Yes]** to hide the properties, including removing them from any derived metrics that contain the properties.

1. (Optional) [Change the name that appears in column headings](transaction-property-edit-display-name.md) for any of the properties.

   The default display name for each visible property is the property name as it's spelled in the retrieved data.

>[!NOTE]
>
>If Adobe Advertising collects data for new properties, then the new properties &mdash; except for conversions tracked by [!DNL Google Ads], [!DNL Google Analytics], and [!DNL Microsoft® Advertising] universal event tracking tags &mdash; are automatically excluded from management views and reports until you include them. New conversions tracked by [!DNL Google Ads], [!DNL Google Analytics], and [!DNL Microsoft® Advertising] universal event tracking tags are always automatically available.

>[!MORELIKETHIS]
>
>* [About managing an advertiser's transaction properties](transaction-property-about.md)
>* [View the transaction properties tracked for an advertiser](transaction-property-view-tracked.md)
>* [Change the display name for a transaction property](transaction-property-edit-display-name.md)
