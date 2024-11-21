---
title: Upload offline conversion data for enhanced conversions
description: Learn how to upload first-party, offline conversion data to map to [!DNL Google Ads] enhanced conversions for leads and [!DNL Microsoft Advertising] enhanced conversions.
feature: Conversions
exl-id: 5c5dfbb8-3b17-4973-8012-fc7f0e97e33b
---
# Upload offline conversion data for enhanced conversions

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts only*

You can upload your first-party, offline conversion data &mdash; including hashed email addresses and telephone numbers &mdash; to map to your existing [[!DNL Google Ads] enhanced conversions for leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) and [[!DNL Microsoft Advertising] enhanced conversions](https://help.ads.microsoft.com/#apex/ads/en/60178). All uploaded data is synced in real-time to the ad network.

## Upload data for enhanced conversions

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions]**, and then click the **[!UICONTROL Upload]** tab.

1. Select the ad network, and then the account.

1. (Optional) To download a template with all [required data fields](#enhanced-conversions-leads-data) in [!DNL Microsoft Excel] format, click **[!UICONTROL View Template]**, and then download the file according to your browser's normal procedure.

   You can edit the file to include your data and save your changes, and then upload the file in the next step.

1. Click **[!UICONTROL Choose File]**, and then select a file to upload from your device or network.

## Required data for uploaded files {#enhanced-conversions-leads-data}

### Data above the table

`Parameters:TimeZone=insert_timezone`

Enter the account's time zone either in this location or in the "[!UICONTROL Conversion Time]" column for each row. Use either a\) ([!DNL Google Ads only]) the [supported time zone ID format](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) or b\) the GMT offset, as indicated by + or - and the 4-digit time difference (such as -0500 for New York, +0100 for Berlin, or +0000 for Greenwich Mean Time).

### Table columns and values for [!DNL Google Ads]

| Column | Description |
| ------ | ----------- |
| Email | The user's email address, which must be hashed using the SHA-256 algorithm. Each row must include either an Email value or a Phone Number value. |
| Phone Number | The user's telephone number, which must be hashed using the SHA-256 algorithm. It must include a country code, and it may contain dashes and other symbols. Each row must include either an Email value or a Phone Number value. |
| Conversion Name | (Required) The name of the conversion action. |
| Conversion Time | (Required) The time the conversion event occurred in a [supported time format](https://support.google.com/google-ads/answer/7014069#prepare_data). If you don't include the account's time zone ID in the `Parameters:TimeZone=insert_timezone` line above the data table, then include the time zone for each row using either a\) the [supported time zone ID format](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) or b\) the GMT offset, as indicated by + or - and the 4-digit time difference (such as -0500 for New York, +0100 for Berlin, or +0000 for Greenwich Mean Time).|
| Conversion Value | (Required) The numeric conversion value. |
| Conversion Currency | The currency code for the conversion event. |
| Ad User Data | (Applicable for data pertaining to users in the European Economic Area (EEA) or United Kingdom (UK)) Indicates if user consent was given for sending user data to [!DNL Google] for ad personalization purposes. Values may include `Granted`, `Denied`, or \[null\] (which is sent to [!DNL Google Ads] as `Unspecified`). **Note:** [!DNL Google Ads] doesn't currently enforce consent for enhanced conversions for leads, but it may do so in the future. |
| Ad Personalization | (Applicable for data pertaining to users in the European Economic Area (EEA) or United Kingdom (UK)) Indicates if user consent was given for sending user data to [!DNL Google] for advertising purposes. Values may include `Granted`, `Denied`, or \[null\] (which is sent to [!DNL Google Ads] as `Unspecified`). **Note:** [!DNL Google Ads] doesn't currently enforce consent for enhanced conversions for leads, but it may do so in the future. |

### Table columns and values for [!DNL Microsoft Advertising]

For more instructions for using the template, see [https://help.ads.microsoft.com/#apex/3/56852](https://help.ads.microsoft.com/#apex/3/56852).

| Column | Description |
| ------ | ----------- |
| Conversion Name | (Required) The name of the conversion action. |
| Conversion Time | (Required) The time the conversion event occurred. If you don't include the account's time zone ID in the `Parameters:TimeZone=insert_timezone` line above the data table, then include the time zone for each row using the GMT offset, as indicated by + or - and the 4-digit time difference (such as -0500 for New York, +0100 for Berlin, or +0000 for Greenwich Mean Time). For a list of time zones for various cities, see [https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones), but make sure that you use the format specified here instead of the format in the time zone list. |
| Conversion Value | (Required) The numeric conversion value. |
| Conversion Currency | The currency code for the conversion event. |
| Microsoft Click ID | The associated unique [!DNL Microsoft] click identifier (MSCLKID). This field may be empty for enhanced offline conversions. |
| Hashed Email Address | The user's email address, which must be hashed using the SHA-256 algorithm. For enhanced offline conversions, each row must include either a Hashed Email Address value or a Hashed Phone Number value. |
| Hashed Phone Number | The user's telephone number, which must be hashed using the SHA-256 algorithm. It must include a country code, and it may contain dashes and other symbols. For enhanced offline conversions, each row must include either a Hashed Email Address value or a Hashed Phone Number value. |

>[!MORELIKETHIS]
>
>* [Create a conversion action for a [!DNL Google Ads] enhanced conversion for leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Implement [!DNL Google Ads] enhanced conversions for leads](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Implement [!DNL Microsoft Advertising] enhanced offline conversions](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
