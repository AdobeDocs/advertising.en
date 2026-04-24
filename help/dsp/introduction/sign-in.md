---
title: Sign in to DSP
description: Learn how to sign in to DSP.
feature: DSP Introduction
exl-id: 1704cd75-81f8-4715-a177-69a03093ba1d
TQID: https://experienceleague.adobe.com/KjBIag8qcpMONcX6pS2IJot3IA4Q-KOq0Av-1VzAot4
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Sign in to Adobe Advertising DSP

Adobe Advertising DSP is transitioning to the Adobe Identity Management Service (IMS) for login authentication. IMS provides single sign-on (SSO) access using federated IDs to all [!DNL Adobe] products that support IMS, including Real-Time Customer Data Platform, Customer Journey Analytics, [!DNL Target], and [!DNL Analytics]. With the change: 

* You can use one [!DNL Adobe ID] to sign in across [!DNL Adobe] products from either the Adobe CX Enterprise (formerly Adobe Experience Cloud) sign-in page or the legacy DSP sign-in page. Your [!DNL Adobe ID] provides user profile management. In a future release, you'll be able to change the DSP account, IMS organization account, and [!DNL Adobe] product from the top menu.

* Enterprise authentication is supported.

* You can stay logged in for 24 hours instead of logging in every hour.

Your current DSP credentials will remain active for a short time so that you can prepare for the change.

## Use a legacy DSP login for authentication

* Go to [advertising.adobe.com](https://advertising.adobe.com), and sign in using your legacy DSP credentials.

## Use an [!DNL Adobe ID] for authentication

1. Open either of the following sign-in screens:

   * Go to [advertising.adobe.com](https://advertising.adobe.com). Under "[!UICONTROL Sign in with the Adobe Experience Cloud account]," click **[!UICONTROL Continue]**.
   
   * Go to [experience.adobe.com](https://experience.adobe.com).

1. Enter your credentials:

   * If you already use an [!DNL Adobe] account, then sign in with your existing credentials.

   * If you don't have an [!DNL Adobe] account, then look for an email inviting you to create an [!DNL Adobe] account. You'll receive one invitation for each of your DSP accounts. Follow the link in the email to set up your credentials. If you have multiple DSP accounts, follow the instructions to link them.

1. Choose your organization:

   * If prompted, select either **[!UICONTROL Personal Account]" or **[!UICONTROL Company or School Account]**.

   * If you have access to multiple IMS organizations, select the correct one.
   
For more information about the CX Enterprise interface, including managing your user profile, see "[CX Enterprise interface and administration](https://experienceleague.adobe.com/en/docs/core-services/interface/experience-cloud)."

### Troubleshooting

For general sign-in issues, see also "[Solve Adobe account sign-in issues](https://helpx.adobe.com/manage-account/kb/account-password-sign-help.linkfree.html)."

#### Are there any prerequisites to enable a new [!DNL Adobe] IMS login? 

To add a new login account, share the email address with your Adobe Account Team. The team will add your address to the user list for the IMS organization to which DSP has been provisioned. 

In the meanwhile, the user can continue to use their legacy DSP credentials.

#### After signing in using an Adobe IMS account, I'm redirected back to the adobe.advertising.com login page.  

Check with your IMS organization administrator that the email you are using was added to the IMS organization. If the administrator confirms that you are added to the IMS organization, then ask your Adobe Account Team to provision your account to use DSP.  

In the meanwhile, you can continue to use your legacy DSP credentials.

#### I signed in using an incorrect email address, which signed me into [!DNL Adobe] but doesn't provide DSP access.  

1. Go to [experience.adobe.com](https://experience.adobe.com) and sign out.  

1. Go to [advertising.adobe.com](https://advertising.adobe.com) and sign in with the correct email ID.  

#### My [!DNL Adobe] IMS account and DSP account are registered with different emails. How do I sign in using my [!DNL Adobe] IMS account? 

Ask your Adobe Account Team to provision your existing [!DNL Adobe] IMS account to use DSP.
