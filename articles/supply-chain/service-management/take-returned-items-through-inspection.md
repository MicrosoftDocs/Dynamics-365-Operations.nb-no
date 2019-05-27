---
title: Ta returnerte varer gjennom inspeksjon
description: Ta returnerte varer gjennom inspeksjon.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82d94e055326e598113822b8d7c4852b7dcb0c4e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565517"
---
# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="a34fc-103">Ta returnerte varer gjennom inspeksjon</span><span class="sxs-lookup"><span data-stu-id="a34fc-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="a34fc-104">Klikk **Lagerstyring** \> **Periodisk** \> **Kvalitetsstyring** \> **Karanteneordrer**.</span><span class="sxs-lookup"><span data-stu-id="a34fc-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="a34fc-105">Finn ordrelinjen som tilsvarer den returnerte varen du undersøker.</span><span class="sxs-lookup"><span data-stu-id="a34fc-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="a34fc-106">En karanteneordre kan bare tilknyttes ett enkelt varenummer.</span><span class="sxs-lookup"><span data-stu-id="a34fc-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="a34fc-107">Hvis 10 varer som har forskjellige varenumre returneres i én enkelt forsendelse og sendes i karantene, opprettes det 10 forskjellige karanteneordrer.</span><span class="sxs-lookup"><span data-stu-id="a34fc-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="a34fc-108">Når du er ferdig med å undersøke varen, velger du et alternativ i **Disposisjonskode**-feltet som angir hva som skal gjøres med varen og hvordan de tilknyttede finanstransaksjonene skal håndteres.</span><span class="sxs-lookup"><span data-stu-id="a34fc-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="a34fc-109">Du kan for eksempel velge å returnere varen til lager og refundere kunden, kassere varen og sende kunden en ny, eller returnere varen til kunden uten godtgjøring.</span><span class="sxs-lookup"><span data-stu-id="a34fc-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="a34fc-110">Hvis det returnerte partiet består av flere varer med samme partinummer, men som krever forskjellige disposisjonskoder, må du dele opp karanteneordren (<STRONG>Funksjoner</STRONG> &gt; <STRONG>Del</STRONG>) for å kunne tildele hvert delparti en egen disposisjonskode.</span><span class="sxs-lookup"><span data-stu-id="a34fc-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="a34fc-111">Når du er ferdig med undersøkelsen, klikker du **Ferdigmeld** for å frigi de returnerte varene og opprette en oppføring i vareankomstjournalen.</span><span class="sxs-lookup"><span data-stu-id="a34fc-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="a34fc-112">Personen eller avdelingen som mottar varene behandler deretter journalen, slik at varene kan returneres til lager.</span><span class="sxs-lookup"><span data-stu-id="a34fc-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="a34fc-113">– eller –</span><span class="sxs-lookup"><span data-stu-id="a34fc-113">–or–</span></span>
    
    <span data-ttu-id="a34fc-114">Avslutt karanteneordren, og flytt varene tilbake til lager direkte med en av **Lager**-funksjonene.</span><span class="sxs-lookup"><span data-stu-id="a34fc-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="a34fc-115">Lukk skjemaet for å lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="a34fc-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="a34fc-116">Se også</span><span class="sxs-lookup"><span data-stu-id="a34fc-116">See also</span></span>

[<span data-ttu-id="a34fc-117">Angi hvordan du kvitter deg med returnerte varer</span><span class="sxs-lookup"><span data-stu-id="a34fc-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  


