# Tier  2 - Tier 8 fields in shopping ad templates

**[!UICONTROL Tier  2 - Tier 8]:** (When you add tiers of product groups) A product attribute type by which to target products, and the qualifying criteria for the selected attribute type (for example, Brand=Acme or Condition=New). The values are applied hierarchically to determine the eligible products. Select an attribute type and enter the qualifying criteria. Prohibited characters include the following: `[ ] < > >>` (two consecutive "greater than" signs), which are used to designate column names in the template, modifier names in the template, and tier separators in the [!UICONTROL Parent Product Grouping] column in bulksheets.

You can include up to eight tiers (levels) of product groups, including "[!UICONTROL All Products]" (Tier 1). Each tier can include multiple product groups, but they must pertain to the same attribute type (such as "Condition").

>[!NOTE]
>
>* ([!DNL Google Ads] only) The possible values for [!UICONTROL Channel] are "[!UICONTROL Local]" or "[!UICONTROL Online]," and the possible values for [!UICONTROL ChannelExclusivity] are "[!UICONTROL SingleChannel]" and "[!UICONTROL MultiChannel]."
>* When you create a second tier (child) product group for an ad group from the [!UICONTROL Product Groups] tab in the [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] view, another product group, called "[!UICONTROL Everything Else]," is automatically created using the default ad group bid. Using inventory feed templates, however, "[!UICONTROL Everything Else]" product groups are excluded.
>* When you include multiple tiers, and no value is available for the final (highest-numbered) tier, then the next-highest tier is used as the biddable product group. For example, if you include five tiers, and no value is available for Tier 5, then Tier 4 is used as the biddable product group (unit). However, if no value is available for a middle tier, then the row is ignored. For example, if you include five tiers, and Tier 5 has a value but Tier 4 doesn't, then Row 4 is ignored.
