---
title: Opprette tillatelsesgrupper for salgssted
description: Dette emnet forklarer hvordan du oppretter en salgsstedstillatelsesgruppe.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ffc64fd39a390af3ca7110178ef0999527106dc
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141390"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="6899e-103">Opprette tillatelsesgrupper for salgssted</span><span class="sxs-lookup"><span data-stu-id="6899e-103">Create POS permission groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6899e-104">Dette emnet forklarer hvordan du oppretter en salgsstedstillatelsesgruppe.</span><span class="sxs-lookup"><span data-stu-id="6899e-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="6899e-105">Demonstrasjonsdatafirmaet USRT brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="6899e-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="6899e-106">Denne oppgaven er ment for rollen Driftsleder for handel.</span><span class="sxs-lookup"><span data-stu-id="6899e-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="6899e-107">I navigasjonsruten går du til **Moduler > Detaljhandel og handel > Ansatte > Tillatelsesgrupper**.</span><span class="sxs-lookup"><span data-stu-id="6899e-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="6899e-108">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6899e-108">Select **New**.</span></span>
3. <span data-ttu-id="6899e-109">Skriv inn en verdi i feltet **ID for salgsstedstillatelsesgruppe**.</span><span class="sxs-lookup"><span data-stu-id="6899e-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="6899e-110">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6899e-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="6899e-111">Velg **Ja** i feltet **Vis tidsklokkeoppføringer**.</span><span class="sxs-lookup"><span data-stu-id="6899e-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="6899e-112">Nå kan du aktivere eller deaktivere ulike tillatelser for salgsstedstillatelsesgruppen.</span><span class="sxs-lookup"><span data-stu-id="6899e-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="6899e-113">For enkelte tillatelser kan du angi en verdi som skal brukes til å vurdere om salgsstedsbrukeren kan utføre handlingen.</span><span class="sxs-lookup"><span data-stu-id="6899e-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="6899e-114">Denne oppgaveveiledningen angir noen tillatelser som kan gis til en kasserer.</span><span class="sxs-lookup"><span data-stu-id="6899e-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="6899e-115">Velg **Ja** i feltet **Tillat oppretting av ordre**.</span><span class="sxs-lookup"><span data-stu-id="6899e-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="6899e-116">Velg **Ja** i feltet **Tillat redigering av ordre**.</span><span class="sxs-lookup"><span data-stu-id="6899e-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="6899e-117">Velg **Ja** i feltet **Tillat oppretting av ordre**.</span><span class="sxs-lookup"><span data-stu-id="6899e-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="6899e-118">Velg **Ja** i feltet **Tillat passordendring**.</span><span class="sxs-lookup"><span data-stu-id="6899e-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="6899e-119">Velg **Ja** i feltet **Tillat usporet lukking**.</span><span class="sxs-lookup"><span data-stu-id="6899e-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="6899e-120">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6899e-120">Select **Save**.</span></span> <span data-ttu-id="6899e-121">Når endringene er lagret, må du kjøre stabsdistribusjonsplanen for å overføre endringene til handelskanalene.</span><span class="sxs-lookup"><span data-stu-id="6899e-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="6899e-122">I navigasjonsruten går du til **Moduler > Personale > Jobber > Jobber**.</span><span class="sxs-lookup"><span data-stu-id="6899e-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="6899e-123">Vi vil nå tilordne salgsstedstillatelsesgruppen til en jobb.</span><span class="sxs-lookup"><span data-stu-id="6899e-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="6899e-124">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="6899e-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="6899e-125">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="6899e-125">Select **Edit**.</span></span>
15. <span data-ttu-id="6899e-126">Vis delen **Jobbklassifisering**.</span><span class="sxs-lookup"><span data-stu-id="6899e-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="6899e-127">Angi eller velg en verdi i feltet Gruppe for salgsstedstillatelse.</span><span class="sxs-lookup"><span data-stu-id="6899e-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="6899e-128">Alle arbeidere i stillinger for denne jobben bruker salgsstedstillatelsesgruppens innstillinger med mindre arbeidernes salgsstedstillatelser har blitt overstyrt på stillingsnivået.</span><span class="sxs-lookup"><span data-stu-id="6899e-128">All Workers in Positions for this Job will use this POS permission group's settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="6899e-129">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6899e-129">Select **Save**.</span></span> <span data-ttu-id="6899e-130">Når endringene er lagret, må du kjøre stabsdistribusjonsplanen for å overføre endringene til handelskanalene.</span><span class="sxs-lookup"><span data-stu-id="6899e-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  

