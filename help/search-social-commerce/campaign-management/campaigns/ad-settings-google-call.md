---
title: '[!DNL Google Ads] call-only ad settings'
description: Reference the settings for [!DNL Google Ads] call-only ads.
exl-id: 10672771-53fd-4ce9-9d67-6b1f8f5a41b8
feature: Search Campaign Management
---
# [!DNL Google Ads] call-only ad settings

You can create call-only text ads for campaigns that use the search network.

Search, Social, & Commerce tracks call-only ads using the account-level landing page suffix and tracking template, but you can optionally override the account-level tracking at the ad level within [!DNL Google Ads] Manager.

See the [!DNL Google Ads] help for [ad limits per account](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** The name of the business. The maximum length is 25 characters or 12 double-byte characters.

**[!UICONTROL Country]:** (Optional) The country in which the business is located.

**[!UICONTROL Phone Number]:** The telephone number for the business. Examples: (124) 123-4567, 12345678901, +441234567890.

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** The first and second lines of the body of the ad. The maximum length for each line is 35 characters or 17 double-byte characters.

Keyword substitution syntax doesn't count towards the maximum length. For example, "`{Description1: Free Account Analysis!}`" is treated as 22 characters (only the portion "Free Account Analysis\!").

>[!NOTE]
>
>The description fields can't include telephone numbers.

**[!UICONTROL Display URL]:** The URL displayed in the ad. The display URL must match a domain that's associated with your business, but the ad doesn't send people to a landing page.

The maximum length is 35 single-byte or 17 double-byte characters. Keyword substitution syntax doesn't count towards the maximum length. For example, "`{DisplayURL: example.com}`" is treated as 11 characters (only the portion "example.com").

**[!UICONTROL Verification URL]:** (Optional) A webpage on which the phone number for your ad appears as text, so that [!DNL Google Ads] can verify that the phone number is valid. It must have the same domain as the ad's display URL.

**[!UICONTROL Is Tracked]:** Enables call tracking and call-only conversions.

**[!UICONTROL Count calls as phone call conversions]:** (When "[!UICONTROL Is Tracked]" is selected; optional) Attributes all calls that result from the ad to a specific type of phone call conversion, when one is specified. Otherwise, [!DNL Google Ads] creates a default conversion action called "[!UICONTROL Calls from ads]" once it records at least one conversion from your forwarding numbers, and then attributes calls to it.

**[!UICONTROL Count Action]:** (When "[!UICONTROL Count calls as phone call conversions]" is selected; optional)  The existing conversion action to which calls are attributed.

You can create and manage conversion actions within [!DNL Google Ads].

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}
 
>[!MORELIKETHIS]
>
>* [About ads](ad-about.md)
>* [Manage ads](ad-manage.md)
>* [[!DNL Google Ads] expanded dynamic search ad settings](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] responsive search ad settings](ad-settings-google-rsa.md)
