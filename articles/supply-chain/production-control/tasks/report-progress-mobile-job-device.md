---
title: Rapportere fremdrift på en mobil jobbenhet
description: Denne prosedyren viser hvordan du starter og rapporterer fremdriften for en produksjonsjobb i registreringsskjemaet for jobbenheten.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationTouch, JmgRegistrationTouchUserConfiguration, JmgRegistrationTouchStart, JmgRegistrationTouchReportFeedback, JmgRegistrationTouchAssignedJobs, JmgRegistrationTouchBreak, JmgRegistrationTouchLeave, JmgRegistrationTouchIndirectActivity, JmgDialogForm, JmgRegistrationTouchReportProgress, JmgFeedbackWizard, JmgJobBundleProdFeedback
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a56e538d18c4e458f0e40801d0f01537a2246d2
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826273"
---
# <a name="report-progress-on-a-mobile-job-device"></a><span data-ttu-id="b142c-103">Rapportere fremdrift på en mobil jobbenhet</span><span class="sxs-lookup"><span data-stu-id="b142c-103">Report progress on a mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b142c-104">Denne prosedyren viser hvordan du starter og rapporterer fremdriften for en produksjonsjobb i registreringsskjemaet for jobbenheten.</span><span class="sxs-lookup"><span data-stu-id="b142c-104">This procedure shows you how to start and report progress on a production job in the job device registration form.</span></span>



<span data-ttu-id="b142c-105">Hvis du vil kjøre denne prosedyren, må du ha rollen Systemansvarlig eller Maskinoperatør knyttet til brukerkontoen.</span><span class="sxs-lookup"><span data-stu-id="b142c-105">To be able to run this procedure you must have the System administator or Machine Operator role associated with the user account.</span></span>

1. <span data-ttu-id="b142c-106">Gå til Produksjonskontroll > Produksjonsutførelse > Jobbkortenhet.</span><span class="sxs-lookup"><span data-stu-id="b142c-106">Go to Production control > Manufacturing execution > Job card device.</span></span>
2. <span data-ttu-id="b142c-107">Angi kortet for en arbeider i WorkerTextField-feltet.</span><span class="sxs-lookup"><span data-stu-id="b142c-107">In the WorkerTextField field, enter the badge of a worker.</span></span> <span data-ttu-id="b142c-108">Skriv inn "123" for Christina Portra i demonstrasjonsdataene for USMF.</span><span class="sxs-lookup"><span data-stu-id="b142c-108">In the USMF demo data type '123' for Christina Portra..</span></span>
3. <span data-ttu-id="b142c-109">Klikk Logg på.</span><span class="sxs-lookup"><span data-stu-id="b142c-109">Click Log in.</span></span>
4. <span data-ttu-id="b142c-110">Klikk Filter-knappen.</span><span class="sxs-lookup"><span data-stu-id="b142c-110">Click the Filter button.</span></span>
5. <span data-ttu-id="b142c-111">Merk av eller fjern merket for Bruk konfigurasjonsfilter.</span><span class="sxs-lookup"><span data-stu-id="b142c-111">Check or uncheck the Apply configuration filter check box.</span></span> <span data-ttu-id="b142c-112">Hvis du definerer et filter, kan du bruke produksjonsenheten 110 i USMF.</span><span class="sxs-lookup"><span data-stu-id="b142c-112">If you set a filter you can use production unit 110 in USMF.</span></span>
6. <span data-ttu-id="b142c-113">Velg ressursgruppen for produksjonsjobber som arbeideren kan jobbe på, i Produksjonsenhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="b142c-113">In the Production unit field, select the ressource group for which production jobs the worker can work on.</span></span>
7. <span data-ttu-id="b142c-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b142c-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b142c-115">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b142c-115">Click OK.</span></span>
9. <span data-ttu-id="b142c-116">Klikk Start jobb-knappen.</span><span class="sxs-lookup"><span data-stu-id="b142c-116">Click the Start job button.</span></span>
10. <span data-ttu-id="b142c-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b142c-117">Click OK.</span></span>
11. <span data-ttu-id="b142c-118">Klikk Rapportfremdrift-knappen.</span><span class="sxs-lookup"><span data-stu-id="b142c-118">Click the Report progress button.</span></span>
12. <span data-ttu-id="b142c-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b142c-119">Click OK.</span></span>
13. <span data-ttu-id="b142c-120">Klikk Neste jobb-knappen.</span><span class="sxs-lookup"><span data-stu-id="b142c-120">Click the Next job button.</span></span>
14. <span data-ttu-id="b142c-121">Klikk den tilordnede for å se en oversikt over alle produksjonsjobber.</span><span class="sxs-lookup"><span data-stu-id="b142c-121">Click the Assigned to see an overview of all production jobs button.</span></span>
15. <span data-ttu-id="b142c-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b142c-122">Close the page.</span></span>
16. <span data-ttu-id="b142c-123">Klikk Pause-knappen.</span><span class="sxs-lookup"><span data-stu-id="b142c-123">Click the Break button.</span></span>
17. <span data-ttu-id="b142c-124">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b142c-124">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="b142c-125">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b142c-125">Click OK.</span></span>
19. <span data-ttu-id="b142c-126">Klikk Avslutter-knappen.</span><span class="sxs-lookup"><span data-stu-id="b142c-126">Click the Leaving button.</span></span>
20. <span data-ttu-id="b142c-127">Velg for å logge av.</span><span class="sxs-lookup"><span data-stu-id="b142c-127">Select to log out.</span></span>
21. <span data-ttu-id="b142c-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b142c-128">Click OK.</span></span>
22. <span data-ttu-id="b142c-129">Logg på på nytt i feltet WorkerTextField.</span><span class="sxs-lookup"><span data-stu-id="b142c-129">In the WorkerTextField field, log in again.</span></span> <span data-ttu-id="b142c-130">Du kan velge arbeideren 123 i USMF-demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="b142c-130">You can select worker '123' in USMF demo data.</span></span>
23. <span data-ttu-id="b142c-131">Klikk Logg på.</span><span class="sxs-lookup"><span data-stu-id="b142c-131">Click Log in.</span></span>
24. <span data-ttu-id="b142c-132">Klikk Stopp pause.</span><span class="sxs-lookup"><span data-stu-id="b142c-132">Click Stop break.</span></span>
25. <span data-ttu-id="b142c-133">Klikk Aktivitet-knappen,</span><span class="sxs-lookup"><span data-stu-id="b142c-133">Click the Activity button.</span></span>
26. <span data-ttu-id="b142c-134">Klikk Avbryt.</span><span class="sxs-lookup"><span data-stu-id="b142c-134">Click Cancel.</span></span>
27. <span data-ttu-id="b142c-135">Klikk Avslutter-knappen.</span><span class="sxs-lookup"><span data-stu-id="b142c-135">Click the Leaving button.</span></span>
28. <span data-ttu-id="b142c-136">Velg for å stemple ut.</span><span class="sxs-lookup"><span data-stu-id="b142c-136">Select to clock out.</span></span>
29. <span data-ttu-id="b142c-137">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b142c-137">Click OK.</span></span>
30. <span data-ttu-id="b142c-138">Velg en årsak til hvorfor du stempler ut tidlig.</span><span class="sxs-lookup"><span data-stu-id="b142c-138">Select a reason why you are clocking out early.</span></span>

