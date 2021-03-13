---
title: Opprette en poengsummetode for tilbudsforespørsler
description: Denne fremgangsmåten viser hvordan du oppretter en poengberegningsmetode.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 738768a6756db83a6855756ef48fffb4a5874b4a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021385"
---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="9922f-103">Opprette en poengsummetode for tilbudsforespørsler</span><span class="sxs-lookup"><span data-stu-id="9922f-103">Create a scoring method for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9922f-104">Denne fremgangsmåten viser hvordan du oppretter en poengberegningsmetode.</span><span class="sxs-lookup"><span data-stu-id="9922f-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="9922f-105">En poengberegningsmetode er et sett med kriterier som kan brukes til å sammenligne tilbud som sendes i svar på en tilbudsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="9922f-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="9922f-106">Det kan for eksempel være aktuelt å vurdere en leverandør basert på tidligere ytelse, vurdere om firmaet er miljøvennlig eller en god samarbeidspartner, eller du vil sammenligne bud basert på pris.</span><span class="sxs-lookup"><span data-stu-id="9922f-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="9922f-107">Poengberegningsmetoden kan være knyttet til en forespørselstype som standard poengberegningsmetode for tilbudsforespørsler av denne typen.</span><span class="sxs-lookup"><span data-stu-id="9922f-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="9922f-108">Disse oppgavene vil vanligvis utføres av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="9922f-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="9922f-109">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="9922f-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="9922f-110">Gå til Innkjøp og leverandører > Oppsett > Tilbudsforespørsel > Poengberegningsmetode.</span><span class="sxs-lookup"><span data-stu-id="9922f-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="9922f-111">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="9922f-111">Click New.</span></span>
3. <span data-ttu-id="9922f-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9922f-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9922f-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="9922f-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9922f-114">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="9922f-114">Click Save.</span></span>
6. <span data-ttu-id="9922f-115">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="9922f-115">Click New.</span></span>
7. <span data-ttu-id="9922f-116">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9922f-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="9922f-117">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="9922f-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="9922f-118">Denne beskrivelsen vises sammen med navnet på poengberegningsmetoden når en poengberegningsmetode er valgt for en tilbudsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="9922f-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="9922f-119">Angi et tall i Område fra-feltet.</span><span class="sxs-lookup"><span data-stu-id="9922f-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="9922f-120">Området begrenser hva Innkjøpsansvarlig kan skrive inn som poeng.</span><span class="sxs-lookup"><span data-stu-id="9922f-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="9922f-121">Når det er flere poengkriterier i en tilbudsforespørsel, vil de angitte poengsummene legges sammen, og summen gjøres tilgjengelig slik at bud kan sammenlignes.</span><span class="sxs-lookup"><span data-stu-id="9922f-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="9922f-122">Angi et tall i Område til-feltet.</span><span class="sxs-lookup"><span data-stu-id="9922f-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="9922f-123">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="9922f-123">Click New.</span></span>
12. <span data-ttu-id="9922f-124">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9922f-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="9922f-125">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="9922f-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="9922f-126">Angi et tall i Område fra-feltet.</span><span class="sxs-lookup"><span data-stu-id="9922f-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="9922f-127">Angi et tall i Område til-feltet.</span><span class="sxs-lookup"><span data-stu-id="9922f-127">In the Range to field, enter a number.</span></span>

