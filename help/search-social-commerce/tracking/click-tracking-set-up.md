---
title: Set up cookie-based click tracking
description: Learn how to set up and validate click-tracking tags.
exl-id: 340aec08-a1a5-4aa5-b666-9c819c1709d0
---
# Set up cookie-based click tracking

For Search, Social, & Commerce to track clicks, the following elements must be configured and validated.

1. (Adobe Account Team) Set up the advertiser as a pixel customer.

1. [Specify the correct tracking options for each of the advertiser's ad network accounts and campaigns](#set-up-click-tracking-options).

1. If necessary, [generate tracking URLs and upload them](#generate-upload-tracking-urls) for some campaign elements.

1. [Validate the format of a few of the click tracking URLs, and test them to validate that the correct landing page opens](#validate-tracking-urls).

## Set up tracking options for ad network accounts and campaigns {#set-up-click-tracking-options}

*Agency account manager, [!DNL Adobe] account manager, and administrator user roles only*

1. For each ad network account, do the following:

   1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Accounts]**.
   
   1. Hold the cursor over the account name, click ![Menu icon](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menu icon"), and then select **[!UICONTROL Edit]**.
   
   1. Click **[!UICONTROL Set Account Tracking]**.
   
   1. For the [!UICONTROL Tracking Type] setting, select **[!UICONTROL EF Redirect]**.
   
   1. (To allow Search, Social, & Commerce to exchange data with Adobe Analytics or to track conversions that occur in [!DNL Apple Safari]) Select the [!UICONTROL Redirect Type] option **[!UICONTROL Token]**.
   
   1. (Optional) Turn on the **[!UICONTROL Auto Upload]** option to automatically upload new tracking URLs to the ad network the next time that Search, Social, & Commerce synchronizes with it. This value is inherited as the default for all of the campaigns in the account but can be overridden at the campaign level.

1. For each campaign, do the following:

   1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Campaigns]**.
   
   1. Hold the cursor over the campaign name, click ![Menu icon](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menu icon"), and then select **[!UICONTROL Edit]**.
   
   1. Click **[!UICONTROL Set Campaign Tracking]**. Then select the option to **[!UICONTROL Override Account Tracking]**.
   
   1. For the [!UICONTROL Tracking Type] setting, select **[!UICONTROL EF Redirect]**.
   
   1. (To allow Search, Social, & Commerce to exchange data with Adobe Analytics or to track conversions that occur in [!DNL Apple Safari]) Select the [!UICONTROL Redirect Type] option **[!UICONTROL Token]**.
   
   1. (Optional) Turn on the **[!UICONTROL Auto Upload]** option to automatically upload new tracking URLs to the ad network the next time that Search, Social, & Commerce synchronizes with it. This value is inherited as the default for all of the campaigns in the account but can be overridden at the campaign level.

## Generate and upload tracking URLs {#generate-upload-tracking-urls}

See "[When and how to generate click-tracking URLs](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)."

### Test the format of click-tracking URLs {#validate-tracking-urls}

Validate that the correct landing page opens for the click-tracking URL.

1. Mimic an ad click by sending traffic to the advertiser's staging environment:

   1. In a text editor, paste a click-tracking URL, change the landing page URL to point to the same page within the advertiser's staging environment, and then paste the new URL in your browser's address bar and press the **[!DNL Enter]** key.
   
   1. Look for the cookie in your browser's stored cookies.
   
   1. Complete a transaction on the staging site, and verify that the success page fires the correct pixel. The actual parameters tracked by the pixel vary by advertiser and tracking URL. In the following example, the advertiser wants to track the number of new applications and the amount of new revenue:
   
      For a new end user (with a fresh cookie), the following pixel should be fired:
      
      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`
      
      If the cookie isn't fresh, then the following pixel should be fired:
      
      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


  1. Repeat for several click tracking URLs in the domain.

1. Repeat Step 1 for each domain, using a different landing page accordingly.

1. If required, confirm that Search, Social, & Commerce can see the pixels for the transactions IDs (`ev_transid`) generated during testing.

>[!MORELIKETHIS]
>
>* [When and how to generate click-tracking URLs](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
