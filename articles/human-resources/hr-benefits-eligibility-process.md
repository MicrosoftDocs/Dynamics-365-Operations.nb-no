---
title: Fordelsrettighetsprosess
description: Denne prosedyren viser hvordan fordelsrettighetsprosessen fungerer.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 3720adf26d2cb942bc5d9f6988641bf5e504a852
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465132"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="1e2d2-103">Fordelsrettighetsprosess</span><span class="sxs-lookup"><span data-stu-id="1e2d2-103">Benefit eligibility process</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1e2d2-104">Denne prosedyren viser hvordan fordelsrettighetsprosessen fungerer.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="1e2d2-105">Når prosessen er fullført, kan du vise resultatene.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="1e2d2-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="1e2d2-107">Gå til Personale > Fordeler > Fordeler.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="1e2d2-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1e2d2-109">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1e2d2-110">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="1e2d2-110">Click Edit.</span></span>
5. <span data-ttu-id="1e2d2-111">Velg Regelbasert i Rettighet-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="1e2d2-112">I Regeltype-feltet velger du den fordelspolicyregelen du vil bruke for fordelen.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="1e2d2-113">Klikk Fordel i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="1e2d2-114">Klikk Opprett rettighetshendelse for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="1e2d2-115">Skriv inn en verdi i Hendelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="1e2d2-116">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="1e2d2-117">Velg Åpne registrering i Hendelsestype-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="1e2d2-118">Angi dato og klokkeslett i feltet Startdato for dekning.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="1e2d2-119">Angi en dato og et klokkeslett i feltet Startdato for registreringsperiode.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="1e2d2-120">Angi en verdi er i feltet Dager til registrering.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="1e2d2-121">Klikk Opprett hendelse.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-121">Click Create event.</span></span>
16. <span data-ttu-id="1e2d2-122">Klikk Legg til i hurtigfanen Arbeidere.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="1e2d2-123">Velg Ansatte i feltet Vis etter type.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="1e2d2-124">Velg Gjeldende juridiske enhet i feltet Vis etter juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="1e2d2-125">Merk eller fjern merking for alle rader i listen.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="1e2d2-126">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-126">Click OK.</span></span>
21. <span data-ttu-id="1e2d2-127">Velg Behandle.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-127">Click Process.</span></span>
22. <span data-ttu-id="1e2d2-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-128">Click OK.</span></span>
23. <span data-ttu-id="1e2d2-129">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-129">Refresh the page.</span></span>
24. <span data-ttu-id="1e2d2-130">Klikk Vis resultater.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-130">Click Show results.</span></span>
25. <span data-ttu-id="1e2d2-131">Åpne kolonnefilteret for status.</span><span class="sxs-lookup"><span data-stu-id="1e2d2-131">Open Status column filter.</span></span>
26. <span data-ttu-id="1e2d2-132">Sorter fra A til Å</span><span class="sxs-lookup"><span data-stu-id="1e2d2-132">Sort A to Z</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]