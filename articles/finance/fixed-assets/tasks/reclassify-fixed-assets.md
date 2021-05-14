---
title: Klassifiser anleggsmidler på nytt
description: Hvis du vil omklassifisere et anleggsmiddel, må du overføre det til den nye anleggsmiddelgruppen, eller gi det et nytt anleggsmiddelnummer i samme gruppe.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfb754459fad1f3b1509f4f9c65c20e0385b013
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944720"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="2259d-103">Klassifiser anleggsmidler på nytt</span><span class="sxs-lookup"><span data-stu-id="2259d-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2259d-104">Hvis du vil omklassifisere et anleggsmiddel, må du overføre det til den nye anleggsmiddelgruppen, eller gi det et nytt anleggsmiddelnummer i samme gruppe.</span><span class="sxs-lookup"><span data-stu-id="2259d-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="2259d-105">Når et anleggsmiddel er omklassifisert:</span><span class="sxs-lookup"><span data-stu-id="2259d-105">When a fixed asset is reclassified:</span></span>

- <span data-ttu-id="2259d-106">Alle tablåer for det eksisterende anleggsmiddelet opprettes for det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="2259d-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="2259d-107">All informasjon som ble definert for det originale anleggsmiddelet, kopieres til det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="2259d-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="2259d-108">Statusen til tablåene til det originale anleggsmiddelet er Lukket.</span><span class="sxs-lookup"><span data-stu-id="2259d-108">The status of the books for the original fixed asset is Closed.</span></span> 

- <span data-ttu-id="2259d-109">De nye tablåene for det nye anleggsmiddelet inneholder omklassifiseringsdatoen i **Anskaffelsesdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2259d-109">The new books for the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="2259d-110">Datoen i feltet **Startdato for avskrivning** kopieres fra den opprinnelige anleggsmiddelinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="2259d-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="2259d-111">Hvis avskrivningen allerede har begynt, viser feltet **Datoen da avskrivningen sist ble kjørt** omklassifiseringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="2259d-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

- <span data-ttu-id="2259d-112">De eksisterende anleggsmiddeltransaksjonene for det originale anleggsmiddelet avlyses og genereres på nytt for det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="2259d-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

- <span data-ttu-id="2259d-113">Når et anleggsmiddel som har en overføringstransaksjon er omklassifisert, viser systemet en melding i **handlingssenteret** for å angi at en overføringstransaksjon ikke ble fullført under omklassifiseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="2259d-113">When an asset that has a transfer transaction has been reclassified, the system will display a message in the **Action center** to indicate that a transfer transaction wasn't completed during the reclassification process.</span></span> <span data-ttu-id="2259d-114">Det er nødvendig å fullføre en overføringstransaksjon for å flytte de eksisterende omklassifiseringstransaksjonene til de riktige finansdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="2259d-114">It's necessary to complete a transfer transaction to move the existing reclassification transactions to the appropriate financial dimensions.</span></span> 

   <span data-ttu-id="2259d-115">Under omklassifiseringsprosessen kjører systemet følgende handlinger for å omklassifisere anleggsmiddelsaldoen fra det opprinnelige anleggsmiddelet til det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="2259d-115">During the reclassification process, the system runs the following actions to reclassify the asset balance from the original asset to the new asset.</span></span> 
   
   - <span data-ttu-id="2259d-116">Omklassifiseringsprosessen kopierer dataene fra det opprinnelige anleggsmiddeltablået til det nye anleggsmiddeltablået.</span><span class="sxs-lookup"><span data-stu-id="2259d-116">The reclassification process copies the data from the original fixed asset book to the new fixed asset book.</span></span>

   - <span data-ttu-id="2259d-117">Omklassifiseringstransaksjonen bruker informasjon fra den opprinnelige posterte anskaffelsen, som omfatter finansdimensjonsinformasjon som er inkludert i anskaffelsestransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="2259d-117">The reclassification transaction uses information from the original posted acquisition that includes financial dimension information that is included in the acquisition transaction.</span></span>  
   
   - <span data-ttu-id="2259d-118">Samtidig tilbakefører omklassifiseringsprosessen den opprinnelige anleggsmiddelanskaffelsen og anleggsmiddeloverføringstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="2259d-118">At the same time, the reclassification process reverses the original asset acquisition and asset transfer transaction.</span></span> 

<span data-ttu-id="2259d-119">Diagrammet og fremgangsmåten nedenfor gir et eksempel på omklassifiseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="2259d-119">The following diagram and procedure provide an example of the reclassification process.</span></span> 

<span data-ttu-id="2259d-120">[![Diagram som viser omklassifiseringsprosessen](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span><span class="sxs-lookup"><span data-stu-id="2259d-120">[![Diagram showing the reclassicification process](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span></span>

<span data-ttu-id="2259d-121">Følg disse trinnene for å omklassifisere et anleggsmiddel:</span><span class="sxs-lookup"><span data-stu-id="2259d-121">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="2259d-122">Gå til **Anleggsmidler > Periodiske oppgaver > Omklassifisering**.</span><span class="sxs-lookup"><span data-stu-id="2259d-122">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="2259d-123">I feltet **Anleggsmiddelgruppe** velger du gruppen som skal omklassifiseres.</span><span class="sxs-lookup"><span data-stu-id="2259d-123">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="2259d-124">I feltet **Anleggsmiddelnummer** velger du anleggsmidlet som skal omklassifiseres.</span><span class="sxs-lookup"><span data-stu-id="2259d-124">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="2259d-125">Velg en gruppe som anleggsmidlet skal overføres til, i feltet **Ny anleggsmiddelgruppe**.</span><span class="sxs-lookup"><span data-stu-id="2259d-125">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="2259d-126">Hvis den nye anleggsmiddelgruppen er knyttet til en nummerserie, oppdateres feltet **Nytt anleggsmiddelnummer** med nummeret fra nummerserien til den nye anleggsmiddelgruppen.</span><span class="sxs-lookup"><span data-stu-id="2259d-126">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="2259d-127">Ellers oppdateres feltet **Nytt anleggsmiddelnummer** med nummeret fra nummerserien som er definert på siden **Parametere for anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="2259d-127">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="2259d-128">Hvis en nummerserie ikke er definert på siden **Parametere for anleggsmidler**, angir du et nummer i feltet **Nytt anleggsmiddelnummer**.</span><span class="sxs-lookup"><span data-stu-id="2259d-128">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="2259d-129">Angi en dato i feltet **Omklassifiseringsdato**.</span><span class="sxs-lookup"><span data-stu-id="2259d-129">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="2259d-130">Angi eller velg en verdi i feltet **Bilagsserie**.</span><span class="sxs-lookup"><span data-stu-id="2259d-130">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="2259d-131">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2259d-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
