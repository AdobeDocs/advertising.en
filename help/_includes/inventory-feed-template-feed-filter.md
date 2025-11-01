# Text ad template - Feed Filter

**\[Feed Filter\]:** Which rows in the feed file to propagate:

* *[!UICONTROL Propagate all rows found in feed:]* (The default) To propagate data for all rows.

* *[!UICONTROL Propagate rows that meet certain conditions:]* To propagate data for only rows that meet up to ten specified conditions. Specify the filters to apply:

  1. Select the Boolean operation to use for all filters:  **[!UICONTROL AND]** or **[!UICONTROL OR]**.
  
  1. Select a column name from the first menu, select an operator from the second menu, and then either enter the applicable values or leave the input field blank to propagate data for rows without conditions.
  
    The column list includes all available columns in the feed.
    
    Available operators include *[!UICONTROL contains]*, *[!UICONTROL does not contain]*, *[!UICONTROL =]*, *[!UICONTROL <>]* (isn't equal to), *[!UICONTROL in]*, *[!UICONTROL not in]*, *[!UICONTROL less than]*, and *[!UICONTROL greater than]*. When you select the operator "[!UICONTROL in]," you can enter a comma-separated list of values; if a record matches any of the specified values, then data is propagated for those rows. For all other operators, enter only one value. Values aren't case-sensitive.
    
    For example, if you select the "product_type" column and want to return only rows for product names containing "shoes," then select "**[!UICONTROL contains]**" and enter `shoes` in the input field.
    
  1. (To apply up to nine additional filters) For each additional filter, click **[!UICONTROL Add Condition]**, and then specify the additional filter per Step 2.
