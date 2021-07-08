---
title: Annullerte produktmottak oppdaterer ikke transaksjonsstatusen til Registrert
description: Når du har annullert produktmottak for en innkommende last, oppdaterer systemet automatisk lagertransaksjonsstatusen fra Mottatt til Bestilt.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294144"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="ff488-103">Annullerte produktmottak oppdaterer ikke transaksjonsstatusen til Registrert</span><span class="sxs-lookup"><span data-stu-id="ff488-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="ff488-104">Symptomer</span><span class="sxs-lookup"><span data-stu-id="ff488-104">Symptoms</span></span>

<span data-ttu-id="ff488-105">Når du har kjørt handlingen **Avbryt produktmottak** for en innkommende last, oppdaterer systemet automatisk lagertransaksjonsstatusen fra *Mottatt* til *Bestilt*.</span><span class="sxs-lookup"><span data-stu-id="ff488-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="ff488-106">Løsning</span><span class="sxs-lookup"><span data-stu-id="ff488-106">Resolution</span></span>

<span data-ttu-id="ff488-107">Når følgesedler annulleres for utgående belastninger, forblir statusen for lagertransaksjoner *Plukket*.</span><span class="sxs-lookup"><span data-stu-id="ff488-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="ff488-108">Når produktmottak fra en innkommende last annulleres, vil imidlertid statusen for lagertransaksjoner som gjenopprettes, ikke gjenopprettes til *Registrert*.</span><span class="sxs-lookup"><span data-stu-id="ff488-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="ff488-109">Når et produktmottak fra en innkommende last er annullert, må derfor lagerarbeideren registrere vareantallet på nytt for lasten.</span><span class="sxs-lookup"><span data-stu-id="ff488-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="ff488-110">Hvis du vil ha mer informasjon, kan du se [Registrere vareantall som ankommer for en innkommende last](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span><span class="sxs-lookup"><span data-stu-id="ff488-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
