---
title: Konfigurer stillinger
description: Stillinger er et viktig element i det nederste nivået i et organisasjonshierarki.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmWorkforceWorkspace, HcmWorkerActivityChart, HcmAllWorkersListPart, HcmPosition, HcmPositionNewPosition, HcmJobLookup, HcmPositionReportsToDialog, HcmPositionLookup, FinancialDimensionDefaultTemplatesLookup, DimensionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fd355fb6c3d2742e046a616585ca349c623341d
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "856836"
---
# <a name="set-up-positions"></a><span data-ttu-id="455d6-103">Konfigurer stillinger</span><span class="sxs-lookup"><span data-stu-id="455d6-103">Set up positions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="455d6-104">Stillinger er et viktig element i det nederste nivået i et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="455d6-104">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="455d6-105">En stilling er én enkeltforekomst av en jobb.</span><span class="sxs-lookup"><span data-stu-id="455d6-105">A position is an individual instance of a job.</span></span> <span data-ttu-id="455d6-106">Stillingen "Salgssjef (øst)" er for eksempel én av stillingene som er knyttet til jobben "Salgssjef".</span><span class="sxs-lookup"><span data-stu-id="455d6-106">For example, the position, “Sales manager (East),” is one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="455d6-107">Det finnes en stilling i en avdeling, og bare én arbeider kan tilordnes den.</span><span class="sxs-lookup"><span data-stu-id="455d6-107">A position exists in a department and may have only one worker associated with it.</span></span> <span data-ttu-id="455d6-108">I denne oppgaven vil vi veilede deg gjennom fremgangsmåten som kreves for å opprette en stilling.</span><span class="sxs-lookup"><span data-stu-id="455d6-108">In this task we will walk through the steps required to create a position.</span></span> <span data-ttu-id="455d6-109">Denne fremgangsmåten er ment for en personalespesialister.</span><span class="sxs-lookup"><span data-stu-id="455d6-109">This procedure is intended for Human Resources Specialists.</span></span>

1. <span data-ttu-id="455d6-110">Klikk Administrasjon av arbeidsstyrke.</span><span class="sxs-lookup"><span data-stu-id="455d6-110">Click Workforce management.</span></span>
2. <span data-ttu-id="455d6-111">Klikk Åpne stillinger.</span><span class="sxs-lookup"><span data-stu-id="455d6-111">Click Open positions.</span></span>
3. <span data-ttu-id="455d6-112">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="455d6-112">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="455d6-113">Angi eller velg en verdi i Jobb-feltet.</span><span class="sxs-lookup"><span data-stu-id="455d6-113">In the Job field, enter or select a value.</span></span>
    * <span data-ttu-id="455d6-114">Jobbeskrivelsen, tittelen og omregningsfaktoren for fulltidsekvivalent kopieres automatisk fra den valgte jobben til stillingen.</span><span class="sxs-lookup"><span data-stu-id="455d6-114">The Job description, title, and full-time equivalent employment factor are automatically copied from the selected job into the position.</span></span>  
5. <span data-ttu-id="455d6-115">ResolveChanges jobben.</span><span class="sxs-lookup"><span data-stu-id="455d6-115">ResolveChanges the Job.</span></span>
6. <span data-ttu-id="455d6-116">Klikk Opprett stilling.</span><span class="sxs-lookup"><span data-stu-id="455d6-116">Click Create position.</span></span>
7. <span data-ttu-id="455d6-117">Angi eller velg en verdi i feltet Avdeling.</span><span class="sxs-lookup"><span data-stu-id="455d6-117">In the Department field, enter or select a value.</span></span>
8. <span data-ttu-id="455d6-118">Angi eller velg en verdi i feltet Stillingstype.</span><span class="sxs-lookup"><span data-stu-id="455d6-118">In the Position type field, enter or select a value.</span></span>
9. <span data-ttu-id="455d6-119">Angi eller velg en verdi i feltet Kompensasjonsområde.</span><span class="sxs-lookup"><span data-stu-id="455d6-119">In the Compensation region field, enter or select a value.</span></span>
    * <span data-ttu-id="455d6-120">Feltet Kompensasjonsområde bestemmer rettighetsreglene for kompensasjonen og budsjetter med fast økning som gjelder for en ansatt i denne stillingen.</span><span class="sxs-lookup"><span data-stu-id="455d6-120">The Compensation region field determines the compensation eligibility rules and fixed increase budgets that apply to an employee in that position.</span></span>  
10. <span data-ttu-id="455d6-121">Angi en dato og et klokkeslett i feltet Tilgjengelig for tilordning.</span><span class="sxs-lookup"><span data-stu-id="455d6-121">In the Available for assignment field, enter a date and time.</span></span>
11. <span data-ttu-id="455d6-122">Vis delen Stillingsvarighet.</span><span class="sxs-lookup"><span data-stu-id="455d6-122">Expand the Position duration section.</span></span>
    * <span data-ttu-id="455d6-123">Stillingsvarighet angis som standard basert på datoene for aktivering og avgang ved pensjon, som ble angitt tidligere</span><span class="sxs-lookup"><span data-stu-id="455d6-123">Position duration is entered by default based on activation and retirement dates entered earlier</span></span>  
12. <span data-ttu-id="455d6-124">Utvid delen Rapporterer til stilling.</span><span class="sxs-lookup"><span data-stu-id="455d6-124">Expand the Reports to position section.</span></span>
    * <span data-ttu-id="455d6-125">Når du tilordner en arbeider til en stilling som rapporterer til en annen stilling, oppretter du en direkterapporteringsrelasjon mellom arbeidere som er tilordnet de to stillingene.</span><span class="sxs-lookup"><span data-stu-id="455d6-125">When you assign a worker to a position that reports to another position, you create a direct reporting relationship between the workers who are assigned to the two positions.</span></span>  
13. <span data-ttu-id="455d6-126">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="455d6-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="455d6-127">Angi eller velg en verdi i feltet Rapporter til.</span><span class="sxs-lookup"><span data-stu-id="455d6-127">In the Reports to field, enter or select a value.</span></span>
15. <span data-ttu-id="455d6-128">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="455d6-128">Click Create.</span></span>
16. <span data-ttu-id="455d6-129">Vis delen Arbeidertilordning.</span><span class="sxs-lookup"><span data-stu-id="455d6-129">Expand the Worker assignment section.</span></span>
17. <span data-ttu-id="455d6-130">Vis delen Relasjoner.</span><span class="sxs-lookup"><span data-stu-id="455d6-130">Expand the Relationships section.</span></span>
    * <span data-ttu-id="455d6-131">Hvis organisasjonen bruker et matrisehierarki eller et annet egendefinert hierarki, kan du konfigurere stillingshierarkityper og deretter legge til rapporteringsrelasjoner i stillinger for hver hierarkitype som du definerer.</span><span class="sxs-lookup"><span data-stu-id="455d6-131">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span>  
18. <span data-ttu-id="455d6-132">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="455d6-132">Click Add.</span></span>
19. <span data-ttu-id="455d6-133">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="455d6-133">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="455d6-134">Angi eller velg en verdi i feltet Navn på hierarki.</span><span class="sxs-lookup"><span data-stu-id="455d6-134">In the Hierarchy name field, enter or select a value.</span></span>
21. <span data-ttu-id="455d6-135">Angi eller velg en verdi i feltet Rapporterer til stilling.</span><span class="sxs-lookup"><span data-stu-id="455d6-135">In the Reports to position field, enter or select a value.</span></span>
22. <span data-ttu-id="455d6-136">Vis delen Lønn.</span><span class="sxs-lookup"><span data-stu-id="455d6-136">Expand the Payroll section.</span></span>
23. <span data-ttu-id="455d6-137">Angi eller velg en verdi i feltet Lønnssyklus.</span><span class="sxs-lookup"><span data-stu-id="455d6-137">In the Pay cycle field, enter or select a value.</span></span>
24. <span data-ttu-id="455d6-138">Angi eller velg en verdi i feltet Betalt av.</span><span class="sxs-lookup"><span data-stu-id="455d6-138">In the Paid by field, enter or select a value.</span></span>
25. <span data-ttu-id="455d6-139">Angi et tall i feltet Årlige vanlige timer.</span><span class="sxs-lookup"><span data-stu-id="455d6-139">In the Annual regular hours field, enter a number.</span></span>
    * <span data-ttu-id="455d6-140">Dette er antall regelmessig betalte timer som arbeideren i denne stillingen er forventet å arbeide hvert år.</span><span class="sxs-lookup"><span data-stu-id="455d6-140">This is the number of regularly paid hours that the worker in this position is expected to work each year.</span></span>  
26. <span data-ttu-id="455d6-141">Vis delen Fagforening.</span><span class="sxs-lookup"><span data-stu-id="455d6-141">Expand the Labor union section.</span></span>
27. <span data-ttu-id="455d6-142">Skjul delen Fagforening.</span><span class="sxs-lookup"><span data-stu-id="455d6-142">Collapse the Labor union section.</span></span>
28. <span data-ttu-id="455d6-143">Vis delen Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="455d6-143">Expand the Financial dimensions section.</span></span>
29. <span data-ttu-id="455d6-144">Angi eller velg en verdi i feltet Distribusjonsmal.</span><span class="sxs-lookup"><span data-stu-id="455d6-144">In the Distribution template field, enter or select a value.</span></span>
30. <span data-ttu-id="455d6-145">Angi eller velg en verdi i feltet Avdeling.</span><span class="sxs-lookup"><span data-stu-id="455d6-145">In the Department field, enter or select a value.</span></span>
31. <span data-ttu-id="455d6-146">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="455d6-146">Click Save.</span></span>

