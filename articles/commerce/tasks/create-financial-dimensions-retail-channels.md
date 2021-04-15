---
title: Opprette finansdimensjoner for detaljhandelskanaler og konfigurere dimensjonsverdier i butikker
description: Denne prosedyren hjelper deg å opprette en finansdimensjon for handelskanaler med dimensjonsverdier og trinn for å konfigurere finansdimensjonsverdier for butikker.
author: jashanno
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0212d3bd808b2a46fa30e8b2bdaa3c0b52ca0dd6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790938"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="8ea97-103">Opprette finansdimensjoner for detaljhandelskanaler og konfigurere dimensjonsverdier i butikker</span><span class="sxs-lookup"><span data-stu-id="8ea97-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ea97-104">Denne prosedyren hjelper deg å opprette en finansdimensjon for handelskanaler med dimensjonsverdier og trinn for å konfigurere finansdimensjonsverdier for butikker.</span><span class="sxs-lookup"><span data-stu-id="8ea97-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="8ea97-105">Emnet inneholder ikke andre relaterte trinn, for eksempel å opprette dimensjonssett og kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="8ea97-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="8ea97-106">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="8ea97-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="8ea97-107">Gå til Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="8ea97-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="8ea97-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8ea97-108">Click New.</span></span>
3. <span data-ttu-id="8ea97-109">I feltet Bruk verdier fra velger du Handelskanaler.</span><span class="sxs-lookup"><span data-stu-id="8ea97-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="8ea97-110">Skriv inn en verdi i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="8ea97-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="8ea97-111">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="8ea97-111">Click Activate.</span></span>
6. <span data-ttu-id="8ea97-112">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="8ea97-112">Click Close.</span></span>
7. <span data-ttu-id="8ea97-113">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="8ea97-113">Click Activate.</span></span>
8. <span data-ttu-id="8ea97-114">Klikk Dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="8ea97-114">Click Dimension values.</span></span>
9. <span data-ttu-id="8ea97-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8ea97-115">Close the page.</span></span>
10. <span data-ttu-id="8ea97-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="8ea97-116">Click Save.</span></span>
11. <span data-ttu-id="8ea97-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8ea97-117">Close the page.</span></span>
12. <span data-ttu-id="8ea97-118">Gå til Retail og Commerce > Kanaler > Butikker > Alle butikker.</span><span class="sxs-lookup"><span data-stu-id="8ea97-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="8ea97-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8ea97-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="8ea97-120">Aktiver utvidelsen av delen Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="8ea97-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="8ea97-121">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="8ea97-121">Click Edit.</span></span>
16. <span data-ttu-id="8ea97-122">Klikk rullegardinknappen i Handelskanal-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8ea97-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="8ea97-123">Finn og velg dimensjonsverdien i listen for butikken som oppdateres.</span><span class="sxs-lookup"><span data-stu-id="8ea97-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="8ea97-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8ea97-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="8ea97-125">Klikk rullegardinknappen i feltet CostCenter for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8ea97-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="8ea97-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8ea97-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="8ea97-127">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8ea97-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="8ea97-128">Klikk på rullegardinknappen i Avdeling-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8ea97-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="8ea97-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8ea97-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="8ea97-130">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8ea97-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="8ea97-131">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="8ea97-131">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]