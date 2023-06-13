---
title: Operations you can perform in bulksheets
description: Reference general information about adding, editing, and deleting campaign data using bulksheets.
exl-id: 82969bb8-dff8-48e7-b37d-1446a2a90072
---
# Operations you can perform in bulksheets

You can add, edit, and delete campaign data via bulksheets for [supported ad networks](../bulksheet-about.md#bulksheet-functionality-by-network).

Include a separate data line for each campaign component (campaign, ad group, keyword, or text ad) that you want to add, edit, or delete; or whose properties you want to add, edit, or delete. For example, if you want to create a campaign with one ad group, one keyword, and one ad &mdash; four components total &mdash; you need four separate data lines. To edit the [!UICONTROL Ad Group Name] for an ad group (one component), however, you need only one line. Similarly, to edit four different properties for one ad group (one component), you need only one line.

The following rules apply to working with campaign components and their properties.

* Adding:

  * To add a component, include all fields required to add that component, plus optionally include fields for any of the component's properties.
  
  * To add a property for an existing component, such as the [!UICONTROL Ad Group End Date] for an ad group, include all fields required to edit that component (ad group) plus the field for the property ([!UICONTROL Ad Group End Date]).
  
* To edit a property for an existing component, include all fields required to edit that component plus the field for the property.

  If you leave the property field blank, the existing value is retained.

* Deleting:

  * To delete an existing component, include all fields required to edit that component and change its status to [!UICONTROL Deleted]. For example, to delete a [!DNL Google Ads] ad group, you must include the [!UICONTROL Campaign Name], [!UICONTROL Ad Group Name], [!UICONTROL Ad Group Status] with a value of <i>[!UICONTROL Deleted]</i>, and [!UICONTROL Ad Group ID].

  * ([!UICONTROL Param1], [!UICONTROL Param2], and [!UICONTROL Param3] values only) To delete an existing [!DNL paramN] value for a keyword, include all fields required to edit the keyword and also delete the existing [!DNL paramN] value by entering the value `[delete]` (including the brackets) in the corresponding field.

  * (Allowed property fields) To delete an existing property value for a component, include all fields required to edit that component and also delete the property value by entering the value `[delete]` (including the brackets). Allowed fields include:

    * ([!UICONTROL Google Ads] only) [!UICONTROL Description Line 1], [!UICONTROL Description Line 2]
    
    * ([!DNL Google Ads] and [!DNL Microsoft® Advertising] only) [!UICONTROL Product Scope Filter], [!UICONTROL Base URL/Final URL], [!UICONTROL Tracking Template]

>[!NOTE]
>
>When you include a value in a field that isn't applicable to the action, any value entered in the field is ignored.
  
>[!MORELIKETHIS]
>
>* [About managing campaign data using bulksheets](../bulksheet-about.md)
>* [Supported bulksheet file formats](bulksheet-file-formats.md)
>* [Appendix - Bulksheet errors](../bulksheet-errors.md)
>* [Download/Create a bulksheet file](../bulksheet-download.md)
