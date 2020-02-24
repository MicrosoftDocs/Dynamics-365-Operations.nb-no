---
title: Registrere og fjerne fordeler fra arbeidere
description: Denne prosedyren beskriver hvordan én enkelt arbeider kan registreres i én eller flere fordeler, samt hvordan flere arbeidere kan registreres i en fordel.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 2e150032eb4c620a883520a2b24b74c66fca1fb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010137"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="4c40a-103">Registrere og fjerne fordeler fra arbeidere</span><span class="sxs-lookup"><span data-stu-id="4c40a-103">Enroll and remove benefits from workers</span></span>



<span data-ttu-id="4c40a-104">Denne prosedyren beskriver hvordan én enkelt arbeider kan registreres i én eller flere fordeler, samt hvordan flere arbeidere kan registreres i en fordel.</span><span class="sxs-lookup"><span data-stu-id="4c40a-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="4c40a-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="4c40a-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="4c40a-106">Registrere én arbeider i fordeler</span><span class="sxs-lookup"><span data-stu-id="4c40a-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="4c40a-107">Gå til Personale > Arbeidere > Ansatte.</span><span class="sxs-lookup"><span data-stu-id="4c40a-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="4c40a-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4c40a-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4c40a-109">Klikk Fordeler.</span><span class="sxs-lookup"><span data-stu-id="4c40a-109">Click Benefits.</span></span>
4. <span data-ttu-id="4c40a-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4c40a-110">Click New.</span></span>
5. <span data-ttu-id="4c40a-111">Angi eller velg en verdi i feltet Fordel.</span><span class="sxs-lookup"><span data-stu-id="4c40a-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="4c40a-112">Angi dato og klokkeslett i feltet Startdato for dekning.</span><span class="sxs-lookup"><span data-stu-id="4c40a-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="4c40a-113">Angi dato og klokkeslett i feltet Sluttdato for dekning.</span><span class="sxs-lookup"><span data-stu-id="4c40a-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="4c40a-114">Utvid delen Mottakere hvis mottakere skal legges til i fordelen.</span><span class="sxs-lookup"><span data-stu-id="4c40a-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="4c40a-115">Du kan også legge til avhengige fra denne siden hvis aktuelt for fordelen.</span><span class="sxs-lookup"><span data-stu-id="4c40a-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="4c40a-116">Du kan også redigere detaljene for en fordelsregistrering eller slette en registrering på denne siden.</span><span class="sxs-lookup"><span data-stu-id="4c40a-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="4c40a-117">Når du er ferdig med å gjøre endringer i fordelsregistrering, lukker du siden.</span><span class="sxs-lookup"><span data-stu-id="4c40a-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="4c40a-118">Registrere flere arbeidere i en fordel</span><span class="sxs-lookup"><span data-stu-id="4c40a-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="4c40a-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4c40a-119">Close the page.</span></span>
2. <span data-ttu-id="4c40a-120">Gå til Personale > Arbeidere > Ansatte.</span><span class="sxs-lookup"><span data-stu-id="4c40a-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="4c40a-121">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4c40a-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="4c40a-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4c40a-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4c40a-123">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4c40a-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="4c40a-124">Klikk Registrer i fordeler.</span><span class="sxs-lookup"><span data-stu-id="4c40a-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="4c40a-125">Angi eller velg en verdi i feltet Fordel.</span><span class="sxs-lookup"><span data-stu-id="4c40a-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="4c40a-126">Angi dato og klokkeslett i feltet Startdato for dekning.</span><span class="sxs-lookup"><span data-stu-id="4c40a-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="4c40a-127">Angi dato og klokkeslett i feltet Sluttdato for dekning.</span><span class="sxs-lookup"><span data-stu-id="4c40a-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="4c40a-128">Klikk Registrer.</span><span class="sxs-lookup"><span data-stu-id="4c40a-128">Click Enroll.</span></span>
11. <span data-ttu-id="4c40a-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4c40a-129">Close the page.</span></span>
12. <span data-ttu-id="4c40a-130">Gå til Personale > Fordeler > Registrering > Resultater av fordelsregistrering.</span><span class="sxs-lookup"><span data-stu-id="4c40a-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="4c40a-131">Finn fordelsresultatposten som du leter etter.</span><span class="sxs-lookup"><span data-stu-id="4c40a-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="4c40a-132">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4c40a-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="4c40a-133">På denne siden kan du se hvilke ansatte som er registrert i fordelen, i tillegg til ansatte som ikke er registrert.</span><span class="sxs-lookup"><span data-stu-id="4c40a-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

