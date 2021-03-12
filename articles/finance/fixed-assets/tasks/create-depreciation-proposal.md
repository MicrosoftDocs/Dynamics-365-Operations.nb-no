---
title: Opprette et avskrivningsforslag
description: Dette emnet beskriver hvordan satsvise avskrivningsforslag fungerer, og forklarer hvordan du foreslår avskrivning for anleggsmidler.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3d62e982d26afbec7ac04dd80592a73f4a3286f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968910"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="9be2a-103">Opprette et avskrivningsforslag</span><span class="sxs-lookup"><span data-stu-id="9be2a-103">Create a depreciation proposal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9be2a-104">Dette emnet beskriver hvordan satsvise avskrivningsforslag fungerer, og forklarer hvordan du foreslår avskrivning for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="9be2a-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="9be2a-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF og regnskapsførerrollen.</span><span class="sxs-lookup"><span data-stu-id="9be2a-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="9be2a-106">Opprette et avskrivningsforslag</span><span class="sxs-lookup"><span data-stu-id="9be2a-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="9be2a-107">I navigasjonsruten går du til **Moduler > Anleggsmidler > Journaloppføringer > Opprette avskrivningsforslag**.</span><span class="sxs-lookup"><span data-stu-id="9be2a-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="9be2a-108">I **Journalnavn**-feltet velger du et alternativ fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="9be2a-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="9be2a-109">Angi en dato i **Til dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9be2a-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="9be2a-110">Velg alternativet **Summer avskrivning** for å summere månedlige avskrivninger i én journallinje.</span><span class="sxs-lookup"><span data-stu-id="9be2a-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="9be2a-111">Hvis for eksempel verdien for Til-dato er 31. mars 2015, genereres følgende beskrivelse: "Avskrivninger siden 31. januar 2015."</span><span class="sxs-lookup"><span data-stu-id="9be2a-111">For example, if the To date value is March 31, 2015, the following description is generated: "Depreciation since January 31, 2015."</span></span> <span data-ttu-id="9be2a-112">**Dato**-feltet i de foreslåtte journallinjene settes deretter til 31. mars 2015.</span><span class="sxs-lookup"><span data-stu-id="9be2a-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="9be2a-113">Avskrivningsforslaget kan filtreres etter anleggsmiddel, anleggsmiddelgruppe eller andre kriterier ved hjelp av alternativet for **filtrering**.</span><span class="sxs-lookup"><span data-stu-id="9be2a-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="9be2a-114">Når du bruker skjemaet **Opprett anskaffelses- eller avskrivningsforslag for anleggsmiddel**, kan du foreslå avskrivning i grupper.</span><span class="sxs-lookup"><span data-stu-id="9be2a-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="9be2a-115">Dette anbefales for større forslag som bruker flere systemressurser.</span><span class="sxs-lookup"><span data-stu-id="9be2a-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="9be2a-116">Hvis du velger partialternativet, kan du fortsatt fullføre andre oppgaver i denne perioden.</span><span class="sxs-lookup"><span data-stu-id="9be2a-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="9be2a-117">Når du foreslår avskrivning på denne måten, beregnes avskrivning for verdimodeller for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="9be2a-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="9be2a-118">Velg **Opprett journal**.</span><span class="sxs-lookup"><span data-stu-id="9be2a-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="9be2a-119">Vise avskrivningsposter</span><span class="sxs-lookup"><span data-stu-id="9be2a-119">Review depreciation entries</span></span>
1. <span data-ttu-id="9be2a-120">I navigasjonsruten går du til **Moduler > Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal**.</span><span class="sxs-lookup"><span data-stu-id="9be2a-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="9be2a-121">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9be2a-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9be2a-122">Velg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="9be2a-122">Select **Lines**.</span></span>
4. <span data-ttu-id="9be2a-123">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="9be2a-123">Select **Post**.</span></span>

