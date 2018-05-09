--- 
title: Konfigurere konsernintern prosjektfakturering
description: Denne prosedyren viser hvordan du konfigurerer prosjektfakturering mellom to firmaer i organisasjonen.
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 81c41b121732cb72a40ab3d89075770e5404e3c0
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="9e1b9-103">Konfigurere konsernintern prosjektfakturering</span><span class="sxs-lookup"><span data-stu-id="9e1b9-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e1b9-104">Denne prosedyren viser hvordan du konfigurerer prosjektfakturering mellom to firmaer i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="9e1b9-105">Denne oppgaven bruker USSI-datasettet.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="9e1b9-106">Gå til Leverandører > Leverandører > Alle leverandører.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="9e1b9-107">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9e1b9-108">Klikk Generelt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="9e1b9-109">Klikk Konsernintern.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-109">Click Intercompany.</span></span>
5. <span data-ttu-id="9e1b9-110">Angi Aktiv til Ja for å aktivere konsernintern handel.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="9e1b9-111">Angi eller velg en verdi i Kundefirma-feltet.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="9e1b9-112">Angi eller velg en verdi i Min konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="9e1b9-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-113">Click Save.</span></span>
9. <span data-ttu-id="9e1b9-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-114">Close the page.</span></span>
10. <span data-ttu-id="9e1b9-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-115">Close the page.</span></span>
11. <span data-ttu-id="9e1b9-116">Gå til Prosjektstyring og regnskap > Oppsett > Prosjektstyrings- og regnskapsparametere.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="9e1b9-117">Klikk kategorien Konsernintern.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="9e1b9-118">Flytt glidebryteren til Ja for å aktivere konsernintern ressursplanlegging og timeregistreringer.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="9e1b9-119">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="9e1b9-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-120">Click New.</span></span>
16. <span data-ttu-id="9e1b9-121">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="9e1b9-122">Angi eller velg en verdi i feltet Juridisk enhet som låner.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="9e1b9-123">Merk av for Avsett inntekt.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="9e1b9-124">Angi eller velg en verdi i feltet Standard timeregistreringskategori.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="9e1b9-125">Angi eller velg en verdi i feltet Standard utgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="9e1b9-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-126">Click Save.</span></span>
22. <span data-ttu-id="9e1b9-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-127">Close the page.</span></span>
23. <span data-ttu-id="9e1b9-128">Gå til Prosjektstyring og regnskap > Oppsett > Postering > Finansposteringsoppsett.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="9e1b9-129">Velg et alternativ i feltet Finanskontotyper.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="9e1b9-130">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-130">Click New.</span></span>
26. <span data-ttu-id="9e1b9-131">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="9e1b9-132">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="9e1b9-133">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="9e1b9-134">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-134">Click Save.</span></span>
30. <span data-ttu-id="9e1b9-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-135">Close the page.</span></span>
31. <span data-ttu-id="9e1b9-136">Gå til Prosjektstyring og regnskap > Oppsett > Priser > Overføringspris.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="9e1b9-137">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-137">Click New.</span></span>
33. <span data-ttu-id="9e1b9-138">Angi en dato i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="9e1b9-139">Angi eller velg en verdi i feltet Juridisk enhet som låner.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="9e1b9-140">Velg et alternativ i feltet Overføringsprismodell.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="9e1b9-141">Angi et tall i Prissetting-feltet.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="9e1b9-142">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9e1b9-142">Click Save.</span></span>


