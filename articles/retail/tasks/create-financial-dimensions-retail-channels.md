--- 
title: " Opprette finansdimensjoner for detaljhandelskanaler og konfigurere dimensjonsverdier for butikker"
description: "Denne prosedyren hjelper med å opprette en finansdimensjon for detaljandelskanaler med dimensjonsverdier og trinn for å konfigurere finansdimensjonsverdier for detaljhandelsbutikker."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 56b586e971cfd4684f3c0b259270cc8b31521ac9
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="53575-103"> Opprette finansdimensjoner for detaljhandelskanaler og konfigurere dimensjonsverdier for butikker</span><span class="sxs-lookup"><span data-stu-id="53575-103">Create financial dimensions for Retail channels and configure dimension values on stores</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="53575-104">Denne prosedyren hjelper med å opprette en finansdimensjon for detaljandelskanaler med dimensjonsverdier og trinn for å konfigurere finansdimensjonsverdier for detaljhandelsbutikker.</span><span class="sxs-lookup"><span data-stu-id="53575-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="53575-105">Emnet inneholder ikke andre relaterte trinn, for eksempel å opprette dimensjonssett og kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="53575-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="53575-106">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="53575-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="53575-107">Gå til Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="53575-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="53575-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="53575-108">Click New.</span></span>
3. <span data-ttu-id="53575-109">I feltet Bruk verdier fra velger du Detaljhandelskanaler.</span><span class="sxs-lookup"><span data-stu-id="53575-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="53575-110">Skriv inn en verdi i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="53575-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="53575-111">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="53575-111">Click Activate.</span></span>
6. <span data-ttu-id="53575-112">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="53575-112">Click Close.</span></span>
7. <span data-ttu-id="53575-113">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="53575-113">Click Activate.</span></span>
8. <span data-ttu-id="53575-114">Klikk Dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="53575-114">Click Dimension values.</span></span>
9. <span data-ttu-id="53575-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="53575-115">Close the page.</span></span>
10. <span data-ttu-id="53575-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="53575-116">Click Save.</span></span>
11. <span data-ttu-id="53575-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="53575-117">Close the page.</span></span>
12. <span data-ttu-id="53575-118">Gå til Detaljhandel og handel > Kanaler > Detaljhandelbutikker > Alle detaljhandelsbutikker.</span><span class="sxs-lookup"><span data-stu-id="53575-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="53575-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="53575-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="53575-120">Aktiver utvidelsen av delen Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="53575-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="53575-121">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="53575-121">Click Edit.</span></span>
16. <span data-ttu-id="53575-122">Klikk rullegardinknappen i feltet Retailchannel for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="53575-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="53575-123">Finn og velg dimensjonsverdien i listen for butikken som oppdateres.</span><span class="sxs-lookup"><span data-stu-id="53575-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="53575-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="53575-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="53575-125">Klikk rullegardinknappen i feltet CostCenter for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="53575-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="53575-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="53575-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="53575-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="53575-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="53575-128">Klikk rullegardinknappen i Avdeling-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="53575-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="53575-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="53575-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="53575-130">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="53575-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="53575-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="53575-131">Click Save.</span></span>


