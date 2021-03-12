---
title: " Konfigurere kredittkortbehandling"
description: Denne prosedyren hjelper med å vise listen over betalingsleverandører og hvordan du konfigurerer en betalingskonto for kunder.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 611cc49d2373247da141d2fafc149d05f3bd13b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006116"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="7c8ef-103"> Konfigurere kredittkortbehandling</span><span class="sxs-lookup"><span data-stu-id="7c8ef-103">Configure credit card processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c8ef-104">Denne prosedyren hjelper med å vise listen over betalingsleverandører og hvordan du konfigurerer en betalingskonto for kunder.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="7c8ef-105">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene og er ment for administratorer og IT-eksperter.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="7c8ef-106">Vise en liste med betalingsleverandører</span><span class="sxs-lookup"><span data-stu-id="7c8ef-106">View a list of payment providers</span></span>
1. <span data-ttu-id="7c8ef-107">Gå til Kunder > Betalingsoppsett > Betalingstjenester.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="7c8ef-108">Klikk Vis tilgjengelige leverandører.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="7c8ef-109">Konfigurere betalingskonto</span><span class="sxs-lookup"><span data-stu-id="7c8ef-109">Configure payment account</span></span>
1. <span data-ttu-id="7c8ef-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-110">Click New.</span></span>
2. <span data-ttu-id="7c8ef-111">Skriv inn en verdi i Betalingstjeneste-feltet.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="7c8ef-112">Velg et alternativ i feltet Betalingskobling.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="7c8ef-113">Aktiver/deaktiver utvidelsen av delen Betalingstjenestekonto.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="7c8ef-114">I Miljø-feltet skriver du inn PROD.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="7c8ef-115">Klikk Kredittkorttyper.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-115">Click Credit card types.</span></span>
7. <span data-ttu-id="7c8ef-116">Klikk rullegardinknappen i feltet Betalingsjournal for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="7c8ef-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7c8ef-118">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-118">Click Add.</span></span>
10. <span data-ttu-id="7c8ef-119">Skriv inn en verdi i Valuta-feltet.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="7c8ef-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="7c8ef-121">Klikk rullegardinknappen i feltet Betalingsjournal for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="7c8ef-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="7c8ef-123">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-123">Click Add.</span></span>
15. <span data-ttu-id="7c8ef-124">Skriv inn en verdi i Valuta-feltet.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="7c8ef-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7c8ef-126">Du kan gjenta denne fremgangsmåten for så mange korttyper du ønsker.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="7c8ef-127">Klikk rullegardinknappen i feltet Betalingsjournal for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="7c8ef-128">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="7c8ef-129">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-129">Click Add.</span></span>
20. <span data-ttu-id="7c8ef-130">Skriv inn en verdi i Valuta-feltet.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="7c8ef-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-131">Click Save.</span></span>
22. <span data-ttu-id="7c8ef-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-132">Close the page.</span></span>
23. <span data-ttu-id="7c8ef-133">Klikk Valider.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-133">Click Validate.</span></span>
24. <span data-ttu-id="7c8ef-134">Klikk Standardbehandler for nye kredittkort.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="7c8ef-135">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7c8ef-135">Click Save.</span></span>

