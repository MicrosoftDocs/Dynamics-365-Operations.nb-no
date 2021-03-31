---
title: Klassifiser anleggsmidler på nytt
description: Hvis du vil omklassifisere et anleggsmiddel, må du overføre det til den nye anleggsmiddelgruppen, eller gi det et nytt anleggsmiddelnummer i samme gruppe.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85132ee72a72c712f726bec9e3450dbd4e1d8f0b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224723"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="2a247-103">Klassifiser anleggsmidler på nytt</span><span class="sxs-lookup"><span data-stu-id="2a247-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2a247-104">Hvis du vil omklassifisere et anleggsmiddel, må du overføre det til den nye anleggsmiddelgruppen, eller gi det et nytt anleggsmiddelnummer i samme gruppe.</span><span class="sxs-lookup"><span data-stu-id="2a247-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="2a247-105">Når et anleggsmiddel er omklassifisert:</span><span class="sxs-lookup"><span data-stu-id="2a247-105">When a fixed asset is reclassified:</span></span>

* <span data-ttu-id="2a247-106">Alle tablåer for det eksisterende anleggsmiddelet opprettes for det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="2a247-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="2a247-107">All informasjon som ble definert for det originale anleggsmiddelet, kopieres til det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="2a247-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="2a247-108">Statusen til tablåene til det originale anleggsmiddelet er Lukket.</span><span class="sxs-lookup"><span data-stu-id="2a247-108">The status of the books for the original fixed asset is Closed.</span></span> 

* <span data-ttu-id="2a247-109">De nye tablåene til det nye anleggsmiddelet inneholder omklassifiseringsdatoen i **Anskaffelsesdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2a247-109">The new books of the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="2a247-110">Datoen i feltet **Startdato for avskrivning** kopieres fra den opprinnelige anleggsmiddelinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="2a247-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="2a247-111">Hvis avskrivningen allerede har begynt, viser feltet **Datoen da avskrivningen sist ble kjørt** omklassifiseringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="2a247-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

* <span data-ttu-id="2a247-112">De eksisterende anleggsmiddeltransaksjonene for det originale anleggsmiddelet avlyses og genereres på nytt for det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="2a247-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

<span data-ttu-id="2a247-113">Følg disse trinnene for å omklassifisere et anleggsmiddel:</span><span class="sxs-lookup"><span data-stu-id="2a247-113">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="2a247-114">Gå til **Anleggsmidler > Periodiske oppgaver > Omklassifisering**.</span><span class="sxs-lookup"><span data-stu-id="2a247-114">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="2a247-115">I feltet **Anleggsmiddelgruppe** velger du gruppen som skal omklassifiseres.</span><span class="sxs-lookup"><span data-stu-id="2a247-115">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="2a247-116">I feltet **Anleggsmiddelnummer** velger du anleggsmidlet som skal omklassifiseres.</span><span class="sxs-lookup"><span data-stu-id="2a247-116">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="2a247-117">Velg en gruppe som anleggsmidlet skal overføres til, i feltet **Ny anleggsmiddelgruppe**.</span><span class="sxs-lookup"><span data-stu-id="2a247-117">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="2a247-118">Hvis den nye anleggsmiddelgruppen er knyttet til en nummerserie, oppdateres feltet **Nytt anleggsmiddelnummer** med nummeret fra nummerserien til den nye anleggsmiddelgruppen.</span><span class="sxs-lookup"><span data-stu-id="2a247-118">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="2a247-119">Ellers oppdateres feltet **Nytt anleggsmiddelnummer** med nummeret fra nummerserien som er definert på siden **Parametere for anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="2a247-119">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="2a247-120">Hvis en nummerserie ikke er definert på siden **Parametere for anleggsmidler**, angir du et nummer i feltet **Nytt anleggsmiddelnummer**.</span><span class="sxs-lookup"><span data-stu-id="2a247-120">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="2a247-121">Angi en dato i feltet **Omklassifiseringsdato**.</span><span class="sxs-lookup"><span data-stu-id="2a247-121">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="2a247-122">Angi eller velg en verdi i feltet **Bilagsserie**.</span><span class="sxs-lookup"><span data-stu-id="2a247-122">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="2a247-123">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a247-123">Click **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]