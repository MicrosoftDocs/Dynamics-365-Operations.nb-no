---
title: Tilordne brukere til sikkerhetsroller
description: Brukere må tilordnes sikkerhetsroller for å få tilgang til Finance and Operations-apper.
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
ms.openlocfilehash: 0744f45ac91dfb9b5aae35091e3675202c9144f9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143563"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="29a14-103">Tilordne brukere til sikkerhetsroller</span><span class="sxs-lookup"><span data-stu-id="29a14-103">Assign users to security roles</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="29a14-104">For å bruke noe annet enn vanlige funksjoner må brukerne tilordnes sikkerhetsroller.</span><span class="sxs-lookup"><span data-stu-id="29a14-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="29a14-105">Denne fremgangsmåten beskriver hvordan systemansvarlige kan tilordne brukere roller automatisk, basert på forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="29a14-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="29a14-106">Tilordne brukere automatisk til roller</span><span class="sxs-lookup"><span data-stu-id="29a14-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="29a14-107">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Tilordne brukere til roller**.</span><span class="sxs-lookup"><span data-stu-id="29a14-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="29a14-108">Velg Regnskapsansvarlig i treet.</span><span class="sxs-lookup"><span data-stu-id="29a14-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="29a14-109">Velg rollen som du vil konfigurere regelen for.</span><span class="sxs-lookup"><span data-stu-id="29a14-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="29a14-110">Velg regnskapsansvarlig i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="29a14-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="29a14-111">Klikk på **Legg til regel** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="29a14-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="29a14-112">Finn og velg ønsket post i listen **Velg en spørring**.</span><span class="sxs-lookup"><span data-stu-id="29a14-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="29a14-113">Velg spørringen som skal brukes for denne regelen.</span><span class="sxs-lookup"><span data-stu-id="29a14-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="29a14-114">Klikk på koblingen i den valgte raden i listen **Navn på medlemskapsregel**.</span><span class="sxs-lookup"><span data-stu-id="29a14-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="29a14-115">Klikk på **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="29a14-115">Click **Edit query**.</span></span> <span data-ttu-id="29a14-116">Rediger spørringen etter behov.</span><span class="sxs-lookup"><span data-stu-id="29a14-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="29a14-117">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="29a14-117">Click **OK**.</span></span>
8. <span data-ttu-id="29a14-118">Klikk på **Kjør automatisk rolletilordning**.</span><span class="sxs-lookup"><span data-stu-id="29a14-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="29a14-119">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Brukere > Brukere** (ideelt i en egen webleserkategori).</span><span class="sxs-lookup"><span data-stu-id="29a14-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="29a14-120">Gå gjennom rollene som er tilordnet ulike brukere for å bekrefte at rolletildelingsspørringen var riktig.</span><span class="sxs-lookup"><span data-stu-id="29a14-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="29a14-121">Juster og kjør på nytt om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="29a14-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="29a14-122">Utelate brukere fra automatisk rolletilordning</span><span class="sxs-lookup"><span data-stu-id="29a14-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="29a14-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="29a14-123">Close the page.</span></span>
2. <span data-ttu-id="29a14-124">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Tilordne brukere til roller**.</span><span class="sxs-lookup"><span data-stu-id="29a14-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="29a14-125">Velg Regnskapsansvarlig i treet.</span><span class="sxs-lookup"><span data-stu-id="29a14-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="29a14-126">Velg en rolle.</span><span class="sxs-lookup"><span data-stu-id="29a14-126">Select a role.</span></span> <span data-ttu-id="29a14-127">Velg regnskapsansvarlig i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="29a14-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="29a14-128">Velg **Tilordne/utelate brukere manuelt** på menyen **Brukere som er tilordnet til rolle**.</span><span class="sxs-lookup"><span data-stu-id="29a14-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="29a14-129">Merk den valgte raden i listen **Tilordne brukere til, eller utelat brukere fra rolle**.</span><span class="sxs-lookup"><span data-stu-id="29a14-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="29a14-130">Velg en bruker.</span><span class="sxs-lookup"><span data-stu-id="29a14-130">Select a user.</span></span>  
6. <span data-ttu-id="29a14-131">Velg **Utelat fra rolle** i **Handlingsrute**.</span><span class="sxs-lookup"><span data-stu-id="29a14-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="29a14-132">Klikk på **Utelat fra rolle** for å utelate de valgte brukerne fra rollen.</span><span class="sxs-lookup"><span data-stu-id="29a14-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="29a14-133">Hvis du vil fjerne utelatelser, velger du brukeren du vil fjerne utelatelser for, og klikker deretter på **Tilbakestill status**.</span><span class="sxs-lookup"><span data-stu-id="29a14-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="29a14-134">Når du fjerner en utelatelse ved å tilbakestille statusen for brukeren, tilordnes brukerens rolle automatisk på nytt.</span><span class="sxs-lookup"><span data-stu-id="29a14-134">When you remove an exclusion by resetting the user's status, the user's role is again assigned automatically.</span></span> <span data-ttu-id="29a14-135">Brukeren tilordnes imidlertid ikke umiddelbart rollen eller utelates fra rollen når du tilbakestiller statusen.</span><span class="sxs-lookup"><span data-stu-id="29a14-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="29a14-136">I stedet blir brukeren tilordnet rollen eller fjernet fra rollen neste gang reglene for automatisk rolletilordning kjøres.</span><span class="sxs-lookup"><span data-stu-id="29a14-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
