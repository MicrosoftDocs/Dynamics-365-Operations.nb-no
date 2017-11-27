--- 
title: "Klassifiser anleggsmidler på nytt"
description: "Hvis du vil omklassifisere et anleggsmiddel, må du overføre det til den nye anleggsmiddelgruppen, eller gi det et nytt anleggsmiddelnummer i samme gruppe."
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cafd499e849570cae7b7f58bf2d487a7ac0093e6
ms.openlocfilehash: 6bce294329c7ec6dc436c3d3baf6597e0283c9bd
ms.contentlocale: nb-no
ms.lasthandoff: 10/30/2017

---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="13e31-103">Klassifiser anleggsmidler på nytt</span><span class="sxs-lookup"><span data-stu-id="13e31-103">Reclassify fixed assets</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="13e31-104">Hvis du vil omklassifisere et anleggsmiddel, må du overføre det til den nye anleggsmiddelgruppen, eller gi det et nytt anleggsmiddelnummer i samme gruppe.</span><span class="sxs-lookup"><span data-stu-id="13e31-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="13e31-105">Når et anleggsmiddel er omklassifisert:</span><span class="sxs-lookup"><span data-stu-id="13e31-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="13e31-106">• Alle verdimodellene til det eksisterende anleggsmiddelet opprettes for det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="13e31-106">• All value models for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="13e31-107">All informasjon som ble definert for det originale anleggsmiddelet, kopieres til det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="13e31-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="13e31-108">Statusen til verdimodellene til den originale anleggsmiddelet er Lukket.</span><span class="sxs-lookup"><span data-stu-id="13e31-108">The status of the value models for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="13e31-109">• De nye verdimodellene til det nye anleggsmiddelet inneholder omklassifiseringsdatoen i Anskaffelsesdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="13e31-109">• The new value models of the new fixed asset contain the date of the reclassification in the Acquisition date field.</span></span> <span data-ttu-id="13e31-110">Datoen i feltet Startdato for avskrivning kopieres fra den opprinnelige anleggsmiddelinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="13e31-110">The date in the Depreciation run date field is copied from the original asset information.</span></span> <span data-ttu-id="13e31-111">Hvis avskrivningen allerede har begynt, viser feltet Datoen da avskrivningen sist ble kjørt omklassifiseringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="13e31-111">If the depreciation has already started, the Date when depreciation was last run field displays the date of the reclassification.</span></span> 

<span data-ttu-id="13e31-112">• De eksisterende anleggsmiddeltransaksjonene for det originale anleggsmiddelet avlyses og genereres på nytt for det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="13e31-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

1. <span data-ttu-id="13e31-113">Gå til Anleggsmidler > Periodiske oppgaver > Omklassifisering.</span><span class="sxs-lookup"><span data-stu-id="13e31-113">Go to Fixed assets > Periodic tasks > Reclassification.</span></span>
2. <span data-ttu-id="13e31-114">I feltet Anleggsmiddelgruppe velger du gruppen som skal omklassifiseres.</span><span class="sxs-lookup"><span data-stu-id="13e31-114">In the Fixed asset group field, select the group to reclassify.</span></span>
3. <span data-ttu-id="13e31-115">I feltet Anleggsmiddelnummer velger du anleggsmidlet som skal omklassifiseres.</span><span class="sxs-lookup"><span data-stu-id="13e31-115">In the Fixed asset number field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="13e31-116">Velg en gruppe som anleggsmidlet skal overføres til, i feltet Ny anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="13e31-116">In the New fixed asset group field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="13e31-117">Hvis den nye anleggsmiddelgruppen er knyttet til en nummerserie, oppdateres feltet Nytt anleggsmiddelnummer med nummeret fra nummerserien til den nye anleggsmiddelgruppen.</span><span class="sxs-lookup"><span data-stu-id="13e31-117">If the new fixed asset group is attached to a number sequence, the New fixed asset number field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="13e31-118">Ellers oppdateres feltet Nytt anleggsmiddelnummer med nummeret fra nummerserien som er definert på siden Parametere for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="13e31-118">Otherwise, the New fixed asset number field is updated with the number from the number sequence that is set up in the Fixed asset parameters page.</span></span> <span data-ttu-id="13e31-119">Hvis en nummerserie ikke er definert på siden Parametere for anleggsmidler, angir du et nummer i feltet Nytt anleggsmiddelnummer.</span><span class="sxs-lookup"><span data-stu-id="13e31-119">If a number sequence is not set up in the Fixed asset parameters page, enter a number in the New fixed asset number field.</span></span>  
5. <span data-ttu-id="13e31-120">Angi en dato i feltet Omklassifiseringsdato.</span><span class="sxs-lookup"><span data-stu-id="13e31-120">In the Reclassification date field, enter a date.</span></span>
6. <span data-ttu-id="13e31-121">Angi eller velg en verdi i feltet Bilagsserie.</span><span class="sxs-lookup"><span data-stu-id="13e31-121">In the Voucher series field, enter or select a value.</span></span>
7. <span data-ttu-id="13e31-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="13e31-122">Click OK.</span></span>


