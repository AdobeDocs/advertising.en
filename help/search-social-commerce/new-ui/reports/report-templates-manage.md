---
title: (New UI) Manage report templates
description: Learn how to create, view, edit, and delete reusable report templates for scheduled and on-demand reports.
feature: Search Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
---
# (New UI) Manage report templates

Report templates are predefined report layouts that you can reuse when you generate most reports. Using templates saves you time if you want to use non-default parameters, run variations of the same report, or run the same report according to a regular schedule. Saved templates are available on the **[!UICONTROL Templates]** tab in **[!UICONTROL Reports] > [!UICONTROL Reports]**.

You can maintain up to 100 templates at a time.

Viewing the data requires the [!UICONTROL View Scheduled Reports] permission. Creating, duplicating, editing, running, and deleting templates, as well as copying row data, requires the [!UICONTROL Edit Scheduled Reports] permission. You can edit only templates that you created.

## Available actions

* [Create a report template](#template-create) as a new template or based on an existing template.

* [View a report template's settings without changing the original](#template-view).

* [Edit a report template](#template-edit), including its schedule.

* [Run reports on demand for specified templates](#template-run).

* [Delete report templates](#template-delete).

* [Copy all data in selected rows to your clipboard](#copy-to-clipboard).

## Create a report template {#template-create}

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Reports]**.

1. Click the **[!UICONTROL Templates]** tab.

1. Do either of the following:

   * To create a new template, click **[!UICONTROL Create Template]**. In the **[!UICONTROL Create a New Template]** panel, select the report category and report type, and then click **[!UICONTROL Proceed]**.

   * To create a template based on an existing template, hold the cursor over the template row and click either ![Template Settings](/help/search-social-commerce/assets/settings-new.png "Template Settings") **[!UICONTROL Template Settings]** or **[!UICONTROL ...] > [!UICONTROL Duplicate]**.

1. Enter a unique **[!UICONTROL Report Name]** for the template, and make sure **[!UICONTROL Save as Template]** is enabled.

   The setting is enabled by default when you start with **[!UICONTROL Create Template]**. If you disable it, the final action changes to **[!UICONTROL Run Report]**, which generates a report instead of saving a template.

1. Configure the report settings for [basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md), [assist reports](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md), [model accuracy reports](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md), or [specialty reports](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md).

   Click **[!UICONTROL Next]** to move between the settings sections.

1. (Optional) To generate reports automatically, configure the **[!UICONTROL Frequency]** and delivery settings in **[!UICONTROL Scheduling]**.

1. Click **[!UICONTROL Create]**.

You can also save a template while [creating a report from the Latest Reports tab](/help/search-social-commerce/new-ui/reports/management/report-manage.md) by enabling **[!UICONTROL Save as Template]** before submitting the report settings.

## View a report template's settings {#template-view}

To inspect settings without changing the original template, open a duplicate. This requires the [!UICONTROL Edit Scheduled Reports] permission. Opening the duplicate doesn't save a new template.

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Reports]**.

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template row and click ![Template Settings](/help/search-social-commerce/assets/settings-new.png "Template Settings") **[!UICONTROL Template Settings]**.

1. Review the report settings.

1. Click **[!UICONTROL Cancel]** when you're finished. If prompted to discard the setup, click **[!UICONTROL Discard]**.

To save a copy instead, follow the [template creation procedure](#template-create).

## Edit a report template {#template-edit}

You can change the settings and schedule of any template that you created. The changes apply to reports generated from the template in the future.

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Reports]**.

1. Click the **[!UICONTROL Templates]** tab.

1. Select the check box next to one template that you created.

1. In the bulk actions toolbar, click **[!UICONTROL Edit]**.

   [!UICONTROL Edit] isn't available when multiple templates are selected or the selected template was created by another user.

1. Change the report settings. To add, change, or remove a schedule, edit **[!UICONTROL Frequency]** in **[!UICONTROL Scheduling]**.

   Select a daily, weekly, or monthly frequency for scheduled reports. To remove a recurring schedule, select **[!UICONTROL Now]**.

   **[!UICONTROL Save as Template]** and **[!UICONTROL Type]** are read-only when editing an existing template. You don't need to enable [!UICONTROL Save as Template] again.

1. Click **[!UICONTROL Save]**.

## Run reports on demand for specified templates {#template-run}

You can run reports for one or more templates at any time.

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Reports]**.

1. Click the **[!UICONTROL Templates]** tab.

1. Do either of the following:

   * (To run a single template):

     1. Open the template row's menu and select **[!UICONTROL Run]**.

     1. In the confirmation message, click **[!UICONTROL Confirm]**.
   
   * (To run one or more templates):

     1. Select the check box next to each template that you want to run.

     1. In the bulk actions toolbar, click **[!UICONTROL Run]**.
     
     1. In the confirmation message, click **[!UICONTROL Confirm]**.

You can also run a template while editing it by clicking **[!UICONTROL Run Report]** and then **[!UICONTROL Confirm]**. Save any changes first; this action runs the saved template.

## Delete report templates {#template-delete}

You can delete any report template available to you. When you delete a template that includes a schedule, that report isn't generated in the future.

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Reports]**.

1. Click the **[!UICONTROL Templates]** tab.

1. Do either of the following:

   * (To delete a single template):

     1. Open the template row's menu and select **[!UICONTROL Delete]**.

     1. In the confirmation message, click **[!UICONTROL Confirm]**.
   
   * (To delete one or more templates):

     1. Select the check box next to each template that you want to delete.

     1. In the bulk actions toolbar, click **[!UICONTROL Delete]**.
     
     1. In the confirmation message, click **[!UICONTROL Confirm]**.

## Copy all data in selected rows to your clipboard {#copy-to-clipboard}

Copy the visible information in selected rows, according to the applied filters and columns visible in the view. The information is saved as tab-separated values (TSV).

1. Select the check box next to each row whose data you want to copy.

1. In the bulk actions toolbar, click **[!UICONTROL Copy]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.
