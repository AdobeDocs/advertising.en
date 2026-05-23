---
title: (New UI) Manage custom alerts
description: Learn how to create, configure, pause, activate, delete, view, and export custom alerts and alert templates.
feature: Search Alerts
---
# (New UI) Manage custom alerts

Create alert templates to identify when any portfolio, campaign, or ad group meets specific conditions &mdash; such as a performance metric &mdash; during a specified period and then generate an alert. Alerts are available for a single advertiser. Alerts include all columns in the relevant default view. For example, campaign-level alerts include all columns in the default [!UICONTROL Campaigns] view.

You can create alert templates from either the [!UICONTROL Alert Templates] tab in the [!UICONTROL Custom Alerts] panel or from the top of any page.

When an alert instance is triggered for an alert template:

* The specified recipients receive an email notice. When the alert contains up to 1000 records, the email notice includes a [CSV](/help/search-social-commerce/glossary.md#c-d) file with the alert data, including data for all entities that triggered the alert.

* The alert is listed on the [!UICONTROL Triggered Alerts] tab in the [!UICONTROL Custom Alert Templates] panel.<!-- Not available as of 5/22 for alerts triggered the day before:  A downloadable report is available for ten days after the alert is triggered. -->

<!-- This doesn't seem to be true as of 5/22 -- check on this behavior:    * The alert is listed in the [!UICONTROL Notifications] center in the applicable entity view, which is available from the right toolbar. Notifications remain in the [!UICONTROL Notifications] center unless you delete them or mark them as read. -->

## The [!UICONTROL Custom Alerts] view

To open the [!UICONTROL Custom Alerts] panel, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") in the upper right.

The [!UICONTROL Custom Alerts] panel includes the [!UICONTROL Alert Templates] view, which lists all alert templates created for the account and from which you can create, edit, pause, reactivate, and delete alert templates. The [!UICONTROL Triggered Alerts] view lists the generated alert instances.

## Available actions

* [View triggered alerts](#alert-view)

* [View custom alert templates](#alert-template-view)

* [Create a custom alert template](#alert-template-create)

* [Edit a custom alert template](#alert-template-edit)

* [Pause a custom alert template](#alert-template-pause)

* [Activate a custom alert template](#alert-template-activate)

* [Delete a custom alert template](#alert-template-delete)

<!-- Not available as of 5/22:  * [Export data for triggered alerts](#alert-export-data) -->

## View triggered alerts {#alert-view}

1. In the upper right of any page, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert").

1. Click the **[!UICONTROL Triggered Alerts]** tab.

1. (Optional) Filter the list to include alerts for a specific entity type, or search for a text string within the template name. Search queries aren't case-sensitive.

## View custom alert templates {#alert-template-view}

1. In the upper right of any page, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert"), which opens to the [!UICONTROL Alert Templates] tab.

1. (Optional) Filter the list to include alerts for a specific entity type, or search for a text string within the template name. Search queries aren't case-sensitive.

1. (Optional) To view all criteria for an alert template, click the number of criteria (such as ![Example custom alert criteria button](/help/search-social-commerce/assets/custom-alert-criteria.png "Example custom alert criteria button").

## Create a custom alert template {#alert-template-create}

New alert templates have the status "[!UICONTROL Active]."

1. Do either of the following:

   * In the upper right of any page, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL Create Custom Alert]**.
   
   In the upper right of any page, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL View Custom Alerts]**, which opens to the [!UICONTROL Alert Templates] tab. Click **[!UICONTROL Create Alert]**.

1. Specify the [alert settings](#alert-template-settings) on the **[!UICONTROL Entity]**, **[!UICONTROL Date Range]**, **[!UICONTROL Filters]**, and **[!UICONTROL Scheduling and Delivery]** tabs.

   You can move between tabs by clicking the tab name (such as "Filters") or by clicking **[!UICONTROL Next]** in the bottom right.

1. On the [!UICONTROL Summary] tab, click **[!UICONTROL Create Alert]**.

## Edit a custom alert template {#alert-template-edit}

1. In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL View Custom Alerts]**, which opens to the [!UICONTROL Alert Templates] tab.

1. (Optional) Filter the list to include alerts for a specific entity type, or search for a text string within the template name. Search queries aren't case-sensitive.

1. Next to the template name, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit").

1. In the [!UICONTROL Edit Custom Alert] window, edit the [alert settings](#alert-template-settings) on the **[!UICONTROL Date Range]**, **[!UICONTROL Filters]**, and **[!UICONTROL Scheduling and Delivery]** tabs.

   You can move between tabs by clicking the tab name (such as "Filters") or by clicking **[!UICONTROL Next]** in the bottom right.

1. On the [!UICONTROL Summary] tab, click **[!UICONTROL Update Alert]**.

## Pause a custom alert template {#alert-template-pause}

1. In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL View Custom Alerts]**, which opens to the [!UICONTROL Alert Templates] tab.

1. (Optional) Filter the list to include alerts for a specific entity type, or search for a text string within the template name. Search queries aren't case-sensitive.

1. In the template row, select *[!UICONTROL Paused]*.

## Activate a custom alert template {#alert-template-activate}

1. In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL View Custom Alerts]**, which opens to the [!UICONTROL Alert Templates] tab.

1. (Optional) Filter the list to include alerts for a specific entity type, or search for a text string within the template name. Search queries aren't case-sensitive.

1. In the template row, select *[!UICONTROL Active]*.

## Delete a custom alert template {#alert-template-delete}

You can delete only the alert templates that you created.

1. In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL View Custom Alerts]**, which opens to the [!UICONTROL Alert Templates] tab.

1. (Optional) Filter the list to include alerts for a specific entity type, or search for a text string within the template name. Search queries aren't case-sensitive.

1. In the template row, click ![Delete](/help/search-social-commerce/assets/delete-new.png "Delete").

1. In the confirmation message box, click **[!UICONTROL Delete]**.

## Custom alert template settings {#alert-template-settings}

| Tab | Parameter | Description |
|--- |--- |--- |
|  | [!UICONTROL Name] | The alert name. It must include at least five characters. |
|[!UICONTROL Date Range]|[!UICONTROL Select Entity] | The entity type to be evaluated: <i>[!UICONTROL Portfolio]</i>, <i>[!UICONTROL Campaign]</i>, or <i>[!UICONTROL Ad Group]</i>. |
| [!UICONTROL Date Range] | [!UICONTROL Period] | The date range for which to evaluate the conditions for the alert. Metrics are evaluated in aggregate across the date range. The options range from *[!UICONTROL Yesterday]* to *[!UICONTROL Last 180 Days]*. |
| [!UICONTROL Filters] | \[Defined filters\] | The conditions for triggering the alert at the time specified on the [!UICONTROL Scheduling and Delivery] tab. The available columns vary by the entity type. All filters are joined using the Boolean function AND, which means that all specified conditions must be met.<ul><li><p>To add a filter, do the following:<p><ol><li><p>(Optional) To filter the column names by text string, enter the search string in the [!UICONTROL ADD FILTER] input field.</p></li><li><p>In the column list, select a column name.</p></li><li><p>Define the filter on the column:</p></li><ul><li><p>(Filters without input fields) Click ![Down arrow](/help/search-social-commerce/assets/arrow-down-expand.png "Down arrow") next to the second menu, and then select the check boxes next to each value to include.</p></li><li><p>(All other filters with input fields) Select an operator from the second menu, and then enter the applicable value.</p><p>For example, if you've selected the "Clicks" column and want to return only rows with more than 100 clicks, then select "greater than" and enter 100 in the input field.</p><p>Depending on the data type, available operators may include <i>greater than</i>, <i>less than</i>, <i>equals</i>, <i>contains</i>, <i>doesn't contain</i>, <i>starts with</i>, <i>ends with</i>, <i>no value</i>, <i>has value</i>, <i>before</i>, <i>after</i>, or <i>no date</i>.</p><p>**Note:** Text values aren't case-sensitive. For example, if you filter by campaigns with "loan" in the name, then the results could include "Consumer Loans" and "loan applications."</p></li></ol><li><p>To remove a filter, click ![Delete](/help/search-social-commerce/assets/delete.png "Delete") next to the filter definition.</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Trigger this Alert] \[when\] | How often the alert checks for the specified condition filters and, when all conditions are met, sends email notifications:<ul><li><p>[!UICONTROL Daily at <*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Weekly on <*Day of Week*> at <*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Every month on <*Day NN*> at <*NN*> `[AM\|PM]`]</p></li></ul>**Note:** This value doesn't affect the evaluation period. |
|  | [!UICONTROL Email Recipients] | (Editable only by the creator of the alert template; read-only for everyone else) Registered Search, Social, & Commerce users to which to send notifications when an alert is triggered. By default, tthe name for your user account is selected. Optionally add or remove users with access to the advertiser's data.<br><br>When the alert includes up to 1000 records, a CSV version of the alert is attached to the email message. |

<!--

Not available as of 5/22:

## Export data for triggered alerts {#alert-export-data}

You can export data for a triggered alert or data for the most recently triggered alert for an alert template as a [!DNL Microsoft Excel] workbook ([XLS](/help/search-social-commerce/glossary.md#w-x) file), a tab-separated values ([TSV](/help/search-social-commerce/glossary.md#s-t)) file, or a comma-separated values ([CSV](/help/search-social-commerce/glossary.md#c-d)) file. Downloadable reports are available for ten days after the alert is triggered and are then automatically deleted.

1. Do either of the following:

   * (To export data for the most recently triggered alert for an alert template) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL View Custom Alerts]**, which opens to the [!UICONTROL Alert Templates] tab.

   * (To export data for a specific triggered alert) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert"). Click **[!UICONTROL Triggered Alerts]**.

1. In the [!UICONTROL Export] column next to the template or report name, click the name of a format, and then open or save the file according to your browser's normal procedure:

   * **[!UICONTROL XLS]:** For an [!DNL Excel] workbook with a single worksheet (XLS). The report includes one worksheet, labeled at the top with the parameters, with one row for each included component when data for the component is available. Rows with no data are omitted. Basic reports include a total for each numeric column.

   * **[!UICONTROL TSV]:** For a TSV file. The report includes the parameters and one row for each included component.

   * **[!UICONTROL CSV]:** For a CSV file. The report includes the parameters and one row for each included component.

-->
