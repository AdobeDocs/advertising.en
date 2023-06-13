---
title: Generate a click-tracking URL
description: Learn how to manually generate a Search, Social, & Commerce click-tracking URL.
exl-id: d22a472a-a562-4812-a067-fbd407cd7d00
---
# Generate a Search, Social, & Commerce click-tracking URL using the Tracking URLs tool

*Advertisers with Adobe Advertising conversion tracking only*

For information about when you must manually generate and implement a click-tracking URL, see "[When and how to generate click-tracking URLs](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)."

>[!NOTE]
>
>This feature doesn't implement the tracking template or destination URL in the relevant ad account.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Tools] > [!UICONTROL Tracking URL]**.

1. Select the ad network account from the list.
   
   ([!DNL Google Ads] keywords; text, mobile app install, and dynamic search ads; placements; sitelinks; and product groups) Tracking tags for the tracking template field are displayed. They don't include any account-level append parameters. Skip to Step 4.
   
   For all other types of tags, input information to generate a tag.

1. (If necessary) Generate a tag:

   1. Specify the landing pages, with sitelinks or product names when requested, in one of the following ways:
      
      * Specify a file containing the information by entering the full path and file name or by clicking **[!UICONTROL Browse]** to locate the file on your device or network. The file must be a tab-delimited text file with one item per line in the following format:
      
        * (Creatives, Standard ads) `**landing_page**`
          
          where `landing_page` is a valid landing page URL or base URL.
          
          Example: http://www.example.com/travel.html
        
        * ([!DNL Microsoft® Advertising] sitelinks) `sitelink <tab> ** <tab> landing_page`
          
          where `sitelink` is the sitelink name and `landing_page` is a valid landing page URL or base URL.

          Example: `Careers <tab> ** <tab> http://www.example.com/careers.html`

          The file can include up to 10,000 lines.
         
        * ([!DNL Google Merchant Center] product groups and [Microsoft® Advertising] product ads) `product name <tab> ** <tab> landing_page`

          where `product name` is the product name and `landing_page` is a valid landing page URL or base URL.

          Example: `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

          The file can include up to 10,000 lines.

      * In the input field, enter one item per line in the following format:

        * (Creatives, Standard ads) `landing_page`

          where `landing_page` is a valid landing page URL or base URL.

          Example: http://www.example.com/travel.html

        * ([!DNL Microsoft® Advertising] sitelinks) `sitelink**landing_page`

          where `sitelink` is the sitelink name and `landing_page` is a valid landing page URL or base URL.

          Example: `Careers**http://www.example.com/careers.html`
      
        * ([!DNL Google Merchant Center] product groups and [!DNL Microsoft® Advertising] product ads) `product name**landing_page`

          where `product name` is the product name and `landing_page` is a valid landing page URL or base URL.

          Example: Acme PR208**http://www.example.com/travel.html

   1. Click **[!UICONTROL Generate Tracking URLs]**.

1. (Optional) Copy the URLs (beginning with "http" or "https") from the screen or output page and implement them in the search or social account.

For accounts with destination URLs, enter the values in the appropriate [!UICONTROL Base URL] fields.

For accounts with final URLs, enter the on-screen value in the appropriate [!UICONTROL Tracking Template] field. You must add a parameter for the final URL after the `&url=` parameter (such as `{lpurl}`). For [!DNL Yahoo! Japan Ads] accounts, use the parameter `{lpurl}`. For a list of [!DNL Google Ads] and [!DNL Microsoft® Advertising] parameters to indicate final URLs in tracking templates, see the [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348) (see the "Tracking template only" parameters in the section on "Available [!DNL ValueTrack] Parameters") and the [[!DNL Microsoft® Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [About the tools to create and decode tracking tags](tracking-tools-about.md)
>* [When and how to generate click-tracking URLs](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [Decode a Search, Social, & Commerce click-tracking URL](click-tracking-url-decode.md)
