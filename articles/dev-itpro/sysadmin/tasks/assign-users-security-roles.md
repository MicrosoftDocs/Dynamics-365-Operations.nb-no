---
title: Tilordne brukere til sikkerhetsroller
description: Brukere må tilordnes sikkerhetsroller for å få tilgang til Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab9f2f5ea07ae1d616c48dffa8810b966f7dbb2f
ms.sourcegitcommit: 33e98f89294086334fe9c0a350abb6a52ef9dacb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/28/2019
ms.locfileid: "1711137"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="b1a91-103">Tilordne brukere til sikkerhetsroller</span><span class="sxs-lookup"><span data-stu-id="b1a91-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1a91-104">Brukere må tilordnes sikkerhetsroller for å få tilgang til Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="b1a91-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="b1a91-105">Denne fremgangsmåten beskriver hvordan systemansvarlige kan tilordne brukere roller automatisk, basert på forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="b1a91-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="b1a91-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="b1a91-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="b1a91-107">Tilordne brukere automatisk til roller</span><span class="sxs-lookup"><span data-stu-id="b1a91-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="b1a91-108">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Tilordne brukere til roller**.</span><span class="sxs-lookup"><span data-stu-id="b1a91-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="b1a91-109">Velg Regnskapsansvarlig i treet.</span><span class="sxs-lookup"><span data-stu-id="b1a91-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="b1a91-110">Velg rollen som du vil konfigurere regelen for.</span><span class="sxs-lookup"><span data-stu-id="b1a91-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="b1a91-111">Velg regnskapsansvarlig i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="b1a91-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="b1a91-112">Klikk på **Legg til regel** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b1a91-112">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="b1a91-113">Finn og velg ønsket post i listen **Velg en spørring**.</span><span class="sxs-lookup"><span data-stu-id="b1a91-113">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="b1a91-114">Velg spørringen som skal brukes for denne regelen.</span><span class="sxs-lookup"><span data-stu-id="b1a91-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="b1a91-115">Klikk på koblingen i den valgte raden i listen **Navn på medlemskapsregel**.</span><span class="sxs-lookup"><span data-stu-id="b1a91-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b1a91-116">Klikk på **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="b1a91-116">Click **Edit query**.</span></span> <span data-ttu-id="b1a91-117">Rediger spørringen etter behov.</span><span class="sxs-lookup"><span data-stu-id="b1a91-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="b1a91-118">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1a91-118">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="b1a91-119">Utelate brukere fra automatisk rolletilordning</span><span class="sxs-lookup"><span data-stu-id="b1a91-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="b1a91-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b1a91-120">Close the page.</span></span>
2. <span data-ttu-id="b1a91-121">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Tilordne brukere til roller**.</span><span class="sxs-lookup"><span data-stu-id="b1a91-121">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="b1a91-122">Velg Regnskapsansvarlig i treet.</span><span class="sxs-lookup"><span data-stu-id="b1a91-122">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="b1a91-123">Velg en rolle.</span><span class="sxs-lookup"><span data-stu-id="b1a91-123">Select a role.</span></span> <span data-ttu-id="b1a91-124">Velg regnskapsansvarlig i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="b1a91-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="b1a91-125">Velg **Tilordne/utelate brukere manuelt** på menyen **Brukere som er tilordnet til rolle**.</span><span class="sxs-lookup"><span data-stu-id="b1a91-125">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="b1a91-126">Merk den valgte raden i listen **Tilordne brukere til, eller utelat brukere fra rolle**.</span><span class="sxs-lookup"><span data-stu-id="b1a91-126">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="b1a91-127">Velg en bruker.</span><span class="sxs-lookup"><span data-stu-id="b1a91-127">Select a user.</span></span>  
6. <span data-ttu-id="b1a91-128">Velg **Utelat fra rolle** i **Handlingsrute**.</span><span class="sxs-lookup"><span data-stu-id="b1a91-128">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="b1a91-129">Klikk på **Utelat fra rolle** for å utelate de valgte brukerne fra rollen.</span><span class="sxs-lookup"><span data-stu-id="b1a91-129">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="b1a91-130">Hvis du vil fjerne utelatelser, velger du brukeren du vil fjerne utelatelser for, og klikker deretter på **Tilbakestill status**.</span><span class="sxs-lookup"><span data-stu-id="b1a91-130">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="b1a91-131">Når du fjerner en utelatelse ved å tilbakestille statusen for brukeren, tilordnes brukerens rolle automatisk på nytt.</span><span class="sxs-lookup"><span data-stu-id="b1a91-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="b1a91-132">Brukeren tilordnes imidlertid ikke umiddelbart rollen eller utelates fra rollen når du tilbakestiller statusen.</span><span class="sxs-lookup"><span data-stu-id="b1a91-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="b1a91-133">I stedet blir brukeren tilordnet rollen eller fjernet fra rollen neste gang reglene for automatisk rolletilordning kjøres.</span><span class="sxs-lookup"><span data-stu-id="b1a91-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
