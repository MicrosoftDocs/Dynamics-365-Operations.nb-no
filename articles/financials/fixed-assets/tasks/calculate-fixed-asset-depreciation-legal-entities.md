--- 
title: "Beregne avskrivning av anleggsmidler på tvers av juridiske enheter"
description: "Denne prosedyren viser deg hvordan du definerer og kjører avskrivningsprosessen for flere juridiske enheter."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 4221acf200f41ca39803bcd56c1b05e0d87bd948
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="db6e3-103">Beregne avskrivning av anleggsmidler på tvers av juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="db6e3-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="db6e3-104">Avskrivning av anleggsmidler kan kjøres på tvers av juridiske enheter i ett enkelt trinn.</span><span class="sxs-lookup"><span data-stu-id="db6e3-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="db6e3-105">Denne prosedyren viser deg hvordan du definerer og kjører prosessen for flere juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="db6e3-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="db6e3-106">Den bruker regnskapsførerrollen.</span><span class="sxs-lookup"><span data-stu-id="db6e3-106">It uses the accountant role.</span></span>  

<span data-ttu-id="db6e3-107">Denne registreringen bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="db6e3-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="db6e3-108">Underoppgave trinn (16): Definer journaler for avskrivningskjøring på tvers av firmaet.</span><span class="sxs-lookup"><span data-stu-id="db6e3-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="db6e3-109">Du må først definere journalene som skal brukes i avskrivningskjøring på tvers av firmaet for hver juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="db6e3-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="db6e3-110">Gå til Anleggsmidler > Oppsett > Parametere for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="db6e3-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="db6e3-111">Vis delen Forslag til anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="db6e3-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="db6e3-112">Opprette en post med journalnavnet som skal brukes for hvert posteringslag i den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="db6e3-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="db6e3-113">Hvis tablåer ikke posterer til finans, skal Ingen postering-laget velges med tilhørende journal.</span><span class="sxs-lookup"><span data-stu-id="db6e3-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="db6e3-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="db6e3-114">Click Add.</span></span> 
4. <span data-ttu-id="db6e3-115">Angi eller velg en verdi i Posteringslag-feltet.</span><span class="sxs-lookup"><span data-stu-id="db6e3-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="db6e3-116">Angi eller velg en verdi i feltet Journalnavn.</span><span class="sxs-lookup"><span data-stu-id="db6e3-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="db6e3-117">Gjenta journaloppsettet på siden Parametere for anleggsmidler i hver juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="db6e3-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="db6e3-118">Underoppgave: Beregne avskrivining.</span><span class="sxs-lookup"><span data-stu-id="db6e3-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="db6e3-119">Bruk siden Opprett avskrivningsforslag til å starte avskrivning på tvers av juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="db6e3-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="db6e3-120">Gå til Anleggsmidler > Journaloppføringer > Opprett avskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="db6e3-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="db6e3-121">Angi eller velg en verdi i Posteringslag-feltet.</span><span class="sxs-lookup"><span data-stu-id="db6e3-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="db6e3-122">Journalnavnet brukes som standard fra Parametere for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="db6e3-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="db6e3-123">Det kan endres her for gjeldende juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="db6e3-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="db6e3-124">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="db6e3-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="db6e3-125">Velg de juridiske enhetene som skal inkluderes i avskrivningskjøringen.</span><span class="sxs-lookup"><span data-stu-id="db6e3-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="db6e3-126">Bare juridiske enheter med journaler som er definert for Forslag til anleggsmidler på siden Parametere for anleggsmidler vises i listen.</span><span class="sxs-lookup"><span data-stu-id="db6e3-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="db6e3-127">Når aktivert, vil alternativet Poster journaler automatisk postere avskrivningsjournalene når de opprettes.</span><span class="sxs-lookup"><span data-stu-id="db6e3-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="db6e3-128">Når det ikke er merket, vil journalene bli opprettet, men ikke postert, slik at du kan se gjennom detaljene før postering.</span><span class="sxs-lookup"><span data-stu-id="db6e3-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="db6e3-129">Velg Ja i feltet Poster journaler.</span><span class="sxs-lookup"><span data-stu-id="db6e3-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="db6e3-130">Filtreringsfeltene inkluderer alle anleggsmidler, grupper og tablåer for de juridiske enhetene som er valgt for denne avskrivningskjøringen.</span><span class="sxs-lookup"><span data-stu-id="db6e3-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="db6e3-131">Alternativet Satsvis behandling er aktivert som standard.</span><span class="sxs-lookup"><span data-stu-id="db6e3-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="db6e3-132">Når dette alternativet er aktivert, vil oppretting og postering av avskrivningsjournalen kjøres i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="db6e3-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="db6e3-133">Klikk Opprett journal.</span><span class="sxs-lookup"><span data-stu-id="db6e3-133">Click Create journal.</span></span> 
10. <span data-ttu-id="db6e3-134">Du må vise avskrivningsjournalene som er opprettet i de respektive juridiske enhetene.</span><span class="sxs-lookup"><span data-stu-id="db6e3-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="db6e3-135">Gå til Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal.</span><span class="sxs-lookup"><span data-stu-id="db6e3-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

