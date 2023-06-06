# Tracking Type field in account and campaign settings

**[!UICONTROL Tracking Type]:** The method by which URLs are generated:

* *[!UICONTROL EF Redirect]* (the default): For clients who want to use the Adobe Advertising conversion tracking service. This method generates unique click-tracking IDs and redirects users to the Adobe Advertising server for tracking purposes before sending them to the client's landing page.

  This method has default tracking options that you optionally can customize, and you also can specify parameters to append to each URL.

* *[!UICONTROL No EF Redirect]:* For clients who want to use only their own click-tracking codes. Search, Social, & Commerce doesn't provide click-tracking IDs or redirect codes. For accounts with destination URLs, each destination URL is the same as the base URL.

  **Notes:**

  * Only agency account manager, Adobe account manager, and administrator users can change this value.
  * If you change the tracking method, you must regenerate tracking URLs for the account.
  * Campaign-level tracking options override account-level settings.
