---
title: Satsvis frigivelse av delvis reserverte overføringsordrer
description: Dette emnet beskriver hvordan du konfigurerer og bruker batchfrigjøring av delvis reserverte overføringsordrer fra en mobilenhet.
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b13e3525049c893a7193b549f5b4ba63b8841b87
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233277"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="c6754-103">Satsvis frigivelse av delvis reserverte overføringsordrer</span><span class="sxs-lookup"><span data-stu-id="c6754-103">Batch release of partially reserved transfer orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6754-104">Funksjonaliteten for batchfrigivelse av delvis reserverte overføringsordrer lar deg delvis frigi overføringsordrer til et lager ved å bruke en batchjobb.</span><span class="sxs-lookup"><span data-stu-id="c6754-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="c6754-105">Fordi du har muligheten til å frigjøre en delmengde, behøver du ikke vente på at hele bestillingsmengden er tilgjengelig på lageret før du frigir en ordre.</span><span class="sxs-lookup"><span data-stu-id="c6754-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="c6754-106">Å frigi bestillinger til et lager er en avansert varehusprosess.</span><span class="sxs-lookup"><span data-stu-id="c6754-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="c6754-107">Denne prosessen omfatter aktiviteter som plukking, pakking og frakt, som en lagerbehandler kan utføre ved bruk av en mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="c6754-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="c6754-108">Der det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="c6754-108">Where it applies</span></span>

<span data-ttu-id="c6754-109">For denne funksjonaliteten blir overføringsordrer frigitt til et lager ved å bruke en batchjobb.</span><span class="sxs-lookup"><span data-stu-id="c6754-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="c6754-110">Denne funksjonaliteten er nyttig når du ikke har nok varer på lageret, men du fortsatt vil overføre varer fra ett lager til et annet.</span><span class="sxs-lookup"><span data-stu-id="c6754-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="c6754-111">Hvordan det er satt opp</span><span class="sxs-lookup"><span data-stu-id="c6754-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="c6754-112">Angi oppfyllelseskriterier for overføringsordrer og salgsordrer</span><span class="sxs-lookup"><span data-stu-id="c6754-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="c6754-113">Før en bestilling kan frigis ut til et lager i et parti, må oppfyllelseskriteriene være oppfylt.</span><span class="sxs-lookup"><span data-stu-id="c6754-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="c6754-114">Disse oppfyllelseskriteriene bestemmes av oppfyllingsregelen.</span><span class="sxs-lookup"><span data-stu-id="c6754-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="c6754-115">Oppfyllingsregler for overføringsordrer og salgsordrer er spesifisert på bedriftsnivå.</span><span class="sxs-lookup"><span data-stu-id="c6754-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="c6754-116">Avhengig av oppsettet av oppfyllelsesreglene, vil frigivelsen av bestillinger i en batch aksepteres eller avvises.</span><span class="sxs-lookup"><span data-stu-id="c6754-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="c6754-117">Ordrene blir deretter behandlet tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="c6754-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="c6754-118">For å opprette oppfyllelsesregler for overføringsordrer og salgsordrer, klikk på **Lagerstyring** \> **Oppsett** \> **Frigi til lager** \> **Oppfyllelsesregler**, og opprett deretter oppfyllelsesregler ved å skrive inn et navn og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="c6754-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="c6754-119">For å angi en oppfyllelseshastighet, en verditype og meldingen som vises hvis oppfyllelsesreglene brytes, klikker du **Lagerstyring** \> **Oppsett** \> **Frigi til lager** \> **Oppfyllelsesregler**, og setter deretter feltene **Oppfyllelsessats**,**Verditype** og **Melding ved brudd på oppfyllelse**.</span><span class="sxs-lookup"><span data-stu-id="c6754-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="c6754-120">Angi oppfyllelsessregler for overføringsordrer og salgsordrer</span><span class="sxs-lookup"><span data-stu-id="c6754-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="c6754-121">For å angi oppfyllelsesregler for overføringsordrer, klikk **Administrering av lagerbeholdning** \> **Oppsett** \> **Parametere for beholdning og lagerstyring** \> **Overføringsordrer** \> **Lagerstyring**, og velger deretter en oppfyllelsesregel for overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="c6754-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="c6754-122">For å angi oppfyllelsesregler for salgsordrer, klikk **Kundefordringer** \> **Oppsett** \> **Parametere for kundefordringer** \> **Lagerstyring**, og velger deretter en oppfyllelsesregel for salgsordre.</span><span class="sxs-lookup"><span data-stu-id="c6754-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="c6754-123">Tillat frigivelse i en batch og angi mengden som skal frigis i en batch</span><span class="sxs-lookup"><span data-stu-id="c6754-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="c6754-124">En batchjobb brukes til å frigi ordrer til et lager i en batch.</span><span class="sxs-lookup"><span data-stu-id="c6754-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="c6754-125">Parametrene som skiller ordrene som skal kjøres i en batchjobb, settes på selve batchjobben.</span><span class="sxs-lookup"><span data-stu-id="c6754-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="c6754-126">Parameteren **Mengde** angir om hele mengden eller den fysisk reserverte mengden skal frigis i batchen.</span><span class="sxs-lookup"><span data-stu-id="c6754-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="c6754-127">Parameteren **Tillate frigivelse av delvis frigitte ordrer** bestemmer om bestillinger i batchen skal aksepteres eller avvises dersom de delvis ble frigitt tidligere.</span><span class="sxs-lookup"><span data-stu-id="c6754-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="c6754-128">For å angi parametere for overføringsordre, **Mengde** og **Tillate frigivelse av delvis frigitte ordrer**, klikk **Lagerstyring** \> **Frigi til lager** \> **Automatisk frigivelse for overføringsordrer**</span><span class="sxs-lookup"><span data-stu-id="c6754-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="c6754-129">For å angi parametere for salgsordre, **Mengde** og **Tillate frigivelse av delvis frigitte ordrer**, klikk **Lagerstyring** \> **Frigi til lager** \> **Automatisk frigivelse for salgsordrer**</span><span class="sxs-lookup"><span data-stu-id="c6754-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]