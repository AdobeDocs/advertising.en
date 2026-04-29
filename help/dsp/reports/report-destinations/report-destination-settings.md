---
title: Report destination settings
description: See the details required for your report destinations, by destination type.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
TQID: https://experienceleague.adobe.com/VB5UY9vm147LQJMKKyGOlhZdNcq6mVDYTT0Ef4RcwVs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
subfeature_v2:
  - id: cc3b7f3c-58f0-4ba4-b808-391002930fd4
    internal-label: DSP Custom Reports
  - id: e8b92199-d82f-4b20-9fc3-ffe694f93ce5
    internal-label: DSP Planner
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Report destination settings

The details required for non-email report destinations vary by destination type.

>[!NOTE]
>
> You can also deliver your custom reports to email recipients, which don't require a saved report destination. You can specify email recipients, instead of saved destinations, within the report settings.

## [!UICONTROL S3]

**[!UICONTROL Name]:** A name to help you identify the destination.

**[!UICONTROL S3 Bucket URL]:** The full path to the folder on the [!DNL Amazon Simple Storage Service] (S3) bucket to which the report is uploaded. Example: `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** The Access Key ID to the ([!DNL Amazon S3]) bucket (provided by [!DNL Amazon]).

**[!UICONTROL Secret Access Key]:** The Secret Access Key to the ([!DNL Amazon S3]) bucket (provided by [!DNL Amazon]).

## [!UICONTROL FTP]

**[!UICONTROL Name]:** A name to help you identify the destination.

**[!UICONTROL Server]:** The host name for the server.

**[!UICONTROL Port]:** The port number to use on the server. The default is *[!UICONTROL 21]*.

**[!UICONTROL Username]:** The user name to sign in to the server.

**[!UICONTROL Password]:** The password to sign in to the server.

**[!UICONTROL Path (Optional)]:** The server path to which the files are uploaded.

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** A name to help you identify the destination.

**[!UICONTROL Server]:** The host name for the server. 

**[!UICONTROL Port]:** The port number to use on the server. The default is *[!UICONTROL 21]*.

**[!UICONTROL Username]:** The user name to sign in to the server.

**[!UICONTROL Password]:** The password to sign in to the server.

**[!UICONTROL Path (Optional)]:** The server path to which the files are uploaded.

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** A name to help you identify the destination.

**[!UICONTROL Server]:** The host name for the server.

**[!UICONTROL Port]:** The port number to use on the server. The default is *[!UICONTROL 21]*.

**[!UICONTROL Username]:** The user name to sign in to the server.

**[!UICONTROL Password]:** The password to sign in to the server.

**[!UICONTROL Path (Optional)]:** The server path to which the files are uploaded.

>[!MORELIKETHIS]
>
>* [About report destinations](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Create a report destination](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Edit a [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Delete a report destination](/help/dsp/reports/report-destinations/report-destination-delete.md)
