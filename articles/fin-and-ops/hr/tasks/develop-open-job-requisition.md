---
title: Utvikle og åpne jobbrekvisisjon
description: Rekrutteringsprosjekter hjelper deg med å administrere rekrutteringsprosessen.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMRecruitingTable, HcmWorkerLookUp, HcmJobLookup, HRMRecruitingMedia, HRMRecruitingJobAd
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 556f99d34521cce70efb64c5fbababd815e8429d
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "857367"
---
# <a name="develop-and-open-job-requisition"></a><span data-ttu-id="15010-103">Utvikle og åpne jobbrekvisisjon</span><span class="sxs-lookup"><span data-stu-id="15010-103">Develop and open job requisition</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="15010-104">Rekrutteringsprosjekter hjelper deg med å administrere rekrutteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="15010-104">Recruitment projects help manage the recruiting process.</span></span> <span data-ttu-id="15010-105">For hvert rekrutteringsprosjekt kan du definere informasjon, for eksempel jobben rekrutteringen gjelder for, navnet på rekruttereren, statusen for prosjektet og avdelingen der jobben er lokalisert.</span><span class="sxs-lookup"><span data-stu-id="15010-105">For each recruitment project, you can set up information, such as the job that recruiting is for, the name of the recruiter, the status of the project and the department that the job will be located in.</span></span> <span data-ttu-id="15010-106">Når du har opprettet et rekrutteringsprosjekt, kan du skrive en stillingsannonse for prosjektet, publisere annonsen på ansattselvbetjeningssider, knytte søknader om ansettelse til prosjektet og spore aktiviteter for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="15010-106">After creating a recruitment project, you can write a job advertisement for the project, publish the ad on Employee self-service pages, associate applications for employment with the project, and track activities for that project.</span></span> <span data-ttu-id="15010-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="15010-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="15010-108">Hvis du vil starte fremgangsmåten, kan du gå til Personale > Rekruttering > Rekrutteringsprosjekter > Rekrutteringsprosjekter</span><span class="sxs-lookup"><span data-stu-id="15010-108">To begin the procedure, go to Human resources > Recruitment > Recruitment projects > Recruitment projects</span></span>

1. <span data-ttu-id="15010-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="15010-109">Click New.</span></span>
2. <span data-ttu-id="15010-110">Skriv inn en verdi i Rekrutteringsprosjekt-feltet.</span><span class="sxs-lookup"><span data-stu-id="15010-110">In the Recruitment project field, type a value.</span></span>
3. <span data-ttu-id="15010-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="15010-111">In the Description field, type a value.</span></span>
4. <span data-ttu-id="15010-112">Klikk rullegardinknappen i Rekrutter-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="15010-112">In the Recruiter field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="15010-113">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="15010-113">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="15010-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="15010-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="15010-115">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="15010-115">Click Select.</span></span>
8. <span data-ttu-id="15010-116">Klikk rullegardinknappen i Avdeling-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="15010-116">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="15010-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="15010-117">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="15010-118">Klikk rullegardinknappen i Jobb-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="15010-118">In the Job field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="15010-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="15010-119">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="15010-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="15010-120">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="15010-121">Angi et tall i feltet Antall ledige stillinger.</span><span class="sxs-lookup"><span data-stu-id="15010-121">In the Number of openings field, enter a number.</span></span>
14. <span data-ttu-id="15010-122">Klikk rullegardinknappen i Ansettelsesansvarlig-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="15010-122">In the Hiring manager field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="15010-123">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="15010-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="15010-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="15010-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="15010-125">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="15010-125">Click Select.</span></span>
18. <span data-ttu-id="15010-126">Angi en dato i Søknadsfrist-feltet.</span><span class="sxs-lookup"><span data-stu-id="15010-126">In the Application deadline field, enter a date.</span></span>
19. <span data-ttu-id="15010-127">Klikk Medier.</span><span class="sxs-lookup"><span data-stu-id="15010-127">Click Media.</span></span>
    * <span data-ttu-id="15010-128">Rekrutteringsprosjekter inkluderer muligheten til å angi mediekanaler som skal brukes til å annonsere ledige stillinger.</span><span class="sxs-lookup"><span data-stu-id="15010-128">Recruitment projects include the option to specify media outlets to use to advertise open positions.</span></span>  
20. <span data-ttu-id="15010-129">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="15010-129">Click New.</span></span>
21. <span data-ttu-id="15010-130">Klikk rullegardinknappen i Medier-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="15010-130">In the Media field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="15010-131">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="15010-131">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="15010-132">Angi en dato i Startdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="15010-132">In the Start date field, enter a date.</span></span>
24. <span data-ttu-id="15010-133">Angi en dato i Sluttdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="15010-133">In the End date field, enter a date.</span></span>
25. <span data-ttu-id="15010-134">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="15010-134">Click Save.</span></span>
26. <span data-ttu-id="15010-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="15010-135">Close the page.</span></span>
27. <span data-ttu-id="15010-136">Klikk Stillingsannonser.</span><span class="sxs-lookup"><span data-stu-id="15010-136">Click Job ads.</span></span>
28. <span data-ttu-id="15010-137">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="15010-137">Click Save.</span></span>
29. <span data-ttu-id="15010-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="15010-138">Close the page.</span></span>
30. <span data-ttu-id="15010-139">Merk av eller fjern merket for Vis på ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="15010-139">Check or uncheck the Display on employee self service checkbox.</span></span>
    * <span data-ttu-id="15010-140">Merk av for Vis på ansattselvbetjening for å gjøre rekrutteringsprosjektet synlig for ansatte på ansattselvbetjeningssidene.</span><span class="sxs-lookup"><span data-stu-id="15010-140">Select the Display on employee self service check box to make the recruitment project visible to employees on their Employee self-service pages.</span></span>  
31. <span data-ttu-id="15010-141">Klikk Rekrutteringsprosjektstatus.</span><span class="sxs-lookup"><span data-stu-id="15010-141">Click Recruitment project status.</span></span>
32. <span data-ttu-id="15010-142">Klikk Start.</span><span class="sxs-lookup"><span data-stu-id="15010-142">Click Start.</span></span>
    * <span data-ttu-id="15010-143">Statusen startet betyr at prosjektet er klar til å motta programmer.</span><span class="sxs-lookup"><span data-stu-id="15010-143">The Started status means that the project is ready to receive applications.</span></span>  
33. <span data-ttu-id="15010-144">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="15010-144">Click OK.</span></span>

