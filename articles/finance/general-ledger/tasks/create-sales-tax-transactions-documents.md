---
title: Opprette mva-transaksjoner på dokumenter
description: Merverdiavgift på dokumenter blir beregnet ved hjelp av en mva-gruppe og en mva-gruppe for vare på dokumentlinjer.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdc4b5c31d9a478a5226ae6b5e8c776de3b661dd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144841"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="922ed-103">Opprette mva-transaksjoner på dokumenter</span><span class="sxs-lookup"><span data-stu-id="922ed-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="922ed-104">Merverdiavgift på dokumenter blir beregnet ved hjelp av en mva-gruppe og en mva-gruppe for vare på dokumentlinjer.</span><span class="sxs-lookup"><span data-stu-id="922ed-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="922ed-105">Dette hentes fra hoveddata, men kan endres manuelt hvis det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="922ed-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="922ed-106">Den beregnede merverdiavgiften kan kontrolleres på et linje- og dokumentnivå.</span><span class="sxs-lookup"><span data-stu-id="922ed-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="922ed-107">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="922ed-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="922ed-108">Gå til Kunder > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="922ed-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="922ed-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="922ed-109">Click New.</span></span>
3. <span data-ttu-id="922ed-110">Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="922ed-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="922ed-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="922ed-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="922ed-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="922ed-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="922ed-113">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="922ed-113">Click OK.</span></span>
7. <span data-ttu-id="922ed-114">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="922ed-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="922ed-115">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="922ed-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="922ed-116">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="922ed-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="922ed-117">Angi et tall i Enhetspris-feltet.</span><span class="sxs-lookup"><span data-stu-id="922ed-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="922ed-118">Vis eller skjul Linjedetaljer-delen.</span><span class="sxs-lookup"><span data-stu-id="922ed-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="922ed-119">Klikk kategorien Oppsett.</span><span class="sxs-lookup"><span data-stu-id="922ed-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="922ed-120">Klikk rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="922ed-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="922ed-121">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="922ed-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="922ed-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="922ed-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="922ed-123">Klikk Finans.</span><span class="sxs-lookup"><span data-stu-id="922ed-123">Click Financials.</span></span>
17. <span data-ttu-id="922ed-124">Klikk Merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="922ed-124">Click Sales tax.</span></span>
18. <span data-ttu-id="922ed-125">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="922ed-125">Click OK.</span></span>
19. <span data-ttu-id="922ed-126">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="922ed-126">Click Add line.</span></span>
20. <span data-ttu-id="922ed-127">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="922ed-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="922ed-128">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="922ed-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="922ed-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="922ed-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="922ed-130">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="922ed-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="922ed-131">Angi et tall i Enhetspris-feltet.</span><span class="sxs-lookup"><span data-stu-id="922ed-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="922ed-132">Klikk rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="922ed-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="922ed-133">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="922ed-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="922ed-134">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="922ed-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="922ed-135">Klikk Selg i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="922ed-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="922ed-136">Klikk Merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="922ed-136">Click Sales tax.</span></span>
30. <span data-ttu-id="922ed-137">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="922ed-137">Click OK.</span></span>

