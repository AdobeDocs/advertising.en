---
title: Reauthenticate a [!DNL Google Analytics] data source
description: Learn how to reauthenticate a [!DNL Google Analytics] data source if you change the associated password or the certificate expires.
role: User, Admin
exl-id: 9233e004-8607-444a-ba99-f63cb83a8b7a
---
# Reauthenticate a [!DNL Google Analytics] data source

*Agency Administrators, Agency Account Managers, Adobe Account Managers, and Administrators Only*

If you change the password for the email account used for a data source, or if the [!DNL OAuth] certificate for the account expires, then all open connections to the email account are closed, and you must reauthenticate to resume syncing data.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Data Source Setup]**.

1. Select the check box next to the data source that you want to reauthenticate.

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Edit the [data source settings](data-source-settings.md):

    1. In the [!UICONTROL Connect to Google Analytics] section, do the following.

       1. (If necessary) Enter a new email address to use to access data for this data source. The email address must be registered to a [!DNL Google] account and have "Read & Analyze" permissions for the [!DNL Google Analytics] account. See the [instructions for assigning user permissions in [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).
       
          >[!TIP]
          >
          >To make sure that only specific [!DNL Google Analytics] properties and views are available within Search, Social, & Commerce, log in using an email address that has access to only those properties and views.
       
      1. Select the check box to authorize Search, Social, & Commerce to access metrics for the account.
     
      1. Click **[!UICONTROL Re-Authenticate]**.

1. Click **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [About syncing [!DNL Google Analytics] conversion metrics](data-source-about.md)
>* [Prerequisites for configuring a [!DNL Google Analytics] data source](data-source-prerequisites.md)
>* [Configure a [!DNL Google Analytics] view as a data source](data-source-configure.md)
>* [Edit a [!DNL Google Analytics] data source](data-source-edit.md)
>* [Pause syncing of a data source](data-source-pause.md)
>* [[!DNL Google Analytics] data source settings](data-source-settings.md)
>* [Appendix - Available [!DNL Google Analytics] metrics](data-source-ga-metrics.md)
