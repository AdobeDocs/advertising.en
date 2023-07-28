---
title: Apply data filters from the toolbar
description: Learn how to filter the page data from the toolbar.
exl-id: 922cc148-e6dc-428b-a7f3-1da3780df326
feature: Search Common Tasks, Search Custom Data Views
---
# Apply data filters from the toolbar

You can apply as many filters as you want to a view. All filters are joined using the AND operator.

1. In the toolbar, click ![Filter](/help/search-social-commerce/assets/filter.png "Filter").

1. In the filter settings, do any of the following:

   * To add a filter, click ![Add Filter](/help/search-social-commerce/assets/add.png "Add Filter") **[!UICONTROL ADD FILTER]**, and then do the following:

     1. (Optional) To filter the column names by text string, enter the search string in the **[!UICONTROL ADD FILTER]** input field.

     1. Select a column name from the column menu.

     1. Define the filter on the column:

        * (Filters without input fields) Click ![Down arrow](/help/search-social-commerce/assets/arrow-down-expand.png "Down arrow") next to the second menu, and then select the check boxes next to each value to include.

        * (Filters with input fields) Select an operator from the second menu, and then enter the applicable value.
   
          For example, if you've selected the "[!UICONTROL Clicks]" column and want to return only rows with more than 100 clicks, then select *[!UICONTROL greater than]*" and enter `100` in the input field.
          
          Depending on the data type, available operators may include *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]*, or *[!UICONTROL no date].* 
          
          **Note:** Text values aren't case-sensitive. For example, if you filter by campaigns with "loan" in the name, then the results will include "Consumer Loans" and "loan applications."

        * ([!UICONTROL Ad Groups], [!UICONTROL Keywords], [!UICONTROL Product Groups], [!UICONTROL Placements], and [!UICONTROL Auto Targets] views only; optional) Change the setting to "[!UICONTROL Include rows with performance data only]." 
        
          **Warning:** If you de-select the option and the view includes many entities without performance data, then the data takes longer to be displayed.

   * To edit an existing filter, click the filter, change the filter definition, and then click ![Update Filter](/help/search-social-commerce/assets/select.png "Update Filter").

   * To remove an existing filter, click **[!UICONTROL X]** next to the filter definition.

1. Click **[!UICONTROL Apply]**.
