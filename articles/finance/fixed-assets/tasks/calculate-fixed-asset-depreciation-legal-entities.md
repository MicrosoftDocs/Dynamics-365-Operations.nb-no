---
title: Beregne avskrivning av anleggsmidler på tvers av juridiske enheter
description: Avskrivning av anleggsmidler kan kjøres på tvers av juridiske enheter i ett enkelt trinn.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 074a1b80584050302920a95c20fb547523a4866c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446253"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="1b1dc-103">Beregne avskrivning av anleggsmidler på tvers av juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="1b1dc-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1b1dc-104">Avskrivning av anleggsmidler kan kjøres på tvers av juridiske enheter i ett enkelt trinn.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="1b1dc-105">Denne prosedyren viser deg hvordan du definerer og kjører prosessen for flere juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="1b1dc-106">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="1b1dc-107">Definere journaler for avskrivningskjøring på tvers av firmaet</span><span class="sxs-lookup"><span data-stu-id="1b1dc-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="1b1dc-108">Gå til Anleggsmidler > Oppsett > Parametere for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="1b1dc-109">Vis delen Forslag til anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="1b1dc-110">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-110">Click Add.</span></span>
4. <span data-ttu-id="1b1dc-111">Angi eller velg en verdi i Posteringslag-feltet.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="1b1dc-112">Angi eller velg en verdi i feltet Journalnavn.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="1b1dc-113">Gjenta journaloppsettet på siden Parametere for anleggsmidler i hver juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="1b1dc-114">Avskrivningskjøring</span><span class="sxs-lookup"><span data-stu-id="1b1dc-114">Depreciation run</span></span>
1. <span data-ttu-id="1b1dc-115">Gå til Anleggsmidler > Journaloppføringer > Opprett avskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="1b1dc-116">Angi eller velg en verdi i Posteringslag-feltet.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="1b1dc-117">Journalnavnet brukes som standard fra Parametere for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="1b1dc-118">Det kan endres her for gjeldende juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="1b1dc-119">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="1b1dc-120">Velg de juridiske enhetene som skal inkluderes i avskrivningskjøringen.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="1b1dc-121">Bare juridiske enheter med journaler som er definert for Forslag til anleggsmidler på siden Parametere for anleggsmidler vises i listen.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="1b1dc-122">Velg Ja i feltet Poster journaler.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="1b1dc-123">Filtreringsfeltene inkluderer alle anleggsmidler, grupper og tablåer for de juridiske enhetene som er valgt for denne avskrivningskjøringen.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="1b1dc-124">Alternativet Satsvis behandling er aktivert som standard.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="1b1dc-125">Når dette alternativet er aktivert, vil oppretting og postering av avskrivningsjournalen kjøres i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="1b1dc-126">Klikk Opprett journal.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-126">Click Create journal.</span></span>
6. <span data-ttu-id="1b1dc-127">Gå til Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

