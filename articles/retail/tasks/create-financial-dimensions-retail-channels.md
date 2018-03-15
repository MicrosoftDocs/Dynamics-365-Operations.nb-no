--- 
title: " Opprette finansdimensjoner for detaljhandelskanaler og konfigurere dimensjonsverdier for butikker"
description: "Denne prosedyren hjelper med å opprette en finansdimensjon for detaljandelskanaler med dimensjonsverdier og trinn for å konfigurere finansdimensjonsverdier for detaljhandelsbutikker."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 5ab4df61ab1e1346eaaf5c586f54a06b7b7432e1
ms.contentlocale: nb-no
ms.lasthandoff: 02/07/2018

---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="d02bf-103"> Opprette finansdimensjoner for detaljhandelskanaler og konfigurere dimensjonsverdier for butikker</span><span class="sxs-lookup"><span data-stu-id="d02bf-103">Create financial dimensions for Retail channels and configure dimension values on stores</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d02bf-104">Denne prosedyren hjelper med å opprette en finansdimensjon for detaljandelskanaler med dimensjonsverdier og trinn for å konfigurere finansdimensjonsverdier for detaljhandelsbutikker.</span><span class="sxs-lookup"><span data-stu-id="d02bf-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="d02bf-105">Emnet inneholder ikke andre relaterte trinn, for eksempel å opprette dimensjonssett og kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="d02bf-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="d02bf-106">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="d02bf-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="d02bf-107">Gå til Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="d02bf-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="d02bf-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d02bf-108">Click New.</span></span>
3. <span data-ttu-id="d02bf-109">I feltet Bruk verdier fra velger du Detaljhandelskanaler.</span><span class="sxs-lookup"><span data-stu-id="d02bf-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="d02bf-110">Skriv inn en verdi i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="d02bf-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="d02bf-111">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="d02bf-111">Click Activate.</span></span>
6. <span data-ttu-id="d02bf-112">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="d02bf-112">Click Close.</span></span>
7. <span data-ttu-id="d02bf-113">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="d02bf-113">Click Activate.</span></span>
8. <span data-ttu-id="d02bf-114">Klikk Dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="d02bf-114">Click Dimension values.</span></span>
9. <span data-ttu-id="d02bf-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d02bf-115">Close the page.</span></span>
10. <span data-ttu-id="d02bf-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="d02bf-116">Click Save.</span></span>
11. <span data-ttu-id="d02bf-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d02bf-117">Close the page.</span></span>
12. <span data-ttu-id="d02bf-118">Gå til Detaljhandel og handel > Kanaler > Detaljhandelbutikker > Alle detaljhandelsbutikker.</span><span class="sxs-lookup"><span data-stu-id="d02bf-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="d02bf-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d02bf-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="d02bf-120">Aktiver utvidelsen av delen Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="d02bf-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="d02bf-121">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="d02bf-121">Click Edit.</span></span>
16. <span data-ttu-id="d02bf-122">Klikk rullegardinknappen i feltet Retailchannel for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d02bf-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="d02bf-123">Finn og velg dimensjonsverdien i listen for butikken som oppdateres.</span><span class="sxs-lookup"><span data-stu-id="d02bf-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="d02bf-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d02bf-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="d02bf-125">Klikk rullegardinknappen i feltet CostCenter for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d02bf-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="d02bf-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d02bf-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="d02bf-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d02bf-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="d02bf-128">Klikk rullegardinknappen i Avdeling-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d02bf-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="d02bf-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d02bf-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="d02bf-130">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d02bf-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="d02bf-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="d02bf-131">Click Save.</span></span>


