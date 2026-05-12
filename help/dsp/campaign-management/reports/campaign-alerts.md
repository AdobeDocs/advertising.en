---
title: View alerts
description: Learn how to view alerts and recommended resolutions for your campaigns and campaign components. Use alerts to troubleshoot issues with your campaigns.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
exl-id: 667bf1c3-3bad-4a1a-b907-0c9bfe5362a9
TQID: https://experienceleague.adobe.com/WhIrF0O8OiqE1aVijiIJ1a-no-sXpimM2CEevnZyWhc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
    internal-label: DSP placements
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
    internal-label: DSP Campaigns
  - id: d9510790-d834-436d-8423-8d69cd50464a
    internal-label: DSP Ads
  - id: f784309e-91ce-4bb5-ade4-5cbbceabecc0
    internal-label: " DSP Campaign Data Views"
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
    internal-label: DSP Packages
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# View alerts

DSP helps you identify when any of your campaigns or campaign components have issues. For each issue, DSP creates an alert with a time stamp and the recommended action to resolve the issue. Reasons for alerts include configuration issues (for example, when no ads are attached to a placement or when a deal is set up incorrectly), ad rejection, and campaign health issues (such as poor ad delivery or performance). Alerts are available at the campaign, package, placement, ad, and deal levels. 

Alerts are available in the following locations:

* A [!UICONTROL Pulse Panel] icon in the [!UICONTROL Campaigns], [!UICONTROL Packages] and package details, [!UICONTROL Placements], and [!UICONTROL Ads] views indicates if any alerts are available for the items in that view. When the icon has a blue dot (![Pulse Panel icon when alerts are available](/help/dsp/assets/alerts-panel.png "Pulse Panel icon when alerts are available")), alerts are available. When no dot is visible (![Pulse Panel icon when no alerts are available](/help/dsp/assets/alerts-panel-empty.png "Pulse Panel icon when no alerts are available")), no alerts are available.

* The data tables in the same views include an "[!UICONTROL Alerts]" column that indicates when the item &mdash; or its components &mdash; has an issue. Alert indicators include "Critical" (![Critical](/help/dsp/assets/indicator-critical.png "Critical")), "Warning" (![Warning](/help/dsp/assets/indicator-warning.png "Warning")), and "Information" (![Information](/help/dsp/assets/indicator-information.png "Information")).

You can open the relevant campaign management view for any alert so that you can edit the settings as needed to resolve the issue.

You can also choose to ignore an individual alert, which removes it from the [!UICONTROL Pulse] panel.

Alerts and alert indicators automatically disappear when the underlying issues are resolved.

## View alerts in the [!UICONTROL Pulse Panel]

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Do any of the following:

   * (For all alerts applicable for the view) To the right of the toolbar in any campaign management view, click ![Pulse Panel icon when alerts are available](/help/dsp/assets/alerts-panel.png "Pulse Panel icon when alerts are available").
   
   * (For all alerts for a specific campaign) Click the alert indicator for a campaign row, and then click **[!UICONTROL View in Pulse panel]**.

   * (For all alerts for a specific package, placement, or ad) Do the following:
   
     1. Click the campaign name.

     1. In the submenu, click **[!UICONTROL Packages]**, **[!UICONTROL Placements]**, or **[!UICONTROL Ads]** to open the relevant campaign component view.

     1. Click the alert indicator for a package, placement, or ad row, and then click **[!UICONTROL View in Pulse Panel]**.

   All alerts associated with the campaign and its components, including targeted deals, are listed. By default, critical alerts are listed first.

1. (Advertisers with Advertising Creative; optional) Click the **[!UICONTROL Creative]** tab to view alerts for placements that include Advertising Creative experiences. 

1. (Optional) To group the alerts according to their first date of detection, or to filter the alerts by alert status, component status, component type, or with a specific campaign name, click ![Filter button](/help/dsp/assets/filter.png) in the upper right of the panel, select the filter options, and then click **[!UICONTROL Apply]**.

1. To view a list of all affected campaign components for a specific alert type, click the alert name, such as "[!UICONTROL Package: No Active Placement (*N*)]". To view the details for each affected component, including the recommended action, click [!UICONTROL EXPAND ALL] or click the component name. To open the relevant campaign management view for any affected component so you can make the recommended changes, hold the cursor over the component name and click ![Go to view](/help/dsp/assets/go-to-view.png "Go to view").

1. (Optional) To ignore (hide) an alert, hold the cursor over the component name and click ![Ignore](/help/dsp/assets/alert-ignore.png "Ignore"), and then click **[!UICONTROL Ignore alert till next check]**, **[!UICONTROL Ignore alert for 3 days]**, or **[!UICONTROL Ignore indefinitely]**.

  You have a few seconds after ignoring an alert to undo the action. Once the option message closes, you can't cancel the action.

1. (Optional) To retrieve ignored alerts, filter the alerts to show an [!UICONTROL Alert Status] of "[!UICONTROL All]" or "[!UICONTROL Ignored]." To unignore an alert, hold the cursor over the component name and click ![Un-ignore](/help/dsp/assets/alert-un-ignore.png "Un-ignore").

## Close the [!UICONTROL Pulse Panel]

* To the right of the toolbar, click ![Pulse Panel icon when alerts are available](/help/dsp/assets/alerts-panel.png "Pulse Panel icon when alerts are available") or ![Pulse Panel icon when no alerts are available](/help/dsp/assets/alerts-panel-empty.png "Pulse Panel icon when no alerts are available").

>[!MORELIKETHIS]
>
>* [Types of performance reports in campaign management views](campaign-reports-about.md)
