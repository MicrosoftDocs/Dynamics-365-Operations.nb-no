--- 
title: Opprette et avskrivningsforslag
description: "Denne fremgangsmåten beskriver hvordan satsvise avskrivningsforslag fungerer, og forklarer hvordan du foreslår avskrivning for anleggsmidler."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 07d8cf2f1c46b99dfcd1d7c3419fe835f37c5a02
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="4ddd3-103">Opprette et avskrivningsforslag</span><span class="sxs-lookup"><span data-stu-id="4ddd3-103">Create a depreciation proposal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4ddd3-104">Denne fremgangsmåten beskriver hvordan satsvise avskrivningsforslag fungerer, og forklarer hvordan du foreslår avskrivning for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="4ddd3-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF og regnskapsførerrollen.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="4ddd3-106">Opprett avskrivningsforslag</span><span class="sxs-lookup"><span data-stu-id="4ddd3-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="4ddd3-107">Gå til Anleggsmidler > Journaloppføringer > Opprett avskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="4ddd3-108">Klikk rullegardinknappen i feltet Journalnavn for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="4ddd3-109">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4ddd3-110">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="4ddd3-111">Velg alternativet Summer avskrivning for å summere månedlige avskrivninger i én journallinje.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="4ddd3-112">Hvis for eksempel verdien for Til-dato er 31. mars 2015, genereres følgende beskrivelse: "Avskrivninger siden 31. januar 2015."</span><span class="sxs-lookup"><span data-stu-id="4ddd3-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="4ddd3-113">Datofeltet i de foreslåtte journallinjene settes deretter til 31. mars 2015.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="4ddd3-114">Avskrivningsforslaget kan filtreres etter anleggsmiddel, anleggsmiddelgruppe eller andre kriterier ved hjelp av alternativet for filtrering.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="4ddd3-115">Når du bruker Opprett anskaffelses- eller avskrivningsforslag for anleggsmiddelskjemaet, kan du foreslå avskrivning i grupper.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="4ddd3-116">Dette anbefales for større forslag som bruker flere systemressurser.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="4ddd3-117">Hvis du velger partialternativet, kan du fortsatt fullføre andre oppgaver i denne perioden.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="4ddd3-118">Når du foreslår avskrivning på denne måten, beregnes avskrivning for verdimodeller for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="4ddd3-119">Klikk Opprett journal.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="4ddd3-120">Vise avskrivningsposter</span><span class="sxs-lookup"><span data-stu-id="4ddd3-120">Review depreciation entries</span></span>
1. <span data-ttu-id="4ddd3-121">Gå til Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="4ddd3-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4ddd3-123">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-123">Click Lines.</span></span>
4. <span data-ttu-id="4ddd3-124">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="4ddd3-124">Click Post.</span></span>


