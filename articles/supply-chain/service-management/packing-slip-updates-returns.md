---
title: Følgesedddeloppdateringer for returer
description: Før returnerte varer kan mottas til lager, må følgeseddelen for ordren som varene tilhører, oppdateres.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87dfad2247c84f8e85074739cfff4a2d1b9f8567
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259704"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="d2a83-103">Følgesedddeloppdateringer for returer</span><span class="sxs-lookup"><span data-stu-id="d2a83-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d2a83-104">Før returnerte varer kan mottas til lager, må følgeseddelen for ordren som varene tilhører, oppdateres.</span><span class="sxs-lookup"><span data-stu-id="d2a83-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="d2a83-105">På samme måte som fakturaoppdateringsprosessen er en oppdatering av finanstransaksjonen, er oppdateringsprosessen for følgeseddelen den fysiske oppdateringen av lagerposten, noe som betyr at endringene aktiveres i beholdningen.</span><span class="sxs-lookup"><span data-stu-id="d2a83-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="d2a83-106">Når det gjelder returer, implementeres trinnene som er tilordnet til disposisjonshandlingen, når følgeseddelen oppdateres</span><span class="sxs-lookup"><span data-stu-id="d2a83-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="d2a83-107">Følgeseddeloppdateringen kan behandles enten i vareankomstjournalen eller i returordren.</span><span class="sxs-lookup"><span data-stu-id="d2a83-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="d2a83-108">Som et ledd i prosessen for postering av følgesedler kan følgeseddelens referansenummer fra kundens forsendelsesdokumenter knyttes til ordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="d2a83-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="d2a83-109">Denne tilknytningen er valgfri og er bare til referanseformål.</span><span class="sxs-lookup"><span data-stu-id="d2a83-109">This association is optional and for reference only.</span></span> <span data-ttu-id="d2a83-110">Det opprettes ikke transaksjonsoppdateringer.</span><span class="sxs-lookup"><span data-stu-id="d2a83-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="d2a83-111">Hvis ikke alle varene som forventes returnert er ankommet, må du inkludere bare det mottatte antallet i følgeseddeloppdateringen.</span><span class="sxs-lookup"><span data-stu-id="d2a83-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="d2a83-112">Se bort fra resten av varene i ordren til resten av returforsendelsen ankommer.</span><span class="sxs-lookup"><span data-stu-id="d2a83-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="d2a83-113">Hvis en vare sendes tilbake fra karantene til forsendelses- eller mottaksavdelingen, for eksempel når karanteneinspektøren ikke vet hvor på lageret varene skal lagres, må den tilsvarende følgeseddelen oppdateres for sikre at disposisjonskoden som er angitt som et resultat av karantenen, registreres og følges opp på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="d2a83-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="d2a83-114">Når du oppdaterer en følgeseddel for en returnert vare fra en salgsavtale, oppdateres automatisk salgsavtaleforpliktelsen for denne varen for å gjenspeile endringen i antallet eller beløpet.</span><span class="sxs-lookup"><span data-stu-id="d2a83-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="d2a83-115">Se også</span><span class="sxs-lookup"><span data-stu-id="d2a83-115">See also</span></span>

[<span data-ttu-id="d2a83-116">Utføre fakturaoppdateringer for returer</span><span class="sxs-lookup"><span data-stu-id="d2a83-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]