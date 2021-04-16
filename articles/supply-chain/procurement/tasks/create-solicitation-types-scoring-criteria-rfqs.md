---
title: Opprette forespørselstyper og poengkriterier for tilbudsforespørsler
description: Denne veiledningen viser hvordan du oppretter en forespørsels og knytter den til en poengberegningsmetode.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d28cb4bf20ba50aae6b85e835339e2df711c99d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812068"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="f0a97-103">Opprette forespørselstyper og poengkriterier for tilbudsforespørsler</span><span class="sxs-lookup"><span data-stu-id="f0a97-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0a97-104">Denne veiledningen viser hvordan du oppretter en forespørsels og knytter den til en poengberegningsmetode.</span><span class="sxs-lookup"><span data-stu-id="f0a97-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="f0a97-105">Den viser også hvordan du bruker forespørselstypen på en tilbudsforespørsel som deretter angir standard poengberegningsmetode.</span><span class="sxs-lookup"><span data-stu-id="f0a97-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="f0a97-106">Disse oppgavene vil vanligvis utføres av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="f0a97-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="f0a97-107">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="f0a97-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="f0a97-108">Du må ha en poengberegningsmetode før du begynner.</span><span class="sxs-lookup"><span data-stu-id="f0a97-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="f0a97-109">Opprette en forespørselstype</span><span class="sxs-lookup"><span data-stu-id="f0a97-109">Create a solicitation type</span></span>
1. <span data-ttu-id="f0a97-110">Gå til Innkjøp og leverandører > Oppsett > Tilbudsforespørsel > Forespørselstype.</span><span class="sxs-lookup"><span data-stu-id="f0a97-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="f0a97-111">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f0a97-111">Click New.</span></span>
3. <span data-ttu-id="f0a97-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f0a97-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f0a97-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f0a97-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f0a97-114">I feltet Poengberegningsmetode velger du poengberegningsmetoden du vil bruke for denne forespørselstypen.</span><span class="sxs-lookup"><span data-stu-id="f0a97-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="f0a97-115">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="f0a97-115">Click Save.</span></span>
7. <span data-ttu-id="f0a97-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f0a97-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="f0a97-117">Bruke forespørselstypen</span><span class="sxs-lookup"><span data-stu-id="f0a97-117">Use the solicitation type</span></span>
1. <span data-ttu-id="f0a97-118">Gå til Innkjøp og leverandører > Tilbudsforespørsler > Alle tilbudsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="f0a97-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="f0a97-119">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f0a97-119">Click New.</span></span>
3. <span data-ttu-id="f0a97-120">I Forespørselstype-feltet velger du forespørselstypen som du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="f0a97-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="f0a97-121">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f0a97-121">Click OK.</span></span>
5. <span data-ttu-id="f0a97-122">Klikk på Poengkriterier.</span><span class="sxs-lookup"><span data-stu-id="f0a97-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="f0a97-123">Poengkriteriene som vises, er de fra poengberegningsmetoden som du knyttet til forespørselstypen.</span><span class="sxs-lookup"><span data-stu-id="f0a97-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="f0a97-124">Du kan velge å legge til eller slette kriteriene på denne siden.</span><span class="sxs-lookup"><span data-stu-id="f0a97-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="f0a97-125">Du kan også legge til nye kriterier ved å kopiere dem fra andre poengberegningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="f0a97-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="f0a97-126">Klikk på Kopier kriterier.</span><span class="sxs-lookup"><span data-stu-id="f0a97-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="f0a97-127">Angi eller velg en verdi i Poengberegningsmetode-feltet.</span><span class="sxs-lookup"><span data-stu-id="f0a97-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="f0a97-128">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f0a97-128">Click OK.</span></span>
9. <span data-ttu-id="f0a97-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f0a97-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]