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
ms.openlocfilehash: 500aa71e57f9c1ac8d1a2a080468381bc248741c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187021"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="89198-103">Beregne avskrivning av anleggsmidler på tvers av juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="89198-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89198-104">Avskrivning av anleggsmidler kan kjøres på tvers av juridiske enheter i ett enkelt trinn.</span><span class="sxs-lookup"><span data-stu-id="89198-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="89198-105">Denne prosedyren viser deg hvordan du definerer og kjører prosessen for flere juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="89198-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="89198-106">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="89198-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="89198-107">Definere journaler for avskrivningskjøring på tvers av firmaet</span><span class="sxs-lookup"><span data-stu-id="89198-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="89198-108">Gå til Anleggsmidler > Oppsett > Parametere for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="89198-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="89198-109">Vis delen Forslag til anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="89198-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="89198-110">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="89198-110">Click Add.</span></span>
4. <span data-ttu-id="89198-111">Angi eller velg en verdi i Posteringslag-feltet.</span><span class="sxs-lookup"><span data-stu-id="89198-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="89198-112">Angi eller velg en verdi i feltet Journalnavn.</span><span class="sxs-lookup"><span data-stu-id="89198-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="89198-113">Gjenta journaloppsettet på siden Parametere for anleggsmidler i hver juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="89198-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="89198-114">Avskrivningskjøring</span><span class="sxs-lookup"><span data-stu-id="89198-114">Depreciation run</span></span>
1. <span data-ttu-id="89198-115">Gå til Anleggsmidler > Journaloppføringer > Opprett avskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="89198-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="89198-116">Angi eller velg en verdi i Posteringslag-feltet.</span><span class="sxs-lookup"><span data-stu-id="89198-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="89198-117">Journalnavnet brukes som standard fra Parametere for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="89198-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="89198-118">Det kan endres her for gjeldende juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="89198-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="89198-119">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="89198-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="89198-120">Velg de juridiske enhetene som skal inkluderes i avskrivningskjøringen.</span><span class="sxs-lookup"><span data-stu-id="89198-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="89198-121">Bare juridiske enheter med journaler som er definert for Forslag til anleggsmidler på siden Parametere for anleggsmidler vises i listen.</span><span class="sxs-lookup"><span data-stu-id="89198-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="89198-122">Velg Ja i feltet Poster journaler.</span><span class="sxs-lookup"><span data-stu-id="89198-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="89198-123">Filtreringsfeltene inkluderer alle anleggsmidler, grupper og tablåer for de juridiske enhetene som er valgt for denne avskrivningskjøringen.</span><span class="sxs-lookup"><span data-stu-id="89198-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="89198-124">Alternativet Satsvis behandling er aktivert som standard.</span><span class="sxs-lookup"><span data-stu-id="89198-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="89198-125">Når dette alternativet er aktivert, vil oppretting og postering av avskrivningsjournalen kjøres i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="89198-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="89198-126">Klikk Opprett journal.</span><span class="sxs-lookup"><span data-stu-id="89198-126">Click Create journal.</span></span>
6. <span data-ttu-id="89198-127">Gå til Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal.</span><span class="sxs-lookup"><span data-stu-id="89198-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

