---
title: Manage shared sitelinks
description: Learn how to create and manage shared sitelink extensions.
---
# Manage shared sitelinks

*[!DNL Google Ads] and [!DNL Microsoft Advertising] only*

Create and manage account-level shared sitelinks for any synchronized [!DNL Google Ads] or [!DNL Microsoft Advertising] account from the [!UICONTROL Extensions] > [!UICONTROL Sitelinks] library. 

## Create a shared sitelink

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Extensions] > [!UICONTROL Sitelinks]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network and the account name, and then click **[!UICONTROL Continue]**.

1. Enter the [shared sitelink settings](#shared-sitelink-settings).

1. Click **[!UICONTROL Post]**.

Once you create a sitelink, you can [assign it to an account, campaign, or ad group](sitelink-extension-associate.md).

## Edit shared sitelink settings

You can edit one shared sitelink at a time.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Extensions] > [!UICONTROL Sitelinks]**.

1. Select the check box next to the sitelink to edit.

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Edit the [shared sitelink settings](#shared-sitelink-settings).

1. Click **[!UICONTROL Post]**.

## Delete shared sitelinks

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Extensions] > [!UICONTROL Sitelinks]**.

1. Select the check box next to each shared sitelink that you want to delete.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar, click ![More](/help/search-social-commerce/assets/more.png "More") and select **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Delete]**.

## Shared sitelink settings {#shared-sitelink-settings}

For additional policies and reasons for sitelink disapproval, see the [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) and [[!DNL Microsoft Advertising]](https://about.ads.microsoft.com/en-us/resources/policies/ad-extensions-policies) sitelink extension requirements.

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** The text to appear for the link. It can include up to 25 single-byte or 12 double-byte characters. The link text must be unique within the account or campaign.

>[!NOTE]
>
>([!DNL Google Ads]) Existing text of 35 characters is displayed in ads on desktops and tablets but not on mobile devices.

**[!UICONTROL Status]:** The display status of the sitelink:  *[!UICONTROL Active]* or *[!UICONTROL Deleted]* (existing sitelinks only). The default for new sitelinks is *[!UICONTROL Active]*.
 
**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Extra text that the search engine may display under the link text. To include a description, enter values for both description fields. Each description field can include up to 35 single-byte or 17 double-byte characters.

**[!UICONTROL Start Date]:** (Campaigns with existing legacy sitelinks or no sitelinks only; optional) The first date on which the sitelink may be displayed with ads in the campaign. The default for new sitelinks is the current day. To specify a future start date, enter a date in the format MM/DD/YYYY or M/D/YYYY, or click   and select a date.

**[!UICONTROL End Date]:** (Optional) The last date on which the sitelink may be displayed with ads in the campaign. By default, the sitelink may be displayed indefinitely. To specify an end date, enter a date in the format MM/DD/YYYY or M/D/YYYY, or click   and select a date.

**[!UICONTROL Mobile Preference]:** (Optional) Allows the network to try to display the ad extension to mobile device users rather than desktop or tablet users. By default, the option isn't enabled, and the ad extension appears on any device type.

>[!NOTE]
>
>The network doesn't guarantee that it will display the ad extension on the preferred device type.

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** The landing page URL to which search engine users are taken when they click your ad. Include any parameters that determine the content of the page. If you enter a value, it overrides the base URL for the ad.

Once you save the record, the base URL includes any append parameters configured for the campaign or account. 

>[!NOTE]
>
>* (Accounts with final URLs) The base URL may contain redirects within the landing page domain or subdomain but no redirects outside the landing page domain. The ad network extracts the domain from this URL, and adds any optional display paths for the ad, to create the display URL for the ad.
>* ([!DNL Google Ads]) Each sitelink in a campaign or ad group must have a unique landing page, and the content for each sitelink landing page must have approximately 80% unique content. For example, you can't have sitelinks with links to multiple anchors within the same page.
>* ([!DNL Google Ads]) Avoid using macros, which aren't substituted for clicks from sources that enable parallel tracking. If the advertiser must use macros, then the Adobe Account Team should work with Customer Support or the implementation team to add them.

**[!UICONTROL Tracking Template]:** (Optional) The tracking template or tracking URL, which specifies all off-landing domain redirects and tracking parameters and also embeds the final/landing page URL in a parameter. Example: `{lpurl}?source={network}&id=5` or `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` to include a redirect.

* For Adobe Advertising conversion tracking, which is applied when the campaign settings include "EF Redirect" and "Auto Upload," Search, Social, & Commerce automatically prefixes its own click-tracking code when you save the record.

* For supported parameters to embed the final URL, see the ([!DNL Microsoft Advertising] only) [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) or ([!DNL Google Ads] only) the "Tracking template only" parameters in the section on "Available ValueTrack Parameters" in the [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).
   
* You can optionally include URL parameters and any custom parameters defined for the campaign, separated by ampersands (&), such as `{lpurl}?matchtype={matchtype}&device={device}`.

* You can optionally add third-party redirects and tracking.

>[!NOTE]
>
>* When the campaign settings include "[!UICONTROL EF Redirect]" and "[!UICONTROL Auto Upload]," Search, Social, & Commerce automatically prefixes its own redirect and tracking code when you save the record.
>* The tracking template at the most granular level overrides the values at all higher levels. For example, if both the account settings and the keyword settings include a value, the keyword value is applied.
>* ([!DNL Google Ads]) If you update a tracking template at the  sitelink, or keyword level, then the relevant ads are resubmitted for review. You can update your tracking templates at the account, campaign, or ad group levels without resubmitting your ads for approval.
>* ([!DNL Microsoft Advertising]) You can update your tracking templates at any level without resubmitting your ads for approval.
>* For [!DNL Google Ads], avoid using macros, which aren't substituted for clicks from sources that enable parallel tracking. If the advertiser must use macros, the Adobe Account Team should work with Customer Support or the implementation team to add them.

>[!MORELIKETHIS]
>
>* [About sitelink extensions](sitelink-extension-about.md)
>* [Associate shared sitelinks with accounts, campaigns, and ad groups](sitelink-extension-associate.md)
