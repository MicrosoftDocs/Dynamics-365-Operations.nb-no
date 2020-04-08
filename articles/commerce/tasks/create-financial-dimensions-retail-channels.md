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
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea36732023092f714b3a783d98b512c0fea7dade
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141413"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="89c7d-103">Opprette finansdimensjoner for detaljhandelskanaler og konfigurere dimensjonsverdier i butikker</span><span class="sxs-lookup"><span data-stu-id="89c7d-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89c7d-104">Denne prosedyren hjelper deg å opprette en finansdimensjon for handelskanaler med dimensjonsverdier og trinn for å konfigurere finansdimensjonsverdier for butikker.</span><span class="sxs-lookup"><span data-stu-id="89c7d-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="89c7d-105">Emnet inneholder ikke andre relaterte trinn, for eksempel å opprette dimensjonssett og kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="89c7d-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="89c7d-106">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="89c7d-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="89c7d-107">Gå til Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="89c7d-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="89c7d-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="89c7d-108">Click New.</span></span>
3. <span data-ttu-id="89c7d-109">I feltet Bruk verdier fra velger du Handelskanaler.</span><span class="sxs-lookup"><span data-stu-id="89c7d-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="89c7d-110">Skriv inn en verdi i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="89c7d-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="89c7d-111">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="89c7d-111">Click Activate.</span></span>
6. <span data-ttu-id="89c7d-112">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="89c7d-112">Click Close.</span></span>
7. <span data-ttu-id="89c7d-113">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="89c7d-113">Click Activate.</span></span>
8. <span data-ttu-id="89c7d-114">Klikk Dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="89c7d-114">Click Dimension values.</span></span>
9. <span data-ttu-id="89c7d-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="89c7d-115">Close the page.</span></span>
10. <span data-ttu-id="89c7d-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="89c7d-116">Click Save.</span></span>
11. <span data-ttu-id="89c7d-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="89c7d-117">Close the page.</span></span>
12. <span data-ttu-id="89c7d-118">Gå til Retail og Commerce > Kanaler > Butikker > Alle butikker.</span><span class="sxs-lookup"><span data-stu-id="89c7d-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="89c7d-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="89c7d-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="89c7d-120">Aktiver utvidelsen av delen Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="89c7d-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="89c7d-121">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="89c7d-121">Click Edit.</span></span>
16. <span data-ttu-id="89c7d-122">Klikk rullegardinknappen i Handelskanal-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="89c7d-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="89c7d-123">Finn og velg dimensjonsverdien i listen for butikken som oppdateres.</span><span class="sxs-lookup"><span data-stu-id="89c7d-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="89c7d-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="89c7d-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="89c7d-125">Klikk rullegardinknappen i feltet CostCenter for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="89c7d-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="89c7d-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="89c7d-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="89c7d-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="89c7d-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="89c7d-128">Klikk rullegardinknappen i Avdeling-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="89c7d-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="89c7d-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="89c7d-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="89c7d-130">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="89c7d-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="89c7d-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="89c7d-131">Click Save.</span></span>

