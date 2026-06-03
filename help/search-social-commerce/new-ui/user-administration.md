---
title: (New UI) User administration
description: Learn how to manage user access.
feature: Search Introduction
exl-id: bfc43692-cfb6-468f-90df-a808a21a0c23
TQID: 'https://experienceleague.adobe.com/b28N5zmqqdZ6Yvg2swGLWv260fWsMUgjK2eW1DDn-uo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# (New UI) User administration for Search, Social & Commerce

Some users can manage access to the new Search, Social, & Commerce user interface using the [Adobe Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html), which is the central location for managing all Adobe entitlements and user management. Users are categorized as either end users or administrators. Your Adobe Account Team notifies you if you're an administrator. If you're an administrator, see the following sections to identify your permissions and workflows for managing users.

## Types of administrators

Admin Console provides multiple types of administrators. The following administrator types and permissions are required for Search, Social, & Commerce. You can add additional types if you wish to delegate user management tasks.

**System admin:** Super user who manages all products for the organization, including all client instances for the organization. (Client instances are the same as legacy advertiser accounts, with one or more instances per organization ID). A system admin can perform all administrative tasks in Admin Console for the organization and can delegate administrative functionality to other users for any of the organization's products.

**Product admin:** Manages access to a specific [!DNL Adobe] product (such as Search, Social, & Commerce) and the user entitlements to that product. Product admins can create product profiles for the product, create (but not remove) users and user groups for the product, add or remove users and user groups from product profiles, and add or remove other product admins from the product.

<!-- 
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Default product profiles

Product profiles, which are similar to roles, entitle users with specific services for a specific product.

The new user interface for Search, Social & Commerce has the following default product profiles, which provide different subsets of features and services. You can't edit the product permissions for the default product profiles or delete the default product profiles. However, product admins, product profile admins, and system administrators can create and manage additional product profiles with different subsets of available permissions, as needed.

* **[!UICONTROL Basic Optimization]:** For users who need standard portfolio management and planning capabilities with basic settings access.

* **[!UICONTROL Expert Optimization]:** For power users who need full portfolio settings access including advanced expert-level controls. Includes all performance planning, objective, campaign, setup, and report management permissions.

* **[!UICONTROL Read-Only Optimization]:** For users who need visibility into portfolios, simulations, and campaigns without any edit or create capabilities.

* **[!UICONTROL \[Optimization\] Admin]:** Grants full access to all functionality available and allows users to create new client instances (the same as legacy advertiser accounts, with one or more instances per organization ID). Don't assign this right to anyone unless you have a proper business justification.

### Functionality per product profile

<!-- These don't correspond exactly to the GUI menu -->

A checkmark (✓) indicates that the permission is included in the product profile.

**Portfolio Management**

| Permission | Basic | Expert | Read-Only | Admin |
|---|---|---|---|---|
| View Portfolios | ✓ | ✓ | ✓ | ✓ |
| View Portfolio Settings | ✓ | ✓ | ✓ | ✓ |
| View Portfolio Performance Details | ✓ | ✓ | ✓ | ✓ |
| View Portfolio Groups | ✓ | ✓ | ✓ | ✓ |
| Edit Portfolio Groups | ✓ | ✓ | | ✓ |
| Edit Basic Portfolio Settings | ✓ | | | |
| Edit Expert Portfolio Settings | | ✓ | | ✓ |

<!--
Noone has permissions as of 6/1; spelling [sic]:
| Edit Advance Portfolio Settings | | | | |
-->

**Performance Planning Management**

| Permission | Basic | Expert | Read-Only | Admin |
|---|---|---|---|---|
| View Simulation | ✓ | ✓ | ✓ | ✓ |
| Create Simulation | ✓ | ✓ | | ✓ |
| View Spend Recommendations | | ✓ | | ✓ |
| Apply Spend Recommendations | | ✓ | | ✓ |

**Objective Management**

| Permission | Basic | Expert | Read-Only | Admin |
|---|---|---|---|---|
| View Objective | ✓ | ✓ | ✓ | ✓ |
| Edit Objective | ✓ | ✓ | | ✓ |
| View Conversion Value Rules | ✓ | ✓ | ✓ | ✓ |
| Edit Conversion Value Rules | | ✓ | | ✓ |
| View Conversions | | ✓ | | ✓ |
| Edit Conversions | | ✓ | | ✓ |
| View Conversions Visibility | | ✓ | | ✓ |

**Campaign Management**

| Permission | Basic | Expert | Read-Only | Admin |
|---|---|---|---|---|
| View Campaigns | ✓ | ✓ | ✓ | ✓ |
| Edit Campaigns | ✓ | ✓ | | ✓ |
| View Ad Groups | ✓ | ✓ | ✓ | ✓ |
| Edit Ad Groups | ✓ | ✓ | | ✓ |
| Ads View | ✓ | ✓ | ✓ | ✓ |
| Ads Edit | | ✓ | | ✓ |
| Keywords View | ✓ | ✓ | ✓ | ✓ |
| Audiences View | ✓ | ✓ | ✓ | ✓ |
| Auto Targets View | ✓ | ✓ | ✓ | ✓ |
| Creatives View | ✓ | ✓ | ✓ | ✓ |
| Extensions View | ✓ | ✓ | ✓ | ✓ |
| Label Classifications View | ✓ | ✓ | ✓ | ✓ |
| Placements View | ✓ | ✓ | ✓ | ✓ |
| Recommendations View | ✓ | ✓ | ✓ | ✓ |
| View Bulksheets | | ✓ | | ✓ |
| Edit Bulksheets | ✓ | ✓ | ✓ | ✓ |

**Report Management**

| Permission | Basic | Expert | Read-Only | Admin |
|---|---|---|---|---|
| View History Logs | ✓ | ✓ | ✓ | ✓ |
| View Scheduled Reports | ✓ | ✓ | ✓ | ✓ |
| Edit Scheduled Reports | | ✓ | | ✓ |

**Setup Management**

| Permission | Basic | Expert | Read-Only | Admin |
|---|---|---|---|---|
| View Account | ✓ | ✓ | ✓ | ✓ |
| Edit Account | | ✓ | | ✓ |
| View MCC Accounts | ✓ | ✓ | ✓ | ✓ |
| Edit MCC Accounts | | ✓ | | ✓ |

## Tasks for administrators

### Sign in to Adobe Admin Console and open it to Search, Social, & Commerce

>[!PREREQUISITES]
>
>You must have some type of administrator access to Search, Social, & Commerce to sign in to Admin Console. 

1. Go to https://adminconsole.adobe.com/enterprise/.

1. (If you're not signed in to CX Enterprise) Sign in to CX Enterprise:

   1. Enter your [!DNL Adobe] ID, and click **[!UICONTROL Continue]**.

   1. Select either **[!UICONTROL Personal Account]" or **[!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Select the applicable CX Enterprise organization.

      Admin Console opens to the [!UICONTROL Overview] tab.
   
   1. Under [!UICONTROL Product & services], click "[!UICONTROL Adobe Advertising, Search, Social, & Commerce &mdash; Org Name]."
   
      The product page opens to the [!UICONTROL Product profiles] tab for Search, Social, & Commerce. Additional tabs include [!UICONTROL Users] and [!UICONTROL Product Admins].

### Workflow for system administrators

Follow this workflow for each client instance of Search, Social, & Commerce.

1. [Sign in to Adobe Admin Console and open it to Search, Social, & Commerce](#open-admin-console).

1. (Optional) [Add another system administrator](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise) as backup.

1. Delegate product and user management by [adding product administrators](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise).

### Workflow for product administrators

Follow this workflow for each client instance of Search, Social, & Commerce.

1. [Sign in to Adobe Admin Console and open it to Search, Social, & Commerce](#open-admin-console).

1. As needed, create end users [individually](https://helpx.adobe.com/enterprise/using/manage-users-individually.html) or [in bulk](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. (Optional) Create [user groups](https://helpx.adobe.com/enterprise/using/user-groups.html) for the instance and assign users to each user group.

   If the instance has many users, create user groups to ensure that users are assigned the right profiles based on their level of expertise. (See Step 4 for assigning user groups to product profiles.) You can create user groups based on the line of business, user access needs, user hire date, or other criteria.

   >[!IMPORTANT]
   >
   >User group names should clearly communicate the rights that the group of users should be assigned. For example, if you want to create a user group with "Read Only" rights, include "Read Only" in the user group name, such as "Acme_Uk_ReadOnly" or "Acme_ReadOnly." 

1. (Optional) [Create custom product profiles](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) with defined permission sets.

   Custom profiles are in addition to the four default product profiles that are already available.

   Each product profile for an organization must have a unique name. If your organization uses multiple Search, Social, & Commerce instances (for example, Acme_US and Acme_JP), then you can't duplicate a product profile name in multiple instances. **Best practice:** Use the naming convention `<Name>_<Instance>,` such as "Simulations_Only_JP."

   **Caution:** Product permissions are very granular. Be careful when you configure custom product profiles or you may omit functionality that you want to include.

1. [Assign each user or user group to the relevant product profile](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) manually or in bulk.

## Complete user administration guide and additional links

* For more information about user administration using Adobe Admin Console, see "[Adobe Enterprise & Teams Administration Guide](https://helpx.adobe.com/enterprise/admin-guide.html)," including the [Admin Console overview](https://helpx.adobe.com/enterprise/using/admin-console.html).

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
