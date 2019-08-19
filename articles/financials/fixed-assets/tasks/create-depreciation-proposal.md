---
title: Opprett avskrivningsforslag
description: Denne fremgangsmåten beskriver hvordan satsvise avskrivningsforslag fungerer, og forklarer hvordan du foreslår avskrivning for anleggsmidler.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07146adfe1ead2b6e06e3c323963f8c012381b76
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840007"
---
# <a name="create-depreciation-proposal"></a><span data-ttu-id="0e245-103">Opprett avskrivningsforslag</span><span class="sxs-lookup"><span data-stu-id="0e245-103">Create depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e245-104">Denne fremgangsmåten beskriver hvordan satsvise avskrivningsforslag fungerer, og forklarer hvordan du foreslår avskrivning for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="0e245-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="0e245-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF og regnskapsførerrollen.</span><span class="sxs-lookup"><span data-stu-id="0e245-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="0e245-106">Opprett avskrivningsforslag</span><span class="sxs-lookup"><span data-stu-id="0e245-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="0e245-107">Gå til Anleggsmidler > Journaloppføringer > Opprett avskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="0e245-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="0e245-108">Klikk rullegardinknappen i feltet Journalnavn for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0e245-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0e245-109">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0e245-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0e245-110">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="0e245-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="0e245-111">Velg alternativet Summer avskrivning for å summere månedlige avskrivninger i én journallinje.</span><span class="sxs-lookup"><span data-stu-id="0e245-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="0e245-112">Hvis for eksempel verdien for Til-dato er 31. mars 2015, genereres følgende beskrivelse: "Avskrivninger siden 31. januar 2015."</span><span class="sxs-lookup"><span data-stu-id="0e245-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="0e245-113">Datofeltet i de foreslåtte journallinjene settes deretter til 31. mars 2015.</span><span class="sxs-lookup"><span data-stu-id="0e245-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="0e245-114">Avskrivningsforslaget kan filtreres etter anleggsmiddel, anleggsmiddelgruppe eller andre kriterier ved hjelp av alternativet for filtrering.</span><span class="sxs-lookup"><span data-stu-id="0e245-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="0e245-115">Når du bruker Opprett anskaffelses- eller avskrivningsforslag for anleggsmiddelskjemaet, kan du foreslå avskrivning i grupper.</span><span class="sxs-lookup"><span data-stu-id="0e245-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="0e245-116">Dette anbefales for større forslag som bruker flere systemressurser.</span><span class="sxs-lookup"><span data-stu-id="0e245-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="0e245-117">Hvis du velger partialternativet, kan du fortsatt fullføre andre oppgaver i denne perioden.</span><span class="sxs-lookup"><span data-stu-id="0e245-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="0e245-118">Når du foreslår avskrivning på denne måten, beregnes avskrivning for verdimodeller for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="0e245-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="0e245-119">Klikk Opprett journal.</span><span class="sxs-lookup"><span data-stu-id="0e245-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="0e245-120">Vise avskrivningsposter</span><span class="sxs-lookup"><span data-stu-id="0e245-120">Review depreciation entries</span></span>
1. <span data-ttu-id="0e245-121">Gå til Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal.</span><span class="sxs-lookup"><span data-stu-id="0e245-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="0e245-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0e245-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0e245-123">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="0e245-123">Click Lines.</span></span>
4. <span data-ttu-id="0e245-124">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="0e245-124">Click Post.</span></span>

