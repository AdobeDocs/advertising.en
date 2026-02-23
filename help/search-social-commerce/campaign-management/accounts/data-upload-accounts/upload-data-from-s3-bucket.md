---
title: "Upload account data to an [!DNL Amazon] [!DNL S3] bucket"
description: Learn how to upload account data to an [!DNL Amazon] [!DNL S3] bucket for reporting and simulation support.
---
# Upload account data to an [!DNL Amazon] [!DNL S3] bucket

You can populate an account with campaign content and cost, click, and conversion data by uploading the data to a Search, Social, & Commerce-assigned folder in an [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3]) bucket.

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

1. Contact your Adobe Account Team to enable account data uploads <!-- naming for BYOI feature? --> for your Search, Social, & Commerce advertiser account.

   The team will facilitate the creation of an organization-specific folder in an [!DNL S3] bucket, and they'll let you know when it's completed.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->

1. Retrieve the [!DNL S3] cloud storage path, access key ID, and secret access key for your account.
   
   The same access key ID and secret access key are used for all of the organization's data-upload <!-- naming convention?--> accounts.

   1. In the main menu, click **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. In the submenu, click **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.
   
   1. Hold the cursor over the account name, click ![More](/help/search-social-commerce/assets/more-filters.png "More"), and then select **[!UICONTROL Upload]**.
   
   1. In the [!UICONTROL Cloud Storage Link] box, click **[!UICONTROL Go to the Link]**.

   1. Click **[!UICONTROL Show Access Key and Secret]**.
   
   1. Next to the [!UICONTROL Storage Link] field, click **[!UICONTROL Copy]** to copy the link to your clipboard, and store the link in a secure place.

   1. Similarly, copy and securely store the [!UICONTROL Access Key] and the [!UICONTROL Secret Key] values.

   1. Click **[!UICONTROL Done]**.

1. (Once per organization) Set up your local AWS environment:

   1. Download and install [!DNL AWS Command Line Interface] (AWS CLI), from the following location: [https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).

   1. Configure your AWS credentials:

      1. Create a plaintext file and name it `~/.aws/credentials` (without a file extension).
      
      1. Open the file in any text editor and enter the organization's access key ID and secret access key as follows:
      
         ```
         [default]
         aws_access_key_id = <Access key copied in Step 2>
         aws_secret_access_key = <Secret key copied in Step 2>
         ```

1. Download your account data report from the ad network and save it.

1. In AWS CLI, run the following command to upload your account data to your [!DNL S3] cloud location.

   ```
   aws s3 cp <local-report-file-location <S3-cloud-location-associated-with-your-account>
   ```

   Example:  `aws s3 cp filename.txt s3://cloud-location/`

You can track the progress of the upload job using the [[!UICONTROL Upload Logs] feature](download-upload-log.md). <!-- Anything else to note? -->
