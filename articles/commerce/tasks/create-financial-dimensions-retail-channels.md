---
title: Opprette finansdimensjoner for detaljhandelskanaler og konfigurere dimensjonsverdier i butikker
description: Denne prosedyren hjelper deg å opprette en finansdimensjon for handelskanaler med dimensjonsverdier og trinn for å konfigurere finansdimensjonsverdier for butikker.
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
ms.openlocfilehash: 5250e93757560f4a0f76897e3dd1374d14ff5e60
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264266"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="feab2-103">Opprette finansdimensjoner for detaljhandelskanaler og konfigurere dimensjonsverdier i butikker</span><span class="sxs-lookup"><span data-stu-id="feab2-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="feab2-104">Denne prosedyren hjelper deg å opprette en finansdimensjon for handelskanaler med dimensjonsverdier og trinn for å konfigurere finansdimensjonsverdier for butikker.</span><span class="sxs-lookup"><span data-stu-id="feab2-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="feab2-105">Emnet inneholder ikke andre relaterte trinn, for eksempel å opprette dimensjonssett og kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="feab2-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="feab2-106">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="feab2-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="feab2-107">Gå til Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="feab2-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="feab2-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="feab2-108">Click New.</span></span>
3. <span data-ttu-id="feab2-109">I feltet Bruk verdier fra velger du Handelskanaler.</span><span class="sxs-lookup"><span data-stu-id="feab2-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="feab2-110">Skriv inn en verdi i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="feab2-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="feab2-111">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="feab2-111">Click Activate.</span></span>
6. <span data-ttu-id="feab2-112">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="feab2-112">Click Close.</span></span>
7. <span data-ttu-id="feab2-113">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="feab2-113">Click Activate.</span></span>
8. <span data-ttu-id="feab2-114">Klikk Dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="feab2-114">Click Dimension values.</span></span>
9. <span data-ttu-id="feab2-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="feab2-115">Close the page.</span></span>
10. <span data-ttu-id="feab2-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="feab2-116">Click Save.</span></span>
11. <span data-ttu-id="feab2-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="feab2-117">Close the page.</span></span>
12. <span data-ttu-id="feab2-118">Gå til Retail og Commerce > Kanaler > Butikker > Alle butikker.</span><span class="sxs-lookup"><span data-stu-id="feab2-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="feab2-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="feab2-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="feab2-120">Aktiver utvidelsen av delen Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="feab2-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="feab2-121">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="feab2-121">Click Edit.</span></span>
16. <span data-ttu-id="feab2-122">Klikk rullegardinknappen i Handelskanal-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="feab2-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="feab2-123">Finn og velg dimensjonsverdien i listen for butikken som oppdateres.</span><span class="sxs-lookup"><span data-stu-id="feab2-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="feab2-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="feab2-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="feab2-125">Klikk rullegardinknappen i feltet CostCenter for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="feab2-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="feab2-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="feab2-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="feab2-127">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="feab2-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="feab2-128">Klikk på rullegardinknappen i Avdeling-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="feab2-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="feab2-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="feab2-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="feab2-130">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="feab2-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="feab2-131">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="feab2-131">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]