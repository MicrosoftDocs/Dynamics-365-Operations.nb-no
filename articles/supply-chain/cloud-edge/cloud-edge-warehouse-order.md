---
title: Lagerordrer for sky- og kantskalaenheter
description: Dette emnet inneholder informasjon om funksjonen for lagerordre som brukes som en del av arbeidsbelastningen for lagerskalaenhet.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105722"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="c05a3-103">Lagerordrer for sky- og kantskalaenheter</span><span class="sxs-lookup"><span data-stu-id="c05a3-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="c05a3-104">Ikke alle forretningsfunksjoner støttes fullstendig i den offentlige forhåndsversjonen når arbeidsbelastninger for skalaenhet brukes.</span><span class="sxs-lookup"><span data-stu-id="c05a3-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="c05a3-105">Hvis du bruker skalaenheter, må du passe på at du bare bruker de prosessene som dette emnet beskriver som støttet.</span><span class="sxs-lookup"><span data-stu-id="c05a3-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="c05a3-106">Hva er lagerordrer?</span><span class="sxs-lookup"><span data-stu-id="c05a3-106">What are warehouse orders?</span></span>

<span data-ttu-id="c05a3-107">*Lagerordrer* er en type ordre som ble opprettet for å støtte lagerdistribusjoner for senter og skalaenhet.</span><span class="sxs-lookup"><span data-stu-id="c05a3-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="c05a3-108">De gjør at du kan motta beholdning når du kjører en lagerarbeidsbelastning på en skalaenhet.</span><span class="sxs-lookup"><span data-stu-id="c05a3-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="c05a3-109">De brukes for øyeblikket bare med bestillinger.</span><span class="sxs-lookup"><span data-stu-id="c05a3-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="c05a3-110">Lagerordrer brukes som en del av lagerstyringsbehandling, for eksempel når lagerappen brukes til å registrere fysisk lagerbeholdning under behandling av en innkommende bestilling.</span><span class="sxs-lookup"><span data-stu-id="c05a3-110">Warehouse orders are used as part of warehouse management processing, such as when the warehouse app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="c05a3-111">Lagerordrer opprettes som en del av prosessen *Frigi til lager*, som er tilgjengelig for bestillinger som angir et skalaenhetslager, og varer som er aktivert for å bruke lagerstyringsprosesser.</span><span class="sxs-lookup"><span data-stu-id="c05a3-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c05a3-112">Lagerordrer er bare tilgjengelige i distribusjoner som bruker [arbeidsbelastninger for lagerstyring for sky- og kantskalaenheter](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="c05a3-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="c05a3-113">Opprette en lagerordre</span><span class="sxs-lookup"><span data-stu-id="c05a3-113">Create a warehouse order</span></span>

<span data-ttu-id="c05a3-114">Følg denne fremgangsmåten for å opprette en lagerordre.</span><span class="sxs-lookup"><span data-stu-id="c05a3-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="c05a3-115">Logg deg på forekomsten av Microsoft Dynamics 365 Supply Chain Management som kjører i senteret.</span><span class="sxs-lookup"><span data-stu-id="c05a3-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="c05a3-116">(Du må starte prosessen *Frigi til lager* mens du er logget på senteret.)</span><span class="sxs-lookup"><span data-stu-id="c05a3-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="c05a3-117">Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="c05a3-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="c05a3-118">Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c05a3-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="c05a3-119">Hvis du vil vise de relaterte lagerordrelinjene, åpner du den relevante bestillingen, velger en linje i **Bestillingslinjer**-delen og velger deretter **Lager \> Lagerordrelinjer** på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="c05a3-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="c05a3-120">Hvis du vil vise alle linjene, kan du gå til **Lagerstyring \> Forespørsler og rapporter \> Lagerordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="c05a3-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="c05a3-121">Annullere en lagerordre</span><span class="sxs-lookup"><span data-stu-id="c05a3-121">Cancel a warehouse order</span></span>

<span data-ttu-id="c05a3-122">Som en del av prosessen *Frigi til lager* er lagertransaksjoner for bestilling koblet til lagerordrer og låst fra å bli oppdatert av senteret.</span><span class="sxs-lookup"><span data-stu-id="c05a3-122">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="c05a3-123">Hvis du frigir til lageret ved en feiltakelse, eller hvis du har en annen grunn til å tilbakeføre opprettelsen av lagerordrelinjer, kan du be om å få annullere lagerordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="c05a3-123">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="c05a3-124">Følg denne fremgangsmåten for å annullere lagerordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="c05a3-124">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="c05a3-125">Logg deg på forekomsten av Supply Chain Management som kjører i senteret.</span><span class="sxs-lookup"><span data-stu-id="c05a3-125">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="c05a3-126">Gå til **Lagerstyring \> Forespørsler og rapporter \> Lagerordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="c05a3-126">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="c05a3-127">Velg relevant linje.</span><span class="sxs-lookup"><span data-stu-id="c05a3-127">Select the relevant line.</span></span>
1. <span data-ttu-id="c05a3-128">Velg **Annuller lagerordrelinjer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c05a3-128">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="c05a3-129">Forespørselen om å få annullere linjer blir avslått for alle linjer som allerede venter på annullering, eller som aktivt behandles på et lager som kjører arbeidsbelastningen på en skalaenhet.</span><span class="sxs-lookup"><span data-stu-id="c05a3-129">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="c05a3-130">Overvåke en lagerordre</span><span class="sxs-lookup"><span data-stu-id="c05a3-130">Monitor a warehouse order</span></span>

<span data-ttu-id="c05a3-131">I visningen **Lagerordrelinjer** kan du overvåke fremdriften til innkommende mottak ved å se gjennom verdiene i kolonnen **Gjenstående antall å motta**.</span><span class="sxs-lookup"><span data-stu-id="c05a3-131">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="c05a3-132">Følg ett av disse trinnene for å vise detaljer som er knyttet til arbeid som er gjort ved å bruke lagerappen.</span><span class="sxs-lookup"><span data-stu-id="c05a3-132">To view details that are related to work that is done by using the warehouse app, follow one of these steps.</span></span>

- <span data-ttu-id="c05a3-133">Gå til **Lagerstyring \> Forespørsler og rapporter \> Lagerordrelinjer**, og bruk filteret til å finne linjene du ser etter.</span><span class="sxs-lookup"><span data-stu-id="c05a3-133">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="c05a3-134">Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**, og åpne den relevante bestillingen.</span><span class="sxs-lookup"><span data-stu-id="c05a3-134">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="c05a3-135">Velg én eller flere linjer i delen **Bestillingslinjer**, og velg deretter **Lager \> Oppføringer for lagermottak** på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="c05a3-135">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>
