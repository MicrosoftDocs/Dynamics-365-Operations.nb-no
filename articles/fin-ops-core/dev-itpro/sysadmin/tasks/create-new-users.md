---
title: Opprette nye brukere
description: Brukere er interne ansatte i din organisasjon, eller eksterne kunder og leverandører, som trenger tilgang til systemet for å utføre jobbene sine.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
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
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570527"
---
# <a name="create-new-users"></a><span data-ttu-id="034ad-103">Opprette nye brukere</span><span class="sxs-lookup"><span data-stu-id="034ad-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="034ad-104">Brukere er interne ansatte i din organisasjon, eller eksterne kunder og leverandører, som trenger tilgang til systemet for å utføre jobbene sine.</span><span class="sxs-lookup"><span data-stu-id="034ad-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="034ad-105">Knytte en bruker til en lisens (bare nye lisenstyper)</span><span class="sxs-lookup"><span data-stu-id="034ad-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="034ad-106">For kunder som har én av de nye lisenstypene som ble lagt til i oktober 2019, må brukere være knyttet til en lisens.</span><span class="sxs-lookup"><span data-stu-id="034ad-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="034ad-107">Brukere som er knyttet til en lisens, legges automatisk til som systembrukere som ikke har noen roller første gang de logger på.</span><span class="sxs-lookup"><span data-stu-id="034ad-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="034ad-108">Brukere som ikke er knyttet til en lisens, får en advarsel.</span><span class="sxs-lookup"><span data-stu-id="034ad-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="034ad-109">Systemadministratorer kan [tilordne lisenser til brukere](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) i [administrasjonssenteret for Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="034ad-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="034ad-110">Legge til en ny bruker</span><span class="sxs-lookup"><span data-stu-id="034ad-110">Add a new user</span></span>
1. <span data-ttu-id="034ad-111">Gå til **Systemadministrasjon \> Brukere \> Brukere**.</span><span class="sxs-lookup"><span data-stu-id="034ad-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="034ad-112">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="034ad-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="034ad-113">I **Bruker-ID**-feltet angir du en unik ID for brukeren.</span><span class="sxs-lookup"><span data-stu-id="034ad-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="034ad-114">En bruker-ID er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="034ad-114">A user ID is required.</span></span>  
4. <span data-ttu-id="034ad-115">Angi navnet på brukeren i **Brukernavn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="034ad-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="034ad-116">I **Domene**-feltet angir du brukerens domene.</span><span class="sxs-lookup"><span data-stu-id="034ad-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="034ad-117">Angi brukerens alias i **Alias**-feltet.</span><span class="sxs-lookup"><span data-stu-id="034ad-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="034ad-118">Velg ønsket firma i **Firma**-feltet.</span><span class="sxs-lookup"><span data-stu-id="034ad-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="034ad-119">Velg **Tilordne roller** i hurtigfanen **Brukerroller** for å [tilordne brukere til sikkerhetsroller](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="034ad-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="034ad-120">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="034ad-120">Select **OK**.</span></span>
10. <span data-ttu-id="034ad-121">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="034ad-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="034ad-122">Importer brukere</span><span class="sxs-lookup"><span data-stu-id="034ad-122">Import users</span></span>
1. <span data-ttu-id="034ad-123">Velg **Importer brukere** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="034ad-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="034ad-124">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="034ad-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="034ad-125">Velg **Importer brukere**.</span><span class="sxs-lookup"><span data-stu-id="034ad-125">Select **Import users**.</span></span>
4. <span data-ttu-id="034ad-126">Velg **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="034ad-126">Select **Close**.</span></span>

