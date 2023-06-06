---
title: Create a [!DNL Google Ads] customer match audience from an Adobe Campaign email list
description: Learn how to create a [!DNL Google Ads] customer match audience from an existing Adobe Campaign email list.
---
# Create a [!DNL Google Ads] customer match audience from an Adobe Campaign email list

*[!DNL Google Ads] accounts that are eligible for customer match only*

You can create a [!DNL Google Ads] customer match audience from an email list within Adobe Campaign by setting up an account link and a workflow in [!DNL Campaign].

To do so, you need access to your [!DNL Campaign] instance and an XML file containing the required workflow, which your Adobe Account Team will give you. Instructions may vary for different versions of [!DNL Campaign]. If necessary, your Adobe Account Team can help you set up the workflow in [!DNL Campaign].

1. Obtain credentials for an Advertising Search, Social, & Commerce-provided SFTP account.

1. In [!DNL Campaign], set up delivery of the email list to Advertising Search, Social, & Commerce:

   1. Create an [external account](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) to link your Search, Social, & Commerce-provided SFTP account:

      1. From the left menu, go to **\[Adobe Campaign v6\] > [!UICONTROL Platform] > [!UICONTROL External Accounts]**.

      1. Click ![Create Account](/help/search-social-commerce/assets/campaign-create-account.png "Create Account").

      1. Enter a label for the account and select **[!UICONTROL SFTP]** as the account type.

      1. Enter the URL and port number for the [!DNL Adobe] SFTP server and the advertiser's folder name, username, and password.

      1. Click **[!UICONTROL Save]**.

   1. In [!DNL Campaign Client], install the data package that includes the workflow required to send email data:

      1. From the menu bar, go to **[!UICONTROL Tools] > [!UICONTROL Advanced] > [!UICONTROL Import Package]**.

      1. Select **[!UICONTROL Install a package from a file]**, and then click **[!UICONTROL Next]**.

      1. Locate the data package file (`AMO_Workflow.xml`) on the device or network, and then click **[!UICONTROL Next]**.

      1. Click **[!UICONTROL Start]** and wait for the workflow to be installed.

   1. Edit the installed workflow to optionally edit the filters for the data query and to identify the new audience name and the external SFTP account:

      1. Go to **[!UICONTROL Administration] > [!UICONTROL Configuration] > [!UICONTROL Package management] > [!UICONTROL Installed packages]** and open the package.

      1. (Optional) Edit any of the filters for the data:

         * In the workflow, double-click the query activity (such as ForkTransition 1).

         * Edit the filter expressions.

         * Click **[!UICONTROL Finish]**.

      1. Name the segment:

         * In the workflow, double-click the activity **[!UICONTROL Data extraction (File)]**.

         * On to the **[!UICONTROL Data extraction (File)]** tab, in the **[!UICONTROL File name]** field, enter the segment name with the extension "`.added`" (such as PaidSubscribers.added).

            The segment name must not already exist. The segment name is case-sensitive, and it must consist of ASCII characters but can't include underscores (`_`).

            However, if you want to add the segment to a specific [!DNL Google Ad] account, then append the segment name with an underscore and the [!UICONTROL User SE Account ID] (Search, Social, & Commerce's ID for the [!DNL Google Ads] account, not the network's account ID):

            `_<User SE Account ID>`

            Example: Paid_Subscribers_1234.added

            >[!NOTE]
            >
            >This is an exception to the rule that prohibits underscores in the file name.

            Otherwise, the segment is added to all [!DNL Google Ads] accounts that Search, Social, & Commerce is syncing for the advertiser.

         * Leave the option to **[!UICONTROL Generate an outbound transition]** selected.

         * Click **[!UICONTROL Ok]**.

      1. Specify the external account to which to send the data:

         * In the workflow, double-click the activity **[!UICONTROL File Transfer]**.

         * On to the **[!UICONTROL File Transfer]** tab, in the **[!UICONTROL Remote server]** section, select the option to **[!UICONTROL Use an external account]**.

         * In the **[!UICONTROL External account]** field, select the label for the external account you created in Step 2.

         * In the **[!UICONTROL Server folder]** field, select the value for the [!UICONTROL Account] field for the external account.

         * (Optional) On the **[!UICONTROL Schedule]** tab, specify a different schedule for the file transfer.

            By default, the workflow is run at 00:00 (midnight), which ensures that all records are processed. To minimize latency, schedule the workflow to run no later than 18:00.

         * Click **[!UICONTROL Ok]**.

Search, Social, & Commerce checks the directory every 30 minutes (at NN:30 and NN:59 in the advertiser’s time zone) and moves any files it finds to another location, and then automatically creates an audience from the data and pushes it to Google at 22:00 (10 p.m.). Search, Social, & Commerce continues to check for updates (additions and subtractions) to the email list every 30 minutes and updates the audience on [!DNL Google Ads] accordingly at 22:00 daily.

>[!NOTE]
>
>* If you upload more than one version of a file between processing cycles, then the most recent file is used.
>
>* Search, Social, & Commerce doesn't store any of the customer data from your email lists used to create or edit a [!DNL Google Ads] audience.
>
>* [!DNL Google Ads] may take a while to process updates to an audience.
>
>* See [[!DNL Google Ads] documentation on how customer match works and limitations](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [About audiences](audience-about.md)
>* [Create [!DNL Google Ads] customer match audiences from [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [Manage customer match audiences using customer data lists](audience-from-customer-data-list.md)
>* [Manage dynamic remarketing audiences](audience-dynamic-remarketing-manage.md)
