---
title: Tilordne brukere til sikkerhetsroller
description: Brukere må tilordnes sikkerhetsroller for å få tilgang til Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556715"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="ba1c6-103">Tilordne brukere til sikkerhetsroller</span><span class="sxs-lookup"><span data-stu-id="ba1c6-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ba1c6-104">Brukere må tilordnes sikkerhetsroller for å få tilgang til Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="ba1c6-105">Denne fremgangsmåten beskriver hvordan systemansvarlige kan tilordne brukere roller automatisk, basert på forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="ba1c6-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="ba1c6-107">Tilordne brukere automatisk til roller</span><span class="sxs-lookup"><span data-stu-id="ba1c6-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="ba1c6-108">Gå til Systemadministrasjon > Sikkerhet > Tilordne brukere til roller.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="ba1c6-109">Velg Regnskapsansvarlig i treet.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="ba1c6-110">Velg rollen som du vil konfigurere regelen for.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="ba1c6-111">Velg regnskapsansvarlig i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="ba1c6-112">Klikk Legg til regel for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="ba1c6-113">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ba1c6-114">Velg spørringen som skal brukes for denne regelen.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="ba1c6-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ba1c6-116">Klikk Rediger spørring.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-116">Click Edit query.</span></span>
    * <span data-ttu-id="ba1c6-117">Rediger spørringen etter behov.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="ba1c6-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="ba1c6-119">Utelate brukere fra automatisk rolletilordning</span><span class="sxs-lookup"><span data-stu-id="ba1c6-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="ba1c6-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-120">Close the page.</span></span>
2. <span data-ttu-id="ba1c6-121">Gå til Systemadministrasjon > Sikkerhet > Tilordne brukere til roller.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="ba1c6-122">Velg Regnskapsansvarlig i treet.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="ba1c6-123">Velg en rolle.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-123">Select a role.</span></span> <span data-ttu-id="ba1c6-124">Velg regnskapsansvarlig i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="ba1c6-125">Klikk Tilordne/utelate brukere manuelt.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="ba1c6-126">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ba1c6-127">Velg en bruker.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-127">Select a user.</span></span>  
6. <span data-ttu-id="ba1c6-128">Klikk Utelat fra rolle.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="ba1c6-129">Klikk Utelat fra rolle for å utelate de valgte brukerne fra rollen.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="ba1c6-130">Hvis du vil fjerne utelatelser, velger du brukeren du vil fjerne utelatelser for og klikker deretter Tilbakestill status.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="ba1c6-131">Når du fjerner en utelatelse ved å tilbakestille statusen for brukeren, tilordnes brukerens rolle automatisk på nytt.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="ba1c6-132">Brukeren tilordnes imidlertid ikke umiddelbart rollen eller utelates fra rollen når du tilbakestiller statusen.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="ba1c6-133">I stedet blir brukeren tilordnet rollen eller fjernet fra rollen neste gang reglene for automatisk rolletilordning kjøres.</span><span class="sxs-lookup"><span data-stu-id="ba1c6-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

