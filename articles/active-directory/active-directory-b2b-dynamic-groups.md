---
title: Dynamic groups and Azure Active Directory B2B collaboration | Microsoft Docs
description: Shows how to use Azure AD dynamic groups with Azure Active Directory B2B collaboration 
services: active-directory
documentationcenter: ''
author: twooley
manager: mtillman
editor: ''
tags: ''

ms.assetid:
ms.service: active-directory
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: identity
ms.date: 12/14/2017
ms.author: twooley
ms.reviewer: twooley
ms.reviewer: sasubram

---

# Dynamic groups and Azure Active Directory B2B collaboration

## What are dynamic groups?
Dynamic configuration of security group membership for Azure Active Directory (Azure AD) is available in [the Azure portal](https://portal.azure.com). Administrators can set rules to populate groups that are created in Azure AD based on user attributes (such as userType, department, or country). Members can be automatically added to or removed from a security group based on their attributes. These groups can provide access to applications or cloud resources (SharePoint sites, documents) and to assign licenses to members. Read more about dynamic groups in [Dedicated groups in Azure Active Directory](active-directory-accessmanagement-dedicated-groups.md).

The appropriate [Azure AD Premium P1 or P2 licensing](https://azure.microsoft.com/pricing/details/active-directory/) is required to create and use dynamic groups. Learn more in the article [Create attribute-based rules for dynamic group membership in Azure Active Directory](active-directory-groups-dynamic-membership-azure-portal.md).

## What are the built-in dynamic groups?
The **All users** dynamic group enables tenant admins to create a group containing all users in the tenant with a single click. By default, the **All users** group includes all users in the directory, including Members and Guests.
Within the new Azure Active Directory admin portal, you can choose to enable the **All users** group in the Group Settings view.

![Shows enable the All Users group set to Yes](media/active-directory-b2b-dynamic-groups/enable-all-users-group.png)

## Hardening the All users dynamic group
By default, the **All users** group contains your B2B collaboration (guest) users as well. You can further secure your **All users** group by using a rule to remove guest users. The following illustration shows the **All users** group modified to exclude guests.

![Shows rule where user type not equals guest](media/active-directory-b2b-dynamic-groups/exclude-guest-users.png)

You might also find it useful to create a new dynamic group that contains only guest users, so that you can apply policies (such as Azure AD Conditional Access policies) to them.
What such a group might look like:

![Shows rule where user type equals guest](media/active-directory-b2b-dynamic-groups/only-guest-users.png)

## Next steps

Browse our other articles on Azure AD B2B collaboration:

* [What is Azure AD B2B collaboration?](active-directory-b2b-what-is-azure-ad-b2b.md)
* [B2B collaboration user properties](active-directory-b2b-user-properties.md)
* [Adding a B2B collaboration user to a role](active-directory-b2b-add-guest-to-role.md)
* [Delegate B2B collaboration invitations](active-directory-b2b-delegate-invitations.md)
* [B2B collaboration code and PowerShell samples](active-directory-b2b-code-samples.md)
* [Configure SaaS apps for B2B collaboration](active-directory-b2b-configure-saas-apps.md)

