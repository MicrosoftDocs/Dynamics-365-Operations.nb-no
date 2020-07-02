---
title: Opprette nye brukere
description: Brukere er interne ansatte i din organisasjon, eller eksterne kunder og leverandører, som trenger tilgang til systemet for å utføre jobbene sine.
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d126b449074663772549b96b86acb53db971a5d4
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435590"
---
# <a name="create-new-users"></a><span data-ttu-id="e74ad-103">Opprette nye brukere</span><span class="sxs-lookup"><span data-stu-id="e74ad-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e74ad-104">Brukere er interne ansatte i din organisasjon, eller eksterne kunder og leverandører, som trenger tilgang til systemet for å utføre jobbene sine.</span><span class="sxs-lookup"><span data-stu-id="e74ad-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="e74ad-105">Knytte en bruker til en lisens (bare nye lisenstyper)</span><span class="sxs-lookup"><span data-stu-id="e74ad-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="e74ad-106">For kunder som har én av de nye lisenstypene som ble lagt til i oktober 2019, må brukere være knyttet til en lisens.</span><span class="sxs-lookup"><span data-stu-id="e74ad-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="e74ad-107">Brukere som er knyttet til en lisens, legges automatisk til som systembrukere som ikke har noen roller første gang de logger på.</span><span class="sxs-lookup"><span data-stu-id="e74ad-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="e74ad-108">Systemadministratorer kan [tilordne lisenser til brukere](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) i [administrasjonssenteret for Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="e74ad-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="e74ad-109">Knytte en ekstern bruker til en lisens (bare nye lisenstyper)</span><span class="sxs-lookup"><span data-stu-id="e74ad-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="e74ad-110">Brukere utenfor leieren som miljøet ble distribuert i, må representeres i katalogen for vertsleierkatalogen (Azure Active Directory (Azure AD)) slik at de kan tilordnes lisenser.</span><span class="sxs-lookup"><span data-stu-id="e74ad-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="e74ad-111">Disse eksterne brukerne må legges til for leieren i Azure AD som gjestebrukere og deretter tilordnes de aktuelle lisensene.</span><span class="sxs-lookup"><span data-stu-id="e74ad-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="e74ad-112">Hvis du vil ha mer informasjon, kan du se [Legge til Azure Active Directory B2B-samarbeidsbrukere i Azure-portalen](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="e74ad-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="e74ad-113">Legge til en ny bruker</span><span class="sxs-lookup"><span data-stu-id="e74ad-113">Add a new user</span></span>
1. <span data-ttu-id="e74ad-114">Gå til **Systemadministrasjon \> Brukere \> Brukere**.</span><span class="sxs-lookup"><span data-stu-id="e74ad-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="e74ad-115">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e74ad-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="e74ad-116">I **Bruker-ID**-feltet angir du en unik ID for brukeren.</span><span class="sxs-lookup"><span data-stu-id="e74ad-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="e74ad-117">En bruker-ID er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="e74ad-117">A user ID is required.</span></span>  
4. <span data-ttu-id="e74ad-118">Angi navnet på brukeren i **Brukernavn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e74ad-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="e74ad-119">I **Domene**-feltet angir du brukerens domene.</span><span class="sxs-lookup"><span data-stu-id="e74ad-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="e74ad-120">Angi brukerens alias i **Alias**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e74ad-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="e74ad-121">Velg ønsket firma i **Firma**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e74ad-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="e74ad-122">I **Brukerens roller**-hurtigfanen en velger du **Tilordne roller** for å tilordne brukere til sikkerhetsroller.</span><span class="sxs-lookup"><span data-stu-id="e74ad-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="e74ad-123">Hvis du vil ha mer informasjon, kan du se [Tilordne brukere til sikkerhetsroller](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="e74ad-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="e74ad-124">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e74ad-124">Select **OK**.</span></span>
10. <span data-ttu-id="e74ad-125">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e74ad-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="e74ad-126">Importer brukere</span><span class="sxs-lookup"><span data-stu-id="e74ad-126">Import users</span></span>
1. <span data-ttu-id="e74ad-127">Gå til **Systemadministrasjon \> Brukere \> Brukere**.</span><span class="sxs-lookup"><span data-stu-id="e74ad-127">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="e74ad-128">Velg **Importer brukere** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e74ad-128">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="e74ad-129">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e74ad-129">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e74ad-130">Velg **Importer brukere**.</span><span class="sxs-lookup"><span data-stu-id="e74ad-130">Select **Import users**.</span></span>
5. <span data-ttu-id="e74ad-131">Velg **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="e74ad-131">Select **Close**.</span></span>

