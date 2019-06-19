---
title: Konfigurere kontantstørrelser for salgsstedet
description: Kontantstørrelser for sedler og mynter kan defineres i Back Office som skal brukes av kasserere, selgere og ledere i butikken ved salgsstedet.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a34ae8084c0ad55221f4ab93eb8c6481fa8c4771
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606762"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a><span data-ttu-id="367c8-103">Konfigurere kontantstørrelser for salgsstedet</span><span class="sxs-lookup"><span data-stu-id="367c8-103">Configure cash denominations for the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="367c8-104">Kontantstørrelser for sedler og mynter kan defineres i Back Office som skal brukes av kasserere, selgere og ledere i butikken ved salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="367c8-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="367c8-105">Disse størrelsene kan være til hjelp for å telle kontanter for dagsoppgjør eller raskt gjennomføring av et salg.</span><span class="sxs-lookup"><span data-stu-id="367c8-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="367c8-106">Definere størrelser</span><span class="sxs-lookup"><span data-stu-id="367c8-106">Define denominations</span></span>

<span data-ttu-id="367c8-107">Størrelsene er definert per butikk i alternativet **Oppsett** \> **Kontantoppgjør** fra butikkoppgjørsiden.</span><span class="sxs-lookup"><span data-stu-id="367c8-107">The denominations are set up per store on the **Set up** \> **Cash declaration** option from the store property page.</span></span>

![Kontantoppgjør-alternativet](./media/image1-denomination.png)

<span data-ttu-id="367c8-109">Slik definerer du en størrelse:</span><span class="sxs-lookup"><span data-stu-id="367c8-109">To define a denomination:</span></span>

1. <span data-ttu-id="367c8-110">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="367c8-110">Click **New**.</span></span>
1. <span data-ttu-id="367c8-111">Angi typen (mynt eller seddel).</span><span class="sxs-lookup"><span data-stu-id="367c8-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="367c8-112">Angi beløpet (verdi).</span><span class="sxs-lookup"><span data-stu-id="367c8-112">Specify the amount (value).</span></span>

![Kontantoppgjørsstørrelser-side](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="367c8-114">Konfigurer funksjonalitetsprofilen</span><span class="sxs-lookup"><span data-stu-id="367c8-114">Configure the functionality profile</span></span>

<span data-ttu-id="367c8-115">Ved kontantbetaling i salgsstedet POS kan brukeren bruke seddelstørrelsene til raskt å skrive inn beløpet som betales av kunden.</span><span class="sxs-lookup"><span data-stu-id="367c8-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="367c8-116">I funksjonalitetsprofilen kan du konfigurere de to alternativene for å vise størrelsen i salgssted.</span><span class="sxs-lookup"><span data-stu-id="367c8-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

- <span data-ttu-id="367c8-117">**Større eller lik det forfalte beløpet** – Som standard viser salgssted bare seddelstørrelser som er større enn det forfalte beløpet, noe som muliggjør ett trykks betaling.</span><span class="sxs-lookup"><span data-stu-id="367c8-117">**Greater or equal to amount due** – By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="367c8-118">Hvis det forfalte beløpet for eksempel er $ 7,50, kan salgssted vise følgende størrelser: $ 10, $ 20, $ 50 og $ 100.</span><span class="sxs-lookup"><span data-stu-id="367c8-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="367c8-119">Berøres noen av disse beløpene, gjennomføres automatisk salget for dette beløpet.</span><span class="sxs-lookup"><span data-stu-id="367c8-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="367c8-120">Sedlene $1 og $5 vises ikke siden disse beløpene er lavere enn beløpet som forfaller.</span><span class="sxs-lookup"><span data-stu-id="367c8-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>
- <span data-ttu-id="367c8-121">**Alle størrelser** – Velg dette alternativet for alltid å vise alle seddelstørrelser i salgssted, uavhengig av forfalt beløp.</span><span class="sxs-lookup"><span data-stu-id="367c8-121">**All denominations** – Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="367c8-122">Dette betyr at brukeren kan bruke en kombinasjon av sedler for å nå det forfalte beløpet.</span><span class="sxs-lookup"><span data-stu-id="367c8-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="367c8-123">Hvis for eksempel det forfalte beløpet er $ 25,00, kan brukeren velge $ 20 og $ 5 for å fullføre salget.</span><span class="sxs-lookup"><span data-stu-id="367c8-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>
