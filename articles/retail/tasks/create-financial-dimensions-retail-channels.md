---
title: Opprette finansdimensjoner for detaljhandelskanaler og konfigurere dimensjonsverdier for butikker
description: Denne prosedyren hjelper med å opprette en finansdimensjon for detaljandelskanaler med dimensjonsverdier og trinn for å konfigurere finansdimensjonsverdier for detaljhandelsbutikker.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf32d17a36fd699141ce697d23e20b2eb5cbfa54
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566462"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="fa6d9-103">Opprette finansdimensjoner for detaljhandelskanaler og konfigurere dimensjonsverdier for butikker</span><span class="sxs-lookup"><span data-stu-id="fa6d9-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="fa6d9-104">Denne prosedyren hjelper med å opprette en finansdimensjon for detaljandelskanaler med dimensjonsverdier og trinn for å konfigurere finansdimensjonsverdier for detaljhandelsbutikker.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="fa6d9-105">Emnet inneholder ikke andre relaterte trinn, for eksempel å opprette dimensjonssett og kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="fa6d9-106">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="fa6d9-107">Gå til Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="fa6d9-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-108">Click New.</span></span>
3. <span data-ttu-id="fa6d9-109">I feltet Bruk verdier fra velger du Detaljhandelskanaler.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="fa6d9-110">Skriv inn en verdi i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="fa6d9-111">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-111">Click Activate.</span></span>
6. <span data-ttu-id="fa6d9-112">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-112">Click Close.</span></span>
7. <span data-ttu-id="fa6d9-113">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-113">Click Activate.</span></span>
8. <span data-ttu-id="fa6d9-114">Klikk Dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-114">Click Dimension values.</span></span>
9. <span data-ttu-id="fa6d9-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-115">Close the page.</span></span>
10. <span data-ttu-id="fa6d9-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-116">Click Save.</span></span>
11. <span data-ttu-id="fa6d9-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-117">Close the page.</span></span>
12. <span data-ttu-id="fa6d9-118">Gå til Detaljhandel og handel > Kanaler > Detaljhandelbutikker > Alle detaljhandelsbutikker.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="fa6d9-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="fa6d9-120">Aktiver utvidelsen av delen Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="fa6d9-121">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="fa6d9-121">Click Edit.</span></span>
16. <span data-ttu-id="fa6d9-122">Klikk rullegardinknappen i feltet Retailchannel for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="fa6d9-123">Finn og velg dimensjonsverdien i listen for butikken som oppdateres.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="fa6d9-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="fa6d9-125">Klikk rullegardinknappen i feltet CostCenter for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="fa6d9-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="fa6d9-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="fa6d9-128">Klikk rullegardinknappen i Avdeling-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="fa6d9-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="fa6d9-130">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="fa6d9-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa6d9-131">Click Save.</span></span>

