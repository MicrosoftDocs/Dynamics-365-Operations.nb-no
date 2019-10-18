---
title: Tilordne brukere til sikkerhetsroller
description: For å få tilgang til Finance and Operations-apper må brukere tilordnes sikkerhetsroller.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
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
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180973"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="0657c-103">Tilordne brukere til sikkerhetsroller</span><span class="sxs-lookup"><span data-stu-id="0657c-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0657c-104">For å bruke noe annet enn vanlige funksjoner må brukerne tilordnes sikkerhetsroller.</span><span class="sxs-lookup"><span data-stu-id="0657c-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="0657c-105">Denne fremgangsmåten beskriver hvordan systemansvarlige kan tilordne brukere roller automatisk, basert på forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="0657c-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="0657c-106">Tilordne brukere automatisk til roller</span><span class="sxs-lookup"><span data-stu-id="0657c-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="0657c-107">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Tilordne brukere til roller**.</span><span class="sxs-lookup"><span data-stu-id="0657c-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="0657c-108">Velg Regnskapsansvarlig i treet.</span><span class="sxs-lookup"><span data-stu-id="0657c-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="0657c-109">Velg rollen som du vil konfigurere regelen for.</span><span class="sxs-lookup"><span data-stu-id="0657c-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="0657c-110">Velg regnskapsansvarlig i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="0657c-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="0657c-111">Klikk på **Legg til regel** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="0657c-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="0657c-112">Finn og velg ønsket post i listen **Velg en spørring**.</span><span class="sxs-lookup"><span data-stu-id="0657c-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="0657c-113">Velg spørringen som skal brukes for denne regelen.</span><span class="sxs-lookup"><span data-stu-id="0657c-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="0657c-114">Klikk på koblingen i den valgte raden i listen **Navn på medlemskapsregel**.</span><span class="sxs-lookup"><span data-stu-id="0657c-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0657c-115">Klikk på **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="0657c-115">Click **Edit query**.</span></span> <span data-ttu-id="0657c-116">Rediger spørringen etter behov.</span><span class="sxs-lookup"><span data-stu-id="0657c-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="0657c-117">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="0657c-117">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="0657c-118">Utelate brukere fra automatisk rolletilordning</span><span class="sxs-lookup"><span data-stu-id="0657c-118">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="0657c-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0657c-119">Close the page.</span></span>
2. <span data-ttu-id="0657c-120">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Tilordne brukere til roller**.</span><span class="sxs-lookup"><span data-stu-id="0657c-120">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="0657c-121">Velg Regnskapsansvarlig i treet.</span><span class="sxs-lookup"><span data-stu-id="0657c-121">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="0657c-122">Velg en rolle.</span><span class="sxs-lookup"><span data-stu-id="0657c-122">Select a role.</span></span> <span data-ttu-id="0657c-123">Velg regnskapsansvarlig i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="0657c-123">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="0657c-124">Velg **Tilordne/utelate brukere manuelt** på menyen **Brukere som er tilordnet til rolle**.</span><span class="sxs-lookup"><span data-stu-id="0657c-124">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="0657c-125">Merk den valgte raden i listen **Tilordne brukere til, eller utelat brukere fra rolle**.</span><span class="sxs-lookup"><span data-stu-id="0657c-125">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="0657c-126">Velg en bruker.</span><span class="sxs-lookup"><span data-stu-id="0657c-126">Select a user.</span></span>  
6. <span data-ttu-id="0657c-127">Velg **Utelat fra rolle** i **Handlingsrute**.</span><span class="sxs-lookup"><span data-stu-id="0657c-127">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="0657c-128">Klikk på **Utelat fra rolle** for å utelate de valgte brukerne fra rollen.</span><span class="sxs-lookup"><span data-stu-id="0657c-128">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="0657c-129">Hvis du vil fjerne utelatelser, velger du brukeren du vil fjerne utelatelser for, og klikker deretter på **Tilbakestill status**.</span><span class="sxs-lookup"><span data-stu-id="0657c-129">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="0657c-130">Når du fjerner en utelatelse ved å tilbakestille statusen for brukeren, tilordnes brukerens rolle automatisk på nytt.</span><span class="sxs-lookup"><span data-stu-id="0657c-130">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="0657c-131">Brukeren tilordnes imidlertid ikke umiddelbart rollen eller utelates fra rollen når du tilbakestiller statusen.</span><span class="sxs-lookup"><span data-stu-id="0657c-131">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="0657c-132">I stedet blir brukeren tilordnet rollen eller fjernet fra rollen neste gang reglene for automatisk rolletilordning kjøres.</span><span class="sxs-lookup"><span data-stu-id="0657c-132">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
