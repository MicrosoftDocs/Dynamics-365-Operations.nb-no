--- 
title: " Opprette tillatelsesgrupper for salgssted"
description: Denne prosedyren viser hvordan du oppretter en salgsstedstillatelsesgruppe.
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e924dc59c3e4cb9b6979014852512453dd3d70db
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="6fea6-103"> Opprette tillatelsesgrupper for salgssted</span><span class="sxs-lookup"><span data-stu-id="6fea6-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6fea6-104">Denne prosedyren viser hvordan du oppretter en salgsstedstillatelsesgruppe.</span><span class="sxs-lookup"><span data-stu-id="6fea6-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="6fea6-105">Demonstrasjonsdatafirmaet USRT brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="6fea6-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="6fea6-106">Denne oppgaven er ment for rollen Driftsleder for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="6fea6-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="6fea6-107">Gå til Tillatelsesgrupper.</span><span class="sxs-lookup"><span data-stu-id="6fea6-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="6fea6-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6fea6-108">Click New.</span></span>
3. <span data-ttu-id="6fea6-109">Skriv inn en verdi i feltet ID for salgsstedstillatelsesgruppe.</span><span class="sxs-lookup"><span data-stu-id="6fea6-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="6fea6-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6fea6-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6fea6-111">Velg Ja i feltet Vis tidsklokkeoppføringer.</span><span class="sxs-lookup"><span data-stu-id="6fea6-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="6fea6-112">Nå kan du aktivere eller deaktivere ulike tillatelser for salgsstedstillatelsesgruppen.</span><span class="sxs-lookup"><span data-stu-id="6fea6-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="6fea6-113">For enkelte tillatelser kan du angi en verdi som skal brukes til å vurdere om salgsstedsbrukeren kan utføre handlingen.</span><span class="sxs-lookup"><span data-stu-id="6fea6-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="6fea6-114">Denne oppgaveveiledningen angir noen tillatelser som kan gis til en kasserer.</span><span class="sxs-lookup"><span data-stu-id="6fea6-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="6fea6-115">Velg Ja i feltet Tillat oppretting av ordre.</span><span class="sxs-lookup"><span data-stu-id="6fea6-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="6fea6-116">Velg Ja i feltet Tillat redigering av ordre.</span><span class="sxs-lookup"><span data-stu-id="6fea6-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="6fea6-117">Velg Ja i feltet Tillat oppretting av ordre.</span><span class="sxs-lookup"><span data-stu-id="6fea6-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="6fea6-118">Velg Ja i feltet Tillat passordendring.</span><span class="sxs-lookup"><span data-stu-id="6fea6-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="6fea6-119">Velg Ja i feltet Tillat usporet lukking.</span><span class="sxs-lookup"><span data-stu-id="6fea6-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="6fea6-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6fea6-120">Click Save.</span></span>
    * <span data-ttu-id="6fea6-121">Når endringene er lagret, må du kjøre stabsdistribusjonsplanen for å overføre endringene til detaljhandelskanalene.</span><span class="sxs-lookup"><span data-stu-id="6fea6-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="6fea6-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6fea6-122">Close the page.</span></span>
13. <span data-ttu-id="6fea6-123">Gå til Jobber.</span><span class="sxs-lookup"><span data-stu-id="6fea6-123">Go to Jobs.</span></span>
    * <span data-ttu-id="6fea6-124">Vi vil nå tilordne salgsstedstillatelsesgruppen til en jobb.</span><span class="sxs-lookup"><span data-stu-id="6fea6-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="6fea6-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="6fea6-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="6fea6-126">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6fea6-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="6fea6-127">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="6fea6-127">Click Edit.</span></span>
17. <span data-ttu-id="6fea6-128">Vis delen Jobbklassifisering.</span><span class="sxs-lookup"><span data-stu-id="6fea6-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="6fea6-129">Angi eller velg en verdi i feltet Gruppe for salgsstedstillatelse.</span><span class="sxs-lookup"><span data-stu-id="6fea6-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="6fea6-130">Alle arbeidere i stillinger for denne jobben bruker salgsstedstillatelsesgruppens innstillinger med mindre arbeidernes salgsstedstillatelser har blitt overstyrt på stillingsnivået.</span><span class="sxs-lookup"><span data-stu-id="6fea6-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="6fea6-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6fea6-131">Click Save.</span></span>
    * <span data-ttu-id="6fea6-132">Når endringene er lagret, må du kjøre stabsdistribusjonsplanen for å overføre endringene til detaljhandelskanalene.</span><span class="sxs-lookup"><span data-stu-id="6fea6-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


