---
title: Custom alert template settings
description: Learn about the settings for custom alert templates. 
---
# Custom alert template settings

| Tab | Parameter | Description |
|--- |--- |--- |
| [!UICONTROL Date Range] | [!UICONTROL Date] | The date range for which to evaluate the conditions for the alert. Metrics are evaluated in aggregate across the date range. The options range from *[!UICONTROL Yesterday]* to *[!UICONTROL Last 180 Days]*. |
| [!UICONTROL Filters] |  | The conditions for triggering the alert at the time specified on the [!UICONTROL Scheduling and Delivery] tab. The available columns vary by the entity type (such as campaign or keyword). All filters are joined using the Boolean function AND, which means that all specified conditions must be met.<ul><li><p>To add a filter, click ![Down arrow](/help/search-social-commerce/assets/arrow-down-expand.png "Down arrow") next to ![Add](/help/search-social-commerce/assets/add.png "Add") **[!UICONTROL ADD FILTER]**, and then do the following:</p></li><ol><li><p>(Optional) To filter the column names by text string, enter the search string in the **[!UICONTROL ADD FILTER]** input field.</p></li><li><p>Select a column name from the column menu.</p></li><li><p>Define the filter on the column:</p></li><ul><li><p>(Filters without input fields) Click ![Down arrow](/help/search-social-commerce/assets/arrow-down-expand.png "Down arrow") next to the second menu, and then select the check boxes next to each value to include.</p></li><li><p>(Metric columns for which you want to track increases or decreases in value between the specified date range and the previous period) For the operator, select *increases by* or *decreases by*, and then enter the threshold value.</p><p>For example, if you've selected the "[!UICONTROL Cost]" column and want to be alerted when any campaign's cost increases by 21%, then select "[!UICONTROL increases by]" and enter 21 in the input field. In the [!UICONTROL Date Comparison Format] field, indicate that you're interested in a change in percentage (rather than a change in currency units).</p><p>When you select this option, two additional columns are added for each regular data column. For example, instead of including just one column for "Clicks," the report includes columns for "Clicks R1"(for Range 1) "Clicks R2" (for Range 2), and either "Clicks Diff" or "ClicksDiff (%)," depending on the specified [!UICONTROL Date Comparison Format] (see below).</p><p>**Notes:**</p><ul><li><p>The difference column isn't populated for derived metrics.<p></li><li><p>This feature isn't available for property name, ID, or label classification columns.</p></li><li><p>Reports that compare large date ranges may take longer to generate.</p></li></ul></ul><li><p>(All other filters with input fields) Select an operator from the second menu, and then enter the applicable value.</p><p>For example, if you've selected the "Clicks" column and want to return only rows with more than 100 clicks, then select "greater than" and enter 100 in the input field.</p><p>Depending on the data type, available operators may include <i>greater than</i>, <i>less than</i>, <i>equals</i>, <i>contains</i>, <i>doesn't contain</i>, <i>starts with</i>, <i>ends with</i>, <i>no value</i>, <i>has value</i>, <i>before</i>, <i>after</i>, or <i>no date</i>.</p><p>**Note:** Text values aren't case-sensitive. For example, if you filter by campaigns with "loan" in the name, then the results could include "Consumer Loans" and "loan applications."</p></li></ol><li><p>To remove a filter, click ![Delete](/help/search-social-commerce/assets/delete.png "Delete") next to the filter definition.</p></li></ul> |
|  | [!UICONTROL Comparing] | (Available when the alert tracks increases or decreases in one or more metric columns; read-only) The two date ranges for which data is compared. |
|  | [!UICONTROL Date Comparison Format] | (Available when the alert tracks increases or decreases in one or more metric columns) How to express the difference between data in the two date ranges:<ul><li><p><i>[!UICONTROL Variance]</i> (the default) &mdash; Shows the difference as a numeric value.</p></li><li><p><i>[!UICONTROL % Change]</i> &mdash; Shows the difference as a percentage.</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Name] | The alert name. It must include at least five characters. |
|  | [!UICONTROL Trigger this Alert] [when] | How often the alert checks for the specified condition filters and, when all conditions are met, sends email notifications:<ul><li><p>[!UICONTROL Daily at <*NN*> [AM|PM]]</p></li><li><p>[!UICONTROL Weekly on <*Day of Week*> at <*NN*> [AM|PM]]</p></li><li><p>[!UICONTROL Every month on <*Day NN*> at <*NN*> [AM|PM]]</p></li></ul>**Note:** This value doesn't affect the evaluation period. |
|  | [!UICONTROL Email Recipients] | (Editable only by the creator of the alert template; read-only for everyone else) Email addresses at which to send notifications when an alert is generated. By default, the address for the template creator is entered.<br><br>To add an address, enter the address, and then click **[!UICONTROL Add]**. To specify multiple addresses, separate them with commas or spaces, or add them separately.<br><br>When the alert includes up to 1000 records, a CSV version of the alert is attached to the email message. |

>[!MORELIKETHIS]
>
>* [About custom alerts](alert-about.md)
>* [Create a custom alert template](alert-template-create.md)
>* [Edit a custom alert template](alert-template-edit.md)
>* [Pause a custom alert template](alert-template-pause.md)
>* [Activate a custom alert template](alert-template-activate.md)
>* [Delete a custom alert template](alert-template-delete.md)
>* [View custom alerts](alert-view.md)
>* [Export data for custom alerts](alert-export-data.md)