---
title: (New UI) Manage notifications
description: Learn how to view, configure, and manage Search, Social, & Commerce notifications, including push notifications and the Notification Center web application.
feature: Search Notifications
---
# (New UI) Manage notifications

*Beta feature*

You can configure your notification settings to subscribe to, or unsubscribe from, different types of alerts. You can view your notifications in any of the following ways:

* From the [!UICONTROL Notifications] panel, which is available in the upper right at ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications"). From the panel, you can filter the list, edit your notification settings, or open [!UICONTROL Notification Center].

* From [!UICONTROL Notification Center], which opens in a separate window outside of Search, Social, & Commerce. To open [!UICONTROL Notification Center] from the [!UICONTROL Notifications] panel, click **[!UICONTROL View All]**.

* From a [!UICONTROL Notification Center] web application, which opens [!UICONTROL Notification Center] in a separate window outside of Search, Social, & Commerce.

  The application loads faster than the regular browser version and is automatically updated. You can install the application and manage it using the browser's app manager.

* From push notifications to your browser.

  When you enable push notifications, they appear according to the browser's notification conventions.

You can view your notifications, mark notifications as read or unread, and delete notifications.

## Notification types

* **[!UICONTROL Notices]**: Release, downtime, and other change management notices.

* **[!UICONTROL Recommendations]**: Opportunities identified to improve performance, implement best practices, and so on.

* **[!UICONTROL Warnings]**: Issues that require attention but are not critical to optimization or management.

* **[!UICONTROL Issues]**: Critical problems that require immediate attention. Account authorization error notifications are included.

## Notification categories

<!-- Update info, and update links to files for new UI once they're available-->

* [!UICONTROL Campaign Management]

  * **[!UICONTROL Bulksheets]**: Notifications that a [bulksheet operation](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) was completed or failed.<!-- Update link once file for new UI available-->

  * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md), which are required for the correct setup of critical functions.<!-- Moving to Campaign Management > Setup Errors at some point -->

  * **[!UICONTROL UI Actions]**: Notifications that your jobs that are performed in the background were completed or failed. The job types include [bulksheet jobs](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)<!-- Update link once file for new UI available-->, bulk edit jobs within the data table or using the toolbar, entity assignment jobs, or other actions within the user interface (such as synchronizing with ad networks, pasting rows, or renaming entities). Entity assignments include assigning or unassigning a [label classification value](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md) to any entity, assigning a campaign to a portfolio, and [assigning or unassigning a bid constraint to an entity](/help/search-social-commerce/new-ui/goals/constraints-manage.md).

  * [!UICONTROL Data Upload]

    * **[!UICONTROL Direct File Upload]**: Notifications that an account data file was uploaded, or an account data upload failed, via [manual account data upload](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md). <!-- Verify description-->

    * **[!UICONTROL File Upload to Cloud Storage]**: Notifications that an account data file was uploaded, or an account data upload failed, via [account data upload to an [!DNL Amazon] [!DNL S3] bucket](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md). <!-- Verify description-->

  * [!UICONTROL Network Errors]

    * **[!UICONTROL Account Auth Error]**: Notifications that Search, Social, & Commerce was unable to access an [ad network account](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) because of invalid credentials or an invalid or expired authorization token.

    * **[!UICONTROL Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network account](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md).

    * **[!UICONTROL Manager Account Auth Error]**: Notifications that Search, Social, & Commerce was unable to sync with an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md) because of invalid credentials or an invalid or expired authorization token.<!-- Update link once file for new UI available-->

* [!UICONTROL Insights & Reports]

  * **[!UICONTROL Advertising Insights]**: Notifications that [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) was completed or failed.

  * **[!UICONTROL Custom Alerts]**: Notifications that [alert instances](/help/search-social-commerce/new-ui/alerts-manage.md) were triggered for an alert template.

  * **[!UICONTROL Spreadsheet Feeds]**: Notifications that a [spreadsheet feed](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md) was completed or failed.

  * [!UICONTROL Reports]

    * **[!UICONTROL Grid Reports]**: Notifications that a data view report from a specific view (such as the contents of the data table in the [!UICONTROL Camapigns] view) was completed or failed.
    
    * **[!UICONTROL Reports]**: Notifications that a [custom or scheduled report](/help/search-social-commerce/new-ui/reports/management/report-manage.md) was completed or failed.

  * [!UICONTROL Portfolio Management]

    * **[!UICONTROL Intraday Optimization]**: Notifications when intraday optimization is disabled.

    * **[!UICONTROL Simulation Report]**: Notifications about [simulation jobs](/help/search-social-commerce/new-ui/plan/simulations/simulation-about.md).

    * [!UICONTROL Objective & Conversion Configuration]

      * **[!UICONTROL Auto Assign Campaign Conversion Goal - Advertiser Level]**: Notifications at the advertiser level about successful and failed auto-assignment of campaign conversion goals.

      * **[!UICONTROL Auto Assign Campaign Conversion Goal - Portfolio Level]**: Notifications at the portfolio level about successful and failed auto-assignment of campaign conversion goals.

    * [!UICONTROL Portfolios]

      * **[!UICONTROL Portfolio Bulksheet Diagnostic Report]**: Notifications about [portfolio bulk edit jobs via bulksheets](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-bulksheets.md).

      * **[!UICONTROL Portfolio Settings]**: Notifications about [changes to portfolio settings](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-settings.md).

<!--

In Campaign Management:

  * [!UICONTROL Setup Errors]

    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: Notifications that an account-level landing page suffix is incorrect due to missing or incorrect [AMO ID (`s_kwcid` parameter)](/help/integrations/analytics/ids.md).
  
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.

-->

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: Notifications when a portfolio's model accuracy deviates [by how much?] from expectations.
-->


## Available actions

* [View your notifications](#notification-view)

* [Edit your notification settings](#notification-edit)

* [Mark a notification as read or unread](#notification-mark-read-unread)

* [Delete a notification](#notification-delete)

* [Enable and disable push notifications](#notification-push-enable-disable)

* [Install and uninstall the [!UICONTROL Notification Center] web application](#notification-app-install-uninstall)

## View your notifications {#notification-view}

When you are [subscribed to notifications](#notification-edit) about account authentication errors, custom alerts that are triggered, and [!UICONTROL Advertising Insights] that are generated, you can view your notifications in either the [!UICONTROL Notifications] panel or [!UICONTROL Notification Center].

### View notifications within the [!UICONTROL Notifications] panel

1. In the upper right of any page, click ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications").

1. (Optional) Do any of the following:

   * To view the details of any notification, click the notification name.

     In some notifications, the [!UICONTROL Action Recommended] section may include a link that opens a filtered view of the affected or responsible entities.

   * To mark a notification as *read* or *unread*, hold the cursor over the alert name and click ![Mark as Read or Unread](/help/search-social-commerce/assets/notifications-read-unread.png "Mark as Read or Unread").

     Notifications marked as *read* are in a lighter-colored text but remain available until you delete them.

     ![Read and Unread notifications](/help/search-social-commerce/assets/notifications-read-vs-unread.png "Read and Unread notifications")

   * To change your subscription preferences for the notification type, click ![Settings](/help/search-social-commerce/assets/settings-nc.png "Settings") next to the notification, change your settings, and then click **[!UICONTROL Save]**.

   * To delete a notification, click ![Delete](/help/search-social-commerce/assets/delete.png "Delete") next to the notification.

   * To open [!UICONTROL Notification Center], click **[!UICONTROL View All]**.

### View notifications within [!UICONTROL Notification Center]

1. In the upper right of any page, click ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications").

1. Click **[!UICONTROL View All]**.

1. (Optional) To filter your notifications by type, click *[!UICONTROL Notices], [!UICONTROL Recommendations], [!UICONTROL Warnings], or [!UICONTROL Issues]*.

1. (Optional) Do any of the following:

   * To view the details of any notification, click the notification name.

     In some notifications, the [!UICONTROL Action Recommended] section may include a link that opens a filtered view of the affected or responsible entities.

   * To mark a notification as *read* or *unread*, hold the cursor over the alert name and click ![Mark as Read or Unread](/help/search-social-commerce/assets/notifications-read-unread.png "Mark as Read or Unread").

     Notifications marked as *read* are in a lighter-colored text but remain available until you delete them.

   * To change your subscription preferences for the notification type, click ![Settings](/help/search-social-commerce/assets/settings-nc.png "Settings") next to the notification, change your settings, and then click **[!UICONTROL Save]**.

   * To delete a notification, click ![Delete](/help/search-social-commerce/assets/delete.png "Delete") next to the notification.

## Edit your notification settings {#notification-edit}

You can optionally subscribe to, or unsubscribe from, email and web notifications about account authentication errors, all of your custom alerts that are triggered, and completion of the [!UICONTROL Advertising Insights] that you generate.

1. Open the notification settings in either of the following ways:

   * In the upper right of any page, click ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications") to open the [!UICONTROL Notifications] panel. In the upper right, click ![Settings](/help/search-social-commerce/assets/settings-nc.png "Settings").

   * In the upper right of any page, click ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications"), click **[!UICONTROL View All]** to open [!UICONTROL Notification Center], and then in the left menu, click ![Settings](/help/search-social-commerce/assets/settings-nc.png "Settings").

1. Change your settings for any notification category listed above:

   * To subscribe to, or unsubscribe from, notifications, move the slider in the [!UICONTROL Subscribe] column:

     * To unsubscribe from all notification types, move the slider to the left (disabled).

     * To subscribe to one or more notification types, move the slider to the right (enabled).

   * (When [!UICONTROL Subscribe] is enabled) To subscribe to email notifications, select the check box in the **[!UICONTROL Email]** column.

   * (When [!UICONTROL Subscribe] is disabled) To subscribe to web notifications within Search, Social, & Commerce and push notifications if they're enabled for the browser, select the check box in the **[!UICONTROL Web]** column.

     Web notifications are delivered only when you [enable push notifications](#notification-push-enable-disable) to your browser.

1. Click **[!UICONTROL Save]**.

## Mark a notification as read or unread {#notification-mark-read-unread}

Marking a notification as *read* or *unread* changes the number of unread notifications indicated in the [!UICONTROL Notifications] link at the top of each page (such as ![Notifications icon with unread notifications counter](/help/search-social-commerce/assets/notifications-unread.png "Notifications icon with unread notifications counter")).

Notifications marked as *read* are in a lighter-colored text but remain available until you delete them.

![Read and Unread notifications](/help/search-social-commerce/assets/notifications-read-vs-unread.png "Read and Unread notifications")

1. [Open the Notifications panel or Notification Center](#notification-view).

1. Hold the cursor over the alert name and click ![Mark as Read or Unread](/help/search-social-commerce/assets/notifications-read-unread.png "Mark as Read or Unread").

## Delete a notification {#notification-delete}

### Delete a notification within the [!UICONTROL Notifications] panel

1. In the upper right of any page, click ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications").

1. Click ![Delete](/help/search-social-commerce/assets/delete.png "Delete") next to the notification.

### Delete a notification within [!UICONTROL Notification Center]

1. In the upper right of any page, click ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications").

1. Click **[!UICONTROL View All]**.

1. (Optional) To filter your notifications by type, click *[!UICONTROL Notices]*, *[!UICONTROL Recommendations]*, *[!UICONTROL Warnings]*, or *[!UICONTROL Issues]*.

1. Click ![Delete](/help/search-social-commerce/assets/delete.png "Delete") next to the notification.

## Enable and disable push notifications {#notification-push-enable-disable}

You can enable notifications within Search, Social, & Commerce, where they appear according to the browser's notification conventions. On devices using [!DNL Microsoft Windows], notifications are displayed in the bottom right of the screen (system tray). On [!DNL Apple Mac] devices, notifications are displayed in the right menu.

Push notifications are available in the following browsers:

* [!DNL Google Chrome] 40 and higher

* [!DNL Microsoft Edge] 17 and higher

* [!DNL Mozilla Firefox] 44 and higher

You can disable push notifications according to the browser's standard procedure.

### Enable push notifications

1. In the upper right of any page, click ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications").

1. Click **[!UICONTROL View All]**.

1. In the bottom right, click ![Enable push notifications](/help/search-social-commerce/assets/notifications-push.png "Enable push notifications").

1. In the confirmation message, click **[!UICONTROL Enable]**.

1. Configure the browser to allow notifications from [!UICONTROL Notification Center] at `https://alert-center-ui-na.efrontier.com`.

   Default notification settings vary by browser, and you may either a) be automatically presented with the option to allow notifications from [!UICONTROL Notification Center] or b) need to manually manage the notification settings. For example, in [!DNL Microsoft Edge], you can allow notifications from [!UICONTROL Notification Center] from the browser toolbar. See instructions in the browser's help.

   ![Where to manage notification settings in Microsoft Edge](/help/search-social-commerce/assets/notifications-blocked-dialog.png "Where to manage notification settings in Microsoft Edge")

1. In your [notification settings](#notification-edit), enable [!UICONTROL Web] notifications for the alert types you want to be pushed.

### Disable push notifications

Remove notifications from `https://alert-center-ui-na.efrontier.com` within the browser's notification manager. For example, in [!DNL Google Chrome], you can remove or block notifications from specified sites at `chrome://settings/content/notifications`.

See instructions in the browser's help.

## Install and uninstall the [!UICONTROL Notification Center] web application {#notification-app-install-uninstall}

You can receive and manage notifications outside of your browser by installing a [!UICONTROL Notification Center] web application. The application looks the same, and has the same functionality, as [!UICONTROL Notification Center] within Search, Social, & Commerce. The application is available for [!DNL Google Chrome] 40 and higher or [!DNL Microsoft Edge] 17 and higher.

Once you install the [!UICONTROL Notification Center] application, it's automatically enabled in the browser's applications manager, and it loads as a separate window whose layout is dynamically arranged based on the window size. You can open and close the application from the browser's applications manager or pin it to the operating system's taskbar or dock. The application is automatically updated.

![Notification Center icon in Microsoft Windows taskbar](/help/search-social-commerce/assets/windows-taskbar.png "Notification Center icon in Microsoft Windows taskbar")

You can disable or uninstall the application from the browser's applications manager. For additional information about managing web applications, see the browser's help.

### Install the [!UICONTROL Notification Center] web application for [!DNL Google Chrome]

1. In the upper right of any page, click ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications").

1. Click **[!UICONTROL View All]**.

1. In the bottom right, click ![Install Notification Center web app](/help/search-social-commerce/assets/notifications-install-app.png "Install Notification Center web app").

1. In the confirmation message, click **[!UICONTROL Add]**.

1. In the Install App? message, click **[!UICONTROL Install]**.

### Install the [!UICONTROL Notification Center] web application for [!DNL Microsoft Edge]

* From within Search, Social, & Commerce:

   1. In the upper right of any page, click ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications").

   1. Click **[!UICONTROL View All]**.

   1. In the bottom right, click ![Install Notification Center web app](/help/search-social-commerce/assets/notifications-install-app.png "Install Notification Center web app").

   1. In the confirmation message, click **[!UICONTROL Add]**.

   1. In the [!UICONTROL Install Notification Center] app message, click **[!UICONTROL Install]**.

* From the [!DNL Edge] main menu:

   1. In the browser toolbar, click **...** > **[!UICONTROL Apps]** > **[!UICONTROL Install Notification Center]**.

   1. In the [!UICONTROL Install Notification Center] app message, click **[!UICONTROL Install]**.

### Uninstall the [!UICONTROL Notification Center] web application for [!DNL Google Chrome]

* In [!DNL Chrome], go to `chrome://apps`, right-click **[!UICONTROL notification-center]**, and then click **[!UICONTROL Remove from Chrome]**.

### Uninstall the [!UICONTROL Notification Center] web application for [!DNL Microsoft Edge]

1. In the [!DNL Edge] browser toolbar, click **...** > **[!UICONTROL Apps]** > **[!UICONTROL Manage apps]**. Alternately, go to `edge://apps`.

1. Right-click **[!UICONTROL Notification Center]** and click **[!UICONTROL Uninstall]**.
