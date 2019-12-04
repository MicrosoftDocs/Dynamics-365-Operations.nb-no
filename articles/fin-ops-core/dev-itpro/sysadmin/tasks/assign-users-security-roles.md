---
title: Tilordne brukere til sikkerhetsroller
description: For å få tilgang til Finance and Operations-apper må brukere tilordnes sikkerhetsroller.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4f4ef4535de9e371829c2d86d4fdc1400510c7b
ms.sourcegitcommit: 6aa74f66f1abd3a7977050a5339b0b17e62ff053
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/15/2019
ms.locfileid: "2808002"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="6ef52-103">Tilordne brukere til sikkerhetsroller</span><span class="sxs-lookup"><span data-stu-id="6ef52-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ef52-104">For å bruke noe annet enn vanlige funksjoner må brukerne tilordnes sikkerhetsroller.</span><span class="sxs-lookup"><span data-stu-id="6ef52-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="6ef52-105">Denne fremgangsmåten beskriver hvordan systemansvarlige kan tilordne brukere roller automatisk, basert på forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="6ef52-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="6ef52-106">Tilordne brukere automatisk til roller</span><span class="sxs-lookup"><span data-stu-id="6ef52-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="6ef52-107">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Tilordne brukere til roller**.</span><span class="sxs-lookup"><span data-stu-id="6ef52-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="6ef52-108">Velg Regnskapsansvarlig i treet.</span><span class="sxs-lookup"><span data-stu-id="6ef52-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="6ef52-109">Velg rollen som du vil konfigurere regelen for.</span><span class="sxs-lookup"><span data-stu-id="6ef52-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="6ef52-110">Velg regnskapsansvarlig i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="6ef52-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="6ef52-111">Klikk på **Legg til regel** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6ef52-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="6ef52-112">Finn og velg ønsket post i listen **Velg en spørring**.</span><span class="sxs-lookup"><span data-stu-id="6ef52-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="6ef52-113">Velg spørringen som skal brukes for denne regelen.</span><span class="sxs-lookup"><span data-stu-id="6ef52-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="6ef52-114">Klikk på koblingen i den valgte raden i listen **Navn på medlemskapsregel**.</span><span class="sxs-lookup"><span data-stu-id="6ef52-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6ef52-115">Klikk på **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="6ef52-115">Click **Edit query**.</span></span> <span data-ttu-id="6ef52-116">Rediger spørringen etter behov.</span><span class="sxs-lookup"><span data-stu-id="6ef52-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="6ef52-117">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ef52-117">Click **OK**.</span></span>
8. <span data-ttu-id="6ef52-118">Klikk på **Kjør automatisk rolletilordning**.</span><span class="sxs-lookup"><span data-stu-id="6ef52-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="6ef52-119">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Brukere > Brukere** (ideelt i en egen webleserkategori).</span><span class="sxs-lookup"><span data-stu-id="6ef52-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="6ef52-120">Gå gjennom rollene som er tilordnet ulike brukere for å bekrefte at rolletildelingsspørringen var riktig.</span><span class="sxs-lookup"><span data-stu-id="6ef52-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="6ef52-121">Juster og kjør på nytt om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="6ef52-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="6ef52-122">Utelate brukere fra automatisk rolletilordning</span><span class="sxs-lookup"><span data-stu-id="6ef52-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="6ef52-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6ef52-123">Close the page.</span></span>
2. <span data-ttu-id="6ef52-124">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Tilordne brukere til roller**.</span><span class="sxs-lookup"><span data-stu-id="6ef52-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="6ef52-125">Velg Regnskapsansvarlig i treet.</span><span class="sxs-lookup"><span data-stu-id="6ef52-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="6ef52-126">Velg en rolle.</span><span class="sxs-lookup"><span data-stu-id="6ef52-126">Select a role.</span></span> <span data-ttu-id="6ef52-127">Velg regnskapsansvarlig i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="6ef52-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="6ef52-128">Velg **Tilordne/utelate brukere manuelt** på menyen **Brukere som er tilordnet til rolle**.</span><span class="sxs-lookup"><span data-stu-id="6ef52-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="6ef52-129">Merk den valgte raden i listen **Tilordne brukere til, eller utelat brukere fra rolle**.</span><span class="sxs-lookup"><span data-stu-id="6ef52-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="6ef52-130">Velg en bruker.</span><span class="sxs-lookup"><span data-stu-id="6ef52-130">Select a user.</span></span>  
6. <span data-ttu-id="6ef52-131">Velg **Utelat fra rolle** i **Handlingsrute**.</span><span class="sxs-lookup"><span data-stu-id="6ef52-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="6ef52-132">Klikk på **Utelat fra rolle** for å utelate de valgte brukerne fra rollen.</span><span class="sxs-lookup"><span data-stu-id="6ef52-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="6ef52-133">Hvis du vil fjerne utelatelser, velger du brukeren du vil fjerne utelatelser for, og klikker deretter på **Tilbakestill status**.</span><span class="sxs-lookup"><span data-stu-id="6ef52-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="6ef52-134">Når du fjerner en utelatelse ved å tilbakestille statusen for brukeren, tilordnes brukerens rolle automatisk på nytt.</span><span class="sxs-lookup"><span data-stu-id="6ef52-134">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="6ef52-135">Brukeren tilordnes imidlertid ikke umiddelbart rollen eller utelates fra rollen når du tilbakestiller statusen.</span><span class="sxs-lookup"><span data-stu-id="6ef52-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="6ef52-136">I stedet blir brukeren tilordnet rollen eller fjernet fra rollen neste gang reglene for automatisk rolletilordning kjøres.</span><span class="sxs-lookup"><span data-stu-id="6ef52-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
