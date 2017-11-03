---
title: Postere anleggsmiddeltransaksjoner til posteringslag
description: Denne artikkelen gir en oversikt over posteringslag for anleggsmiddeltransaksjoner.
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b210bddf640dff2d65e2aec63a18c27acebdc5a8
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="1008d-103">Postere anleggsmiddeltransaksjoner til posteringslag</span><span class="sxs-lookup"><span data-stu-id="1008d-103">Post fixed asset transactions to posting layers</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1008d-104">Denne artikkelen gir en oversikt over posteringslag for anleggsmiddeltransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="1008d-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="1008d-105">Anleggsmidler avskrives ofte på forskjellige måte for forskjellige formål.</span><span class="sxs-lookup"><span data-stu-id="1008d-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="1008d-106">Avskrivning for skatte- og avgiftsformål beregnes ved hjelp av gjeldende skatteregler for å oppnå høyest mulig avskrivning for skatter og avgifter, mens avskrivning for rapporteringsformål beregnes i henhold til regnskapslover og standarder.</span><span class="sxs-lookup"><span data-stu-id="1008d-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="1008d-107">De forskjellige typene avskrivning beregnes og registreres separat i posteringslagene.</span><span class="sxs-lookup"><span data-stu-id="1008d-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="1008d-108">Hvert tablå som er knyttet til et anleggsmiddel, er definert for et bestemt posteringslag som inneholder det totale avskrivningsmålet.</span><span class="sxs-lookup"><span data-stu-id="1008d-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="1008d-109">Det finnes ti posteringslag: gjeldende, operasjoner, mva og sju egendefinert lag.</span><span class="sxs-lookup"><span data-stu-id="1008d-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="1008d-110">Du kan også deaktivere postering i Finans for tablået ved å sette Poster i økonomimodul til Nei.</span><span class="sxs-lookup"><span data-stu-id="1008d-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="1008d-111">Feltet Posteringslag settes deretter automatisk til Ingen.</span><span class="sxs-lookup"><span data-stu-id="1008d-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="1008d-112">Tablåer som ikke posteres i Finans brukes vanligvis for mva-rapporteringsformål.</span><span class="sxs-lookup"><span data-stu-id="1008d-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="1008d-113">Dette gir deg mer fleksibilitet til å slette historiske transaksjoner for anleggsmiddeltablået fordi de ikke er lagret i Finans.</span><span class="sxs-lookup"><span data-stu-id="1008d-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="1008d-114">Anleggsmiddeljournaler defineres ved hjelp av  Journalnavn-siden under Økonomimodul > Journaloppsett > Journalnavn.</span><span class="sxs-lookup"><span data-stu-id="1008d-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="1008d-115">Hver journal du kan postere avskrivninger i, defineres av journalnavnet for bare ett posteringslag.</span><span class="sxs-lookup"><span data-stu-id="1008d-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="1008d-116">Posteringslaget i journalen kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="1008d-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="1008d-117">Denne begrensningen bidrar til å sikre at transaksjoner for hvert posteringslag holdes separat.</span><span class="sxs-lookup"><span data-stu-id="1008d-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="1008d-118">Minst ett journalnavn må opprettes for hvert posteringslag.</span><span class="sxs-lookup"><span data-stu-id="1008d-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="1008d-119">Hvis du bruker tablåer som ikke posteres til økonomimodulen, må du også opprette en journal der posteringslaget er satt til Ingen.</span><span class="sxs-lookup"><span data-stu-id="1008d-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="1008d-120">Du kan angi finanskontoer for anleggsmiddeltransaksjoner på siden Posteringsprofiler for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="1008d-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="1008d-121">For hver posteringsprofil må du velge den relevante transaksjonstypen og tablået, og deretter angi finanskontoene.</span><span class="sxs-lookup"><span data-stu-id="1008d-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="1008d-122">Definer posteringsprofilposten for hvert tablå som skal posteres til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="1008d-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

> [!NOTE] 
> <span data-ttu-id="1008d-123">Ved å bruke avledede tablåer, kan du postere transaksjoner til forskjellige posteringslag samtidig.</span><span class="sxs-lookup"><span data-stu-id="1008d-123">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="1008d-124">Du oppretter transaksjonene for det primære tablået i en journal der posteringslaget samsvarer med posteringslaget for tablået.</span><span class="sxs-lookup"><span data-stu-id="1008d-124">You create the transactions of the primary book in a journal where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="1008d-125">Under posteringen posteres de avledede tablåtransaksjonene til de respektive posteringslagene.</span><span class="sxs-lookup"><span data-stu-id="1008d-125">During posting, the derived book transactions are posted to the appropriate posting layers.</span></span>

<span data-ttu-id="1008d-126">Hvis du vil ha mer informasjon, kan du se [Avledede bøker](derived-books.md) og [Postering med avledede bøker](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="1008d-126">For more information see, [Derived books](derived-books.md) and [Posting with derived books](post-derived-value-models.md).</span></span>




