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
ms.openlocfilehash: 9102f53ab1b63d08b8bba7b0ae505416ec5a83fd
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556368"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="f5de0-103">Lagerordrer for sky- og kantskalaenheter</span><span class="sxs-lookup"><span data-stu-id="f5de0-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="f5de0-104">Ikke alle forretningsfunksjoner støttes fullstendig i den offentlige forhåndsversjonen når arbeidsbelastninger for skalaenhet brukes.</span><span class="sxs-lookup"><span data-stu-id="f5de0-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="f5de0-105">Hvis du bruker skalaenheter, må du passe på at du bare bruker de prosessene som dette emnet beskriver som støttet.</span><span class="sxs-lookup"><span data-stu-id="f5de0-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="f5de0-106">Hva er lagerordrer?</span><span class="sxs-lookup"><span data-stu-id="f5de0-106">What are warehouse orders?</span></span>

<span data-ttu-id="f5de0-107">*Lagerordrer* er en type ordre som ble opprettet for å støtte lagerdistribusjoner for senter og skalaenhet.</span><span class="sxs-lookup"><span data-stu-id="f5de0-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="f5de0-108">De gjør at du kan motta beholdning når du kjører en lagerarbeidsbelastning på en skalaenhet.</span><span class="sxs-lookup"><span data-stu-id="f5de0-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="f5de0-109">De brukes for øyeblikket bare med bestillinger.</span><span class="sxs-lookup"><span data-stu-id="f5de0-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="f5de0-110">Lagerordrer brukes som en del av lagerstyringsbehandling, for eksempel når lagerappen brukes til å registrere fysisk lagerbeholdning under behandling av en innkommende bestilling.</span><span class="sxs-lookup"><span data-stu-id="f5de0-110">Warehouse orders are used as part of warehouse management processing, such as when the warehouse app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="f5de0-111">Lagerordrer opprettes som en del av prosessen *Frigi til lager*, som er tilgjengelig for bestillinger som angir et skalaenhetslager, og varer som er aktivert for å bruke lagerstyringsprosesser.</span><span class="sxs-lookup"><span data-stu-id="f5de0-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5de0-112">Lagerordrer er bare tilgjengelige i distribusjoner som bruker [arbeidsbelastninger for lagerstyring for sky- og kantskalaenheter](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="f5de0-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="f5de0-113">Opprette en lagerordre</span><span class="sxs-lookup"><span data-stu-id="f5de0-113">Create a warehouse order</span></span>

<span data-ttu-id="f5de0-114">Følg denne fremgangsmåten for å opprette en lagerordre.</span><span class="sxs-lookup"><span data-stu-id="f5de0-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="f5de0-115">Logg deg på forekomsten av Microsoft Dynamics 365 Supply Chain Management som kjører i senteret.</span><span class="sxs-lookup"><span data-stu-id="f5de0-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="f5de0-116">(Du må starte prosessen *Frigi til lager* mens du er logget på senteret.)</span><span class="sxs-lookup"><span data-stu-id="f5de0-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="f5de0-117">Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="f5de0-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="f5de0-118">Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f5de0-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="f5de0-119">Hvis du vil vise de relaterte lagerordrelinjene, åpner du den relevante bestillingen, velger en linje i **Bestillingslinjer**-delen og velger deretter **Lager \> Lagerordrelinjer** på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="f5de0-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="f5de0-120">Hvis du vil vise alle linjene, kan du gå til **Lagerstyring \> Forespørsler og rapporter \> Lagerordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="f5de0-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

<span data-ttu-id="f5de0-121">Du kan også utløse prosessen *Frigi til lager* fra en satsvis jobb ved å gå til **Lagerstyring > Frigi til lager > Automatisk frigivelse av bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="f5de0-121">You can also trigger the *Release to warehouse* process from a batch job by going to **Warehouse management > Release to warehouse > Automatic release of purchase orders**.</span></span> <span data-ttu-id="f5de0-122">Når du definerer den satsvise jobben, kan du velge bestemte bestillingslinjer basert på en spørring.</span><span class="sxs-lookup"><span data-stu-id="f5de0-122">When setting up the batch job, you can select specific purchase order lines based on a query.</span></span> <span data-ttu-id="f5de0-123">Et typisk scenario vil være å sette opp en gjentakende satsvis jobb som frigir alle bekreftede bestillingslinjer som forventes å ankomme neste dag.</span><span class="sxs-lookup"><span data-stu-id="f5de0-123">A typical scenario would be to set up a recurrent batch job that releases all the confirmed purchase order lines expected to arrive the next day.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="f5de0-124">Annullere en lagerordre</span><span class="sxs-lookup"><span data-stu-id="f5de0-124">Cancel a warehouse order</span></span>

<span data-ttu-id="f5de0-125">Som en del av prosessen *Frigi til lager* er lagertransaksjoner for bestilling koblet til lagerordrer og låst fra å bli oppdatert av senteret.</span><span class="sxs-lookup"><span data-stu-id="f5de0-125">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="f5de0-126">Hvis du frigir til lageret ved en feiltakelse, eller hvis du har en annen grunn til å tilbakeføre opprettelsen av lagerordrelinjer, kan du be om å få annullere lagerordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="f5de0-126">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="f5de0-127">Følg denne fremgangsmåten for å annullere lagerordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="f5de0-127">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="f5de0-128">Logg deg på forekomsten av Supply Chain Management som kjører i senteret.</span><span class="sxs-lookup"><span data-stu-id="f5de0-128">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="f5de0-129">Gå til **Lagerstyring \> Forespørsler og rapporter \> Lagerordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="f5de0-129">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="f5de0-130">Velg relevant linje.</span><span class="sxs-lookup"><span data-stu-id="f5de0-130">Select the relevant line.</span></span>
1. <span data-ttu-id="f5de0-131">Velg **Annuller lagerordrelinjer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f5de0-131">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="f5de0-132">Forespørselen om å få annullere linjer blir avslått for alle linjer som allerede venter på annullering, eller som aktivt behandles på et lager som kjører arbeidsbelastningen på en skalaenhet.</span><span class="sxs-lookup"><span data-stu-id="f5de0-132">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="f5de0-133">Overvåke en lagerordre</span><span class="sxs-lookup"><span data-stu-id="f5de0-133">Monitor a warehouse order</span></span>

<span data-ttu-id="f5de0-134">I visningen **Lagerordrelinjer** kan du overvåke fremdriften til innkommende mottak ved å se gjennom verdiene i kolonnen **Gjenstående antall å motta**.</span><span class="sxs-lookup"><span data-stu-id="f5de0-134">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="f5de0-135">Følg ett av disse trinnene for å vise detaljer som er knyttet til arbeid som er gjort ved å bruke lagerappen.</span><span class="sxs-lookup"><span data-stu-id="f5de0-135">To view details that are related to work that is done by using the warehouse app, follow one of these steps.</span></span>

- <span data-ttu-id="f5de0-136">Gå til **Lagerstyring \> Forespørsler og rapporter \> Lagerordrelinjer**, og bruk filteret til å finne linjene du ser etter.</span><span class="sxs-lookup"><span data-stu-id="f5de0-136">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="f5de0-137">Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**, og åpne den relevante bestillingen.</span><span class="sxs-lookup"><span data-stu-id="f5de0-137">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="f5de0-138">Velg én eller flere linjer i delen **Bestillingslinjer**, og velg deretter **Lager \> Oppføringer for lagermottak** på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="f5de0-138">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]