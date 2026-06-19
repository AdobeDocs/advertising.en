---
title: About click-tracking URL formats for the Adobe Advertising conversion tracking service
description: Learn about the click-tracking formats for supported ad networks.
exl-id: b6f225d5-2268-4b2a-9927-063155ba0dc5
feature: Search Tracking
TQID: https://experienceleague.adobe.com/pVSEKmf45CqsfXMbj8HGDltdgV3wUV2UsAzP94vkijg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# About click-tracking URL formats for the Adobe Advertising conversion tracking service

The tracking templates, landing page suffixes (final URL suffixes), and destination URLs for ad accounts and campaigns that use the Adobe Advertising conversion tracking service have the following format:

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

where:

* `http://pixel.everesttech.net` redirects the user to the Adobe Advertising pixel servers.

* `<advertiser_ID>` is a variable for the unique user ID assigned to the advertiser within Adobe Advertising.

* `<token passing parameter>` is a variable for one of the following:

  * `cq?` or `rq` denotes token passing is enabled.

  * `c?` or `r` denotes token passing is disabled.

* `<ad network ID>` is a variable for the numeric ID for the specified ad network, such as *3* for [!DNL Google Ads], *10* for [!DNL Microsoft Advertising], *45* for [!DNL Meta], *86* for [!DNL Yahoo DSP], *87* for [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL LY Ads] (formerly [!DNL Yahoo! Japan Ads]), *105* for [!DNL Yahoo Native] (deprecated), or *106* for [!DNL Pinterest] (deprecated).

* `<tracking ID>` is a variable for a system-generated tracking ID string that identifies a keyword, ad, or placement that is unique in the account. The string varies by ad network.

* `<the landing page>` is a variable that represents the URL on your site to which end users are directed. For accounts with destination URLs, this value is an URL. For accounts with tracking templates, this value is a parameter (such as `{lpurl}`) that represents the final URL. 

See the separate pages indicating the [[!DNL Baidu] formats](formats-click-tracking-baidu.md), [[!DNL Google Ads] formats](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] formats](formats-click-tracking-microsoft.md), [[!DNL Naver] formats](formats-click-tracking-naver.md), [[!DNL Yahoo DSP] formats](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] formats](formats-click-tracking-yahoo-japan.md), and [[!DNL Yandex] formats](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [Click-tracking formats for sponsored ads on [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [Click-tracking formats for [!DNL Google Ads]](formats-click-tracking-google.md)
>* [Click-tracking formats for sponsored ads on [!DNL LY Ads]](formats-click-tracking-yahoo-japan.md)
>* [Click-tracking formats for [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [Click-tracking formats for sponsored ads on [!DNL Naver]](formats-click-tracking-naver.md)
>* [Click-tracking formats for sponsored ads on [!DNL Yahoo DSP]](formats-click-tracking-yahoo-display-network.md)
>* [Click-tracking formats for sponsored ads on [!DNL Yandex]](formats-click-tracking-yandex.md)
