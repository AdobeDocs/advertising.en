# Redirect Type field in account and campaign settings

**[!UICONTROL Redirect Type]:** (For [!UICONTROL EF Redirect] only) The method of redirecting end users to the final URL or destination URL. The selected option is applicable to all ads, keywords, and placements in the account or campaign. The default account-level setting is inherited from the advertiser's tracking settings, and the default campaign-level setting is inherited from the account settings.

* *[!UICONTROL Standard]:* To just redirect the end user to the specified URL.

* *[!UICONTROL Token]:* To redirect the end user to the URL and also record the Search, Social, & Commerce ID for the click (`ef_id`) as a query string parameter, which is used as a token. Choose this option if you will report offline transactions, want Search, Social, & Commerce to exchange data with Adobe Analytics, or want to track all conversions that occur within [!DNL Apple Safari] browsers.

**Notes:**

* If you switch from [!UICONTROL Standard] to [!UICONTROL Token], or vice versa, then you must regenerate tracking URLs for the account.
* You can override the account-level setting at the campaign level.
