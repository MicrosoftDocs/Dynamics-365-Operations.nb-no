---
title: Opprette forespørselstyper og poengkriterier for tilbudsforespørsler
description: Denne veiledningen viser hvordan du oppretter en forespørsels og knytter den til en poengberegningsmetode.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b3876238a191cbbacc4e8c435bb798232e6fd6f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204683"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="a3884-103">Opprette forespørselstyper og poengkriterier for tilbudsforespørsler</span><span class="sxs-lookup"><span data-stu-id="a3884-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a3884-104">Denne veiledningen viser hvordan du oppretter en forespørsels og knytter den til en poengberegningsmetode.</span><span class="sxs-lookup"><span data-stu-id="a3884-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="a3884-105">Den viser også hvordan du bruker forespørselstypen på en tilbudsforespørsel som deretter angir standard poengberegningsmetode.</span><span class="sxs-lookup"><span data-stu-id="a3884-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="a3884-106">Disse oppgavene vil vanligvis utføres av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="a3884-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="a3884-107">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="a3884-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="a3884-108">Du må ha en poengberegningsmetode før du begynner.</span><span class="sxs-lookup"><span data-stu-id="a3884-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="a3884-109">Opprette en forespørselstype</span><span class="sxs-lookup"><span data-stu-id="a3884-109">Create a solicitation type</span></span>
1. <span data-ttu-id="a3884-110">Gå til Innkjøp og leverandører > Oppsett > Tilbudsforespørsel > Forespørselstype.</span><span class="sxs-lookup"><span data-stu-id="a3884-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="a3884-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="a3884-111">Click New.</span></span>
3. <span data-ttu-id="a3884-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3884-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a3884-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="a3884-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a3884-114">I feltet Poengberegningsmetode velger du poengberegningsmetoden du vil bruke for denne forespørselstypen.</span><span class="sxs-lookup"><span data-stu-id="a3884-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="a3884-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="a3884-115">Click Save.</span></span>
7. <span data-ttu-id="a3884-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a3884-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="a3884-117">Bruke forespørselstypen</span><span class="sxs-lookup"><span data-stu-id="a3884-117">Use the solicitation type</span></span>
1. <span data-ttu-id="a3884-118">Gå til Innkjøp og leverandører > Tilbudsforespørsler > Alle tilbudsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="a3884-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="a3884-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="a3884-119">Click New.</span></span>
3. <span data-ttu-id="a3884-120">I Forespørselstype-feltet velger du forespørselstypen som du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="a3884-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="a3884-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a3884-121">Click OK.</span></span>
5. <span data-ttu-id="a3884-122">Klikk Poengkriterier.</span><span class="sxs-lookup"><span data-stu-id="a3884-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="a3884-123">Poengkriteriene som vises, er de fra poengberegningsmetoden som du knyttet til forespørselstypen.</span><span class="sxs-lookup"><span data-stu-id="a3884-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="a3884-124">Du kan velge å legge til eller slette kriteriene på denne siden.</span><span class="sxs-lookup"><span data-stu-id="a3884-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="a3884-125">Du kan også legge til nye kriterier ved å kopiere dem fra andre poengberegningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="a3884-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="a3884-126">Klikk Kopier kriterier.</span><span class="sxs-lookup"><span data-stu-id="a3884-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="a3884-127">Angi eller velg en verdi i Poengberegningsmetode-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3884-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="a3884-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a3884-128">Click OK.</span></span>
9. <span data-ttu-id="a3884-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a3884-129">Close the page.</span></span>

