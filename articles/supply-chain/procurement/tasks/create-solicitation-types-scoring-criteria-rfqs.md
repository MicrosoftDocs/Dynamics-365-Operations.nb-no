--- 
title: "Opprette forespørselstyper og poengkriterier for tilbudsforespørsler"
description: "Denne veiledningen viser hvordan du oppretter en forespørsels og knytter den til en poengberegningsmetode."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 095855d552d228375635bdbaa9fca37c47a3b952
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="161b0-103">Opprette forespørselstyper og poengkriterier for tilbudsforespørsler</span><span class="sxs-lookup"><span data-stu-id="161b0-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="161b0-104">Denne veiledningen viser hvordan du oppretter en forespørsels og knytter den til en poengberegningsmetode.</span><span class="sxs-lookup"><span data-stu-id="161b0-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="161b0-105">Den viser også hvordan du bruker forespørselstypen på en tilbudsforespørsel som deretter angir standard poengberegningsmetode.</span><span class="sxs-lookup"><span data-stu-id="161b0-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="161b0-106">Disse oppgavene vil vanligvis utføres av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="161b0-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="161b0-107">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="161b0-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="161b0-108">Du må ha en poengberegningsmetode før du begynner.</span><span class="sxs-lookup"><span data-stu-id="161b0-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="161b0-109">Opprette en forespørselstype</span><span class="sxs-lookup"><span data-stu-id="161b0-109">Create a solicitation type</span></span>
1. <span data-ttu-id="161b0-110">Gå til Innkjøp og leverandører > Oppsett > Tilbudsforespørsel > Forespørselstype.</span><span class="sxs-lookup"><span data-stu-id="161b0-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="161b0-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="161b0-111">Click New.</span></span>
3. <span data-ttu-id="161b0-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="161b0-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="161b0-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="161b0-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="161b0-114">I feltet Poengberegningsmetode velger du poengberegningsmetoden du vil bruke for denne forespørselstypen.</span><span class="sxs-lookup"><span data-stu-id="161b0-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="161b0-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="161b0-115">Click Save.</span></span>
7. <span data-ttu-id="161b0-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="161b0-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="161b0-117">Bruke forespørselstypen</span><span class="sxs-lookup"><span data-stu-id="161b0-117">Use the solicitation type</span></span>
1. <span data-ttu-id="161b0-118">Gå til Innkjøp og leverandører > Tilbudsforespørsler > Alle tilbudsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="161b0-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="161b0-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="161b0-119">Click New.</span></span>
3. <span data-ttu-id="161b0-120">I Forespørselstype-feltet velger du forespørselstypen som du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="161b0-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
4. <span data-ttu-id="161b0-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="161b0-121">Click OK.</span></span>
5. <span data-ttu-id="161b0-122">Klikk Poengkriterier.</span><span class="sxs-lookup"><span data-stu-id="161b0-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="161b0-123">Poengkriteriene som vises, er de fra poengberegningsmetoden som du knyttet til forespørselstypen.</span><span class="sxs-lookup"><span data-stu-id="161b0-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="161b0-124">Du kan velge å legge til eller slette kriteriene på denne siden.</span><span class="sxs-lookup"><span data-stu-id="161b0-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="161b0-125">Du kan også legge til nye kriterier ved å kopiere dem fra andre poengberegningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="161b0-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="161b0-126">Klikk Kopier kriterier.</span><span class="sxs-lookup"><span data-stu-id="161b0-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="161b0-127">Angi eller velg en verdi i Poengberegningsmetode-feltet.</span><span class="sxs-lookup"><span data-stu-id="161b0-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="161b0-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="161b0-128">Click OK.</span></span>
9. <span data-ttu-id="161b0-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="161b0-129">Close the page.</span></span>


