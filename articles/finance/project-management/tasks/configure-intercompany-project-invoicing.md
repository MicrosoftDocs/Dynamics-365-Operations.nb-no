---
title: Konfigurere konsernintern prosjektfakturering
description: Dette emnet viser hvordan du konfigurerer prosjektfakturering mellom to firmaer i organisasjonen.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31dbae2d37aefe1841fe85cb6caf185c78596e55
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144285"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="b0943-103">Konfigurere konsernintern prosjektfakturering</span><span class="sxs-lookup"><span data-stu-id="b0943-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0943-104">Dette emnet viser hvordan du konfigurerer prosjektfakturering mellom to firmaer i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="b0943-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="b0943-105">Denne oppgaven bruker USSI-datasettet.</span><span class="sxs-lookup"><span data-stu-id="b0943-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="b0943-106">Gå til **Moduler > Leverandører > Leverandører > Leverandører > Alle leverandører** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="b0943-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="b0943-107">Finn og velg ønsket post i listen **Alle leverandører**.</span><span class="sxs-lookup"><span data-stu-id="b0943-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="b0943-108">Klikk på **Generelt** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b0943-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="b0943-109">Velg **Konsernintern**.</span><span class="sxs-lookup"><span data-stu-id="b0943-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="b0943-110">Angi **Aktiv** til **Ja** for å aktivere konsernintern handel.</span><span class="sxs-lookup"><span data-stu-id="b0943-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="b0943-111">Angi eller velg en verdi i **Kundefirma**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0943-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="b0943-112">Angi eller velg en verdi i **Min konto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0943-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="b0943-113">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b0943-113">Select **Save**.</span></span>
9. <span data-ttu-id="b0943-114">Lukk sidene for å gå tilbake til startsiden.</span><span class="sxs-lookup"><span data-stu-id="b0943-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="b0943-115">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Prosjektstyrings- og regnskapsparametere**.</span><span class="sxs-lookup"><span data-stu-id="b0943-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="b0943-116">Velg kategorien **Konsernintern**.</span><span class="sxs-lookup"><span data-stu-id="b0943-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="b0943-117">Flytt glidebryteren til **Ja** for å aktivere konsernintern ressursplanlegging og timeregistreringer.</span><span class="sxs-lookup"><span data-stu-id="b0943-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="b0943-118">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b0943-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="b0943-119">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b0943-119">Select **New**.</span></span>
15. <span data-ttu-id="b0943-120">Angi eller velg en verdi i feltet **Juridisk enhet som låner**.</span><span class="sxs-lookup"><span data-stu-id="b0943-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="b0943-121">Merk av for **Avsett inntekt**.</span><span class="sxs-lookup"><span data-stu-id="b0943-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="b0943-122">Angi eller velg en verdi i feltet **Standard timeregistreringskategori**.</span><span class="sxs-lookup"><span data-stu-id="b0943-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="b0943-123">Angi eller velg en verdi i feltet **Standard utgiftskategori**.</span><span class="sxs-lookup"><span data-stu-id="b0943-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="b0943-124">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b0943-124">Select **Save**.</span></span>
20. <span data-ttu-id="b0943-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b0943-125">Close the page.</span></span>
21. <span data-ttu-id="b0943-126">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Postering > Finansposteringsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="b0943-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="b0943-127">Velg et alternativ i feltet **Finanskontotyper**.</span><span class="sxs-lookup"><span data-stu-id="b0943-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="b0943-128">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b0943-128">Select **New**.</span></span>
24. <span data-ttu-id="b0943-129">Angi de ønskede verdiene i **Hovedkonto**-feltet for den nye raden.</span><span class="sxs-lookup"><span data-stu-id="b0943-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="b0943-130">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b0943-130">Select **Save**.</span></span>
26. <span data-ttu-id="b0943-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b0943-131">Close the page.</span></span>
27. <span data-ttu-id="b0943-132">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Overføringspris**.</span><span class="sxs-lookup"><span data-stu-id="b0943-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="b0943-133">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b0943-133">Select **New**.</span></span>
29. <span data-ttu-id="b0943-134">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="b0943-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="b0943-135">Angi eller velg en verdi i feltet **Juridisk enhet som låner**.</span><span class="sxs-lookup"><span data-stu-id="b0943-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="b0943-136">Velg et alternativ i feltet **Overføringsprismodell**.</span><span class="sxs-lookup"><span data-stu-id="b0943-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="b0943-137">Angi et tall i **Prissetting**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0943-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="b0943-138">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b0943-138">Select **Save**.</span></span>

