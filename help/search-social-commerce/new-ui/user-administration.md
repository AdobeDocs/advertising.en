---
title: User administration
description: Learn how to .
feature: Search Introduction
---
# (New UI) User administration for Search, Social & Commerce

Some users can manage access to the new Search, Social, & Commerce user interface using the Adobe Admin Console, which is the central location for managing all Adobe entitlements and user management. Users are categorized as either end users or administrators. Your Adobe Account Team will notify you if you're an administrator. If you're an administrator, see the following sections to identify your permissions and workflows for managing users.<!-- How can you see what your user role is, or will your Adobe Account Team tell you? -->

## Relevant types of administrators

Admin Console provides multiple types of administrators, but only the following administrator types and permissions are relevant for Search, Social, & Commerce.

**System admin:** Super user for the organization. A system admin can perform all administrative tasks in Admin Console for the organization and can delegate administrative functionality to other users (product admins).<!--, product profile administrators, and user group administrators.  -- I think it's ONLY PRODUCT ADMINS FOR US?  Verify. -->

**Product admin:** Manages access to a specific [!DNL Adobe] product (such as Search, Social, & Commerce) and their users' entitlements to that product. Product admins can create product profiles for the product, create (but not remove) users and user groups, add or remove users and user groups from product profiles, and add or remove other product admins from the product.

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Default product profiles

Product profiles, which are similar to roles, entitle users with specific services for a specific product.

The new user interface for Search, Social & Commerce has the following default product profiles, which provide different subsets of features and services. You can't edit or delete the default product profiles. However, system administrators can create and manage additional product profiles with different subsets of permissions, as needed.

* **Basic Optimization:** This profile provides the following functionality:

  * Objectives: Full access

  * Simulations: Full access

  * Portfolio Groups: Full access

  * Portfolios: Create/edit access to portfolio settings for Objectives, Campaigns, and Spend Management; read-only access to the remaining portfolio settings.

  * Campaigns: Read-only access to campaign settings (no create, edit, or delete features are available); full access to constraint and portfolio assignments<!-- Is that the correct wording? -->

  * Ad Groups: Read-only access to ad group settings (no create, edit, or delete features are available); full access to constraint and portfolio assignments<!-- Is that the correct wording? -->

  This access level is preferred for users who are still learning to use Search, Social, & Commerce.

* **Expert Optimization:** This profile provides the following functionality:

  * Objectives: Full access

  * Simulations: Full access

  * Portfolio Groups: Full access

  * Portfolios: Full access

  * Campaigns: Read-only access to the campaign list (no campaign creation, editing, or deleting features are available yet); full access to constraint and portfolio assignments<!-- Is that the correct wording? -->

  * Ad Groups: Read-only access to the ad group list (no campaign creation, editing, or deleting features are available yet); full access to constraint and portfolio assignments<!-- Is that the correct wording? -->

  This access level is recommended for expert users of Search, Social, & Commerce.

* **Read-Only:** This profile provides the following functionality:

  * Objectives: Read-only access

  * Simulations: Read-only access

  * Portfolio Groups: Read-only access

  * Portfolios: Read-only access

  * Campaigns: Read-only access

  * Ad Groups: Read-only access

* **Admin:** This profile grants full access to all functionality available and allows users to create new client instances. Don't assign this right to anyone unless you have a proper business justification.

<!-- Do I need to include this? If so, adjust wording as needed

## Product-specific instances

 -->

## Tasks for administrators

### Sign in to Adobe Admin Console and open it to Search, Social, & Commerce

>[!PREREQUISITES]
>
>You must have administrator access<!-- which kind? Product administrator, system administrator, but I'm sure also product profile administrator or user group administrator (that might be an internal group -- check) --> to Search, Social, & Commerce. 

1.	Go to https://adminconsole.adobe.com/enterprise/.

1. (If you're not signed in to Experience Cloud) Sign in to Experience Cloud:

   1. Enter your [!DNL Adobe] ID, and click **[!UICONTROL Continue]**.

   1. Select either **[!UICONTROL Personal Account]" or **[!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1.	Select the applicable Experience Cloud organization. 
   
   1.	Under Product & Services, click "[!UICONTROL Adobe Advertising, Search, Social, & Commerce &mdash; Org Name]."

   The product page opens by default to the [!UICONTROL Product profiles] tab for Search, Social, & Commerce. Additional tabs include [!UICONTROL Users] and [!UICONTROL Product Admins].

### Workflow for system administrators

1. [Sign in to Adobe Admin Console and open it to Search, Social, & Commerce](#open-admin-console).

1. Delegate product and user management by [adding product administrators](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise).

<!-- what else? -->

### Workflow for product administrators

1. [Sign in to Adobe Admin Console and open it to Search, Social, & Commerce](#open-admin-console).

1. As needed, create end users [individually](https://helpx.adobe.com/enterprise/using/manage-users-individually.html) or [in bulk](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. (Optional) Create [user groups](https://helpx.adobe.com/enterprise/using/user-groups.html) for each product instance and assign users to each user group.

   If the instance has many users, create user groups to ensure that users are assigned the right profiles based on their level of expertise. (See Step 4 for assigning user groups to product profiles.) You can create user groups based on the line of business, user access needs, user hire date, or other criteria.

   >[!IMPORTANT]
   >
   >User group names should clearly communicate the rights that the group of users should be assigned. For example, if you want to create a user group with “Read Only” rights, include “Read Only” in the user group name, such as "Acme_Uk_ReadOnly" or "Acme_ReadOnly." 

1. (Optional) [Create custom product profiles](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) with defined permission sets.

   Custom profiles are in addition to the four default product profiles that are already available.

   Each product profile for an organization must have a unique name. If your organization uses multiple Search, Social, & Commerce instances (for example, Acme_US and Acme_JP), then you can't duplicate a product profile name in multiple instances. **Best practice:** Use the naming convention `<Name>_<Instance>,` such as "Simulations_Only_JP."

1. [Assign each user or user group to the relevant product profile](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) manually or in bulk.

## Complete user administration guide and additional links

* For more information about user administration using Adobe Admin Console, see "[Adobe Enterprise & Teams Administration Guide](https://helpx.adobe.com/enterprise/admin-guide.html)," including the [Admin Console overview](https://helpx.adobe.com/enterprise/using/admin-console.html)

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
