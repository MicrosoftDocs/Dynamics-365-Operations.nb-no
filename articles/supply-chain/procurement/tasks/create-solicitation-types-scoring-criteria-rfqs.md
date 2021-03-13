---
title: Opprette forespørselstyper og poengkriterier for tilbudsforespørsler
description: Denne veiledningen viser hvordan du oppretter en forespørsels og knytter den til en poengberegningsmetode.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40625152a579bb269411d026d77d449902c8d4bc
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016812"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="b66e5-103">Opprette forespørselstyper og poengkriterier for tilbudsforespørsler</span><span class="sxs-lookup"><span data-stu-id="b66e5-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b66e5-104">Denne veiledningen viser hvordan du oppretter en forespørsels og knytter den til en poengberegningsmetode.</span><span class="sxs-lookup"><span data-stu-id="b66e5-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="b66e5-105">Den viser også hvordan du bruker forespørselstypen på en tilbudsforespørsel som deretter angir standard poengberegningsmetode.</span><span class="sxs-lookup"><span data-stu-id="b66e5-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="b66e5-106">Disse oppgavene vil vanligvis utføres av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="b66e5-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="b66e5-107">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="b66e5-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="b66e5-108">Du må ha en poengberegningsmetode før du begynner.</span><span class="sxs-lookup"><span data-stu-id="b66e5-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="b66e5-109">Opprette en forespørselstype</span><span class="sxs-lookup"><span data-stu-id="b66e5-109">Create a solicitation type</span></span>
1. <span data-ttu-id="b66e5-110">Gå til Innkjøp og leverandører > Oppsett > Tilbudsforespørsel > Forespørselstype.</span><span class="sxs-lookup"><span data-stu-id="b66e5-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="b66e5-111">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="b66e5-111">Click New.</span></span>
3. <span data-ttu-id="b66e5-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="b66e5-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b66e5-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b66e5-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b66e5-114">I feltet Poengberegningsmetode velger du poengberegningsmetoden du vil bruke for denne forespørselstypen.</span><span class="sxs-lookup"><span data-stu-id="b66e5-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="b66e5-115">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="b66e5-115">Click Save.</span></span>
7. <span data-ttu-id="b66e5-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b66e5-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="b66e5-117">Bruke forespørselstypen</span><span class="sxs-lookup"><span data-stu-id="b66e5-117">Use the solicitation type</span></span>
1. <span data-ttu-id="b66e5-118">Gå til Innkjøp og leverandører > Tilbudsforespørsler > Alle tilbudsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="b66e5-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="b66e5-119">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="b66e5-119">Click New.</span></span>
3. <span data-ttu-id="b66e5-120">I Forespørselstype-feltet velger du forespørselstypen som du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="b66e5-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="b66e5-121">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="b66e5-121">Click OK.</span></span>
5. <span data-ttu-id="b66e5-122">Klikk på Poengkriterier.</span><span class="sxs-lookup"><span data-stu-id="b66e5-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="b66e5-123">Poengkriteriene som vises, er de fra poengberegningsmetoden som du knyttet til forespørselstypen.</span><span class="sxs-lookup"><span data-stu-id="b66e5-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="b66e5-124">Du kan velge å legge til eller slette kriteriene på denne siden.</span><span class="sxs-lookup"><span data-stu-id="b66e5-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="b66e5-125">Du kan også legge til nye kriterier ved å kopiere dem fra andre poengberegningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="b66e5-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="b66e5-126">Klikk på Kopier kriterier.</span><span class="sxs-lookup"><span data-stu-id="b66e5-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="b66e5-127">Angi eller velg en verdi i Poengberegningsmetode-feltet.</span><span class="sxs-lookup"><span data-stu-id="b66e5-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="b66e5-128">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="b66e5-128">Click OK.</span></span>
9. <span data-ttu-id="b66e5-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b66e5-129">Close the page.</span></span>

