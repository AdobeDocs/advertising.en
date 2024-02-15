---
title: View Alerts
description: Learn how to view alerts and recommended resolutions for your campaigns and campaign components.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
---
# View Alerts

When any of your campaigns or campaign components has an issue, an alert is created, with a time stamp and recommended action to resolve the issue. Reasons for alerts include configuration issues (such as the absence of active child entities or a required budget update), ad rejection, and metric issues (such as poor ad delivery or performance). Alerts are available at the campaign, package, placement, ad, and deal levels.

Alerts are available in the following locations:

* An [!UICONTROL Alerts Panel] icon in the [!UICONTROL Campaigns], [!UICONTROL Packages] and package details, [!UICONTROL Placements], and [!UICONTROL Ads] views indicates if any alerts are available for the entities that are listed. When the icon has a blue dot (![Alerts Panel icon when alerts are available](/help/dsp/assets/alerts-panel.png "Alerts Panel icon when alerts are available")), alerts are available. When no dot is visible (![Alerts Panel icon when no alerts are available](/help/dsp/assets/alerts-panel-empty.png "Alerts Panel icon when no alerts are available")), no alerts are available.

* The data tables in the same views include an "[!UICONTROL Alerts]" column that indicates when an entity (or any child entity under it) has an issue. Alert indicators include "Critical" (![Critical](/help/dsp/assets/indicator-critical.png "Critical")) and "Warning" (![Warning](/help/dsp/assets/indicator-warning.png "Warning")).

You can open the relevant entity view for any entity with an alert. You can then edit the entity settings as needed to resolve the issue.

You can also choose to ignore an individual alert, which removes it from the [!UICONTROL Alerts Panel].

Alerts and alert indicators disappear when the underlying issues are resolved.

## View Alerts in the [!UICONTROL Alerts Panel]<!-- verify final name-->

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Do any of the following:

   * (For all alerts applicable for the view) To the right of the toolbar in any campaign management view, click ![Alerts Panel icon when alerts are available](/help/dsp/assets/alerts-panel.png "Alerts Panel icon when alerts are available").
   
   * (For all alerts for a specific campaign) Click the alert indicator for a campaign row to see the number of applicable alerts, and then click **[!UICONTROL View in alert panel]**.

   * (For all alerts for a specific package, placement, or ad) Do the following:
   
     1. Click the campaign name.

     1. In the submenu, click **[!UICONTROL Packages]**, **[!UICONTROL Placements]**, or **[!UICONTROL Ads]** to open the relevant campaign component view.

     1. Click the alert indicator for a package, placement, or ad row, and then click **[!UICONTROL View in alert panel]**.

   By default, critical alerts are listed first.

1. (Optional) To filter the alerts by alert grouping or status, entity status, or entity type, or for a specific campaign, click ![Filter button](/help/dsp/assets/filter.png) in the upper right of the panel, select the filter options, and then click **[!UICONTROL Apply]**.

1. To view a list of all affected entities for a specific alert type, click the alert name, such as "[!UICONTROL Package: No Active Placement (*N*)]". To view the details for each affected entity, including the recommended action, click [!UICONTROL EXPAND ALL].

1. (Optional) To open the relevant entity view for any entity with an alert, hold the cursor over the entity name and click ![Go to view](/help/dsp/assets/go-to-view.png "Go to view").

1. (Optional) To permanently remove an individual alert from the [!UICONTROL Alerts Panel], hold the cursor over the entity name and click ![Ignore](/help/dsp/assets/alert-ignore.png "Ignore"), and then click **[!UICONTROL Ignore indefinitely]**.<!-- may add additional options to "Ignore alert until next check" and "Ignore alert for 3 days" -->

   You have a few seconds after ignoring an alert to undo the action. Once the option message closes, you can't cancel the action.

## Close the [!UICONTROL Alerts Panel]<!-- verify final name-->

* To the right of the toolbar, click ![Alerts Panel icon when alerts are available](/help/dsp/assets/alerts-panel.png "Alerts Panel icon when alerts are available") or ![Alerts Panel icon when no alerts are available](/help/dsp/assets/alerts-panel-empty.png "Alerts Panel icon when no alerts are available").

>[!MORELIKETHIS]
>
>* [Types of Performance Reports in Campaign Management Views](campaign-reports-about.md)
