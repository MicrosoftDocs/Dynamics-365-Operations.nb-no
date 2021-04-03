---
title: Tilbakekall ordre-operasjon i POS
description: Dette emnet inneholder funksjoner som er tilgjengelige for forbedrede sider for tilbakekalling av ordrer i POS.
author: hhainesms
manager: annbe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 174821fce4baf81e4298da4b066f855bfec98ca5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585136"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="3ac70-103">Tilbakekall ordre-operasjon i POS</span><span class="sxs-lookup"><span data-stu-id="3ac70-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3ac70-104">**Tilbakekall ordre**-operasjonen i Commerce-salgsstedet (POS) inneholder oppdaterte funksjoner for ordresøk og -filtrering og ordrespesifikk informasjon.</span><span class="sxs-lookup"><span data-stu-id="3ac70-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="3ac70-105">Denne funksjonen er tilgjengelig i Commerce versjon 10.0.15 og nyere.</span><span class="sxs-lookup"><span data-stu-id="3ac70-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="3ac70-106">Hvis du vil aktivere denne funksjonaliteten, aktiverer du funksjonen **Forbedret tilbakekall ordre-operasjon i POS** i arbeidsområdet **Funksjonsbehandling** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="3ac70-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="3ac70-107">Når du har aktivert funksjonen, bør du vurdere å oppdatere [skjermoppsettene](pos-screen-layouts.md) i POS for å dra nytte av noen av de endrede funksjonene.</span><span class="sxs-lookup"><span data-stu-id="3ac70-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="3ac70-108">Konfigurasjon av knappen for **Tilbakekall ordre**-operasjonen lar organisasjoner distribuere operasjonen med en forhåndsdefinert visning.</span><span class="sxs-lookup"><span data-stu-id="3ac70-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Konfigurasjon for knappegruppe](media/recallorderbuttongrid.png)

<span data-ttu-id="3ac70-110">Visningsalternativene er som følger:</span><span class="sxs-lookup"><span data-stu-id="3ac70-110">The display options are as follows.</span></span>
- <span data-ttu-id="3ac70-111">**Ingen** – Dette alternativet distribuerer operasjonen uten en bestemt visning.</span><span class="sxs-lookup"><span data-stu-id="3ac70-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="3ac70-112">Når en bruker åpner operasjonen med denne konfigurasjonen, blir de bedt om å søke etter og finne ordrer, eller velge fra et forhåndsdefinert ordrefilter.</span><span class="sxs-lookup"><span data-stu-id="3ac70-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="3ac70-113">**Ordrer som skal oppfylles** – Når en bruker starter operasjonen, kjøres en spørring automatisk for å søke etter og vise en liste over ordrer som skal oppfylles av brukerens gjeldende butikk.</span><span class="sxs-lookup"><span data-stu-id="3ac70-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the user's current store.</span></span> <span data-ttu-id="3ac70-114">Disse ordrene er konfigurert for henting i butikk eller butikkforsendelse, og linjene i disse ordrene er ennå ikke plukket eller pakket.</span><span class="sxs-lookup"><span data-stu-id="3ac70-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="3ac70-115">**Ordrer som skal hentes** – Når en bruker starter operasjonen, kjøres en spørring automatisk for å søke etter og vise en liste over ordrer som er konfigurert for henting i butikk i brukerens gjeldende butikk.</span><span class="sxs-lookup"><span data-stu-id="3ac70-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="3ac70-116">**Ordrer som skal leveres** – Når en bruker starter operasjonen, kjøres en spørring automatisk for å søke etter og vise en liste over ordrer som er konfigurert for levering fra brukerens gjeldende butikk.</span><span class="sxs-lookup"><span data-stu-id="3ac70-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="3ac70-117">Når du starter **Tilbakekall ordre**-operasjonen fra POS og visningen er konfigurert til **Ingen**, kan en bruker søke etter og hente ordrer på én av måtene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="3ac70-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="3ac70-118">Skanne ordrestrekkoder.</span><span class="sxs-lookup"><span data-stu-id="3ac70-118">Scan order barcodes.</span></span> <span data-ttu-id="3ac70-119">Dette søker etter samsvarende felt for ordrenummer, kanalreferanse og kvitterings-ID.</span><span class="sxs-lookup"><span data-stu-id="3ac70-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="3ac70-120">Velg **Søk etter ordrer**- eller **Søk og filtrer**-ikonet på applinjen for å bruke filtreringsmekanismen til å finne ordrer som oppfyller filterkriteriene.</span><span class="sxs-lookup"><span data-stu-id="3ac70-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="3ac70-121">Velg fra et forhåndsdefinert filter fra rullegardinmenyen **Vis ordrer** (ordrer som skal oppfylles, ordrer som skal hentes, eller ordrer som skal leveres).</span><span class="sxs-lookup"><span data-stu-id="3ac70-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="3ac70-123">Når søkekriteriene er brukt, vil appen vise en liste over samsvarende salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="3ac70-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span> <span data-ttu-id="3ac70-124">Det er viktig å merke seg at når du bruker søke-/filteralternativene, trenger ikke ordrene som hentes, være ordrer som er koblet til brukerens gjeldende butikk.</span><span class="sxs-lookup"><span data-stu-id="3ac70-124">It's important to note that when using the search/filter options, the orders retrieved do not have to be orders linked to the user's current store.</span></span> <span data-ttu-id="3ac70-125">Denne søkeprosessen henter og viser alle kundeordrer som samsvarer med søkekriteriene, selv om ordren ble opprettet eller angitt til å bli utført av en annen butikk/kanal eller lagerlokasjon.</span><span class="sxs-lookup"><span data-stu-id="3ac70-125">This search process will retrieve and display any customer order that matches the search criteria, even if the order was created or set to be fulfilled by another store/channel or warehouse location.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="3ac70-127">En bruker kan velge en ordre i listen for å vise flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="3ac70-127">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="3ac70-128">Informasjonspanelet til høyre på skjermen viser informasjon om den valgte ordren, inkludert ordrelinjedetaljer, leveringsdetaljer og oppfyllingsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="3ac70-128">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="3ac70-129">Fra applinjen kan en bruker velge en operasjon.</span><span class="sxs-lookup"><span data-stu-id="3ac70-129">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="3ac70-130">Det kan hende at bestemte operasjoner ikke er aktivert, avhengig av statusen for ordren.</span><span class="sxs-lookup"><span data-stu-id="3ac70-130">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="3ac70-131">**Retur** – Starter prosessen med å opprette en retur for alle de fakturerte produktene på den valgte kundeordren.</span><span class="sxs-lookup"><span data-stu-id="3ac70-131">**Return** – Initiates the process of creating a return for any of the invoiced products on the selected customer order.</span></span>

- <span data-ttu-id="3ac70-132">**Avbryt** – Utsteder en fullstendig annullering av den valgte salgsordren.</span><span class="sxs-lookup"><span data-stu-id="3ac70-132">**Cancel** – Issue a full cancellation of the selected sales order.</span></span> <span data-ttu-id="3ac70-133">Dette alternativet er ikke tilgjengelig for ordrer som startes via en samtalesenterkanal, og kan ikke brukes til å avbryte en ordre delvis.</span><span class="sxs-lookup"><span data-stu-id="3ac70-133">This option will not be available for orders initiated through a call center channel and cannot be used to partially cancel an order.</span></span>

- <span data-ttu-id="3ac70-134">**Oppfyll** – Overfører brukeren til siden for ordreoppfylling som blir forhåndsfiltrert for den valgte ordren.</span><span class="sxs-lookup"><span data-stu-id="3ac70-134">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="3ac70-135">Bare ordrelinjer som er åpne for oppfyllelse av brukerens butikk for den valgte ordren, vises.</span><span class="sxs-lookup"><span data-stu-id="3ac70-135">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="3ac70-136">**Rediger** – Lar brukere gjøre endringer i den valgte kundeordren.</span><span class="sxs-lookup"><span data-stu-id="3ac70-136">**Edit** – Allows users to make changes to the selected customer order.</span></span> <span data-ttu-id="3ac70-137">Ordrer kan bare redigeres i [bestemte scenarioer](customer-orders-overview.md#edit-an-existing-customer-order).</span><span class="sxs-lookup"><span data-stu-id="3ac70-137">Orders are only editable in [certain scenarios](customer-orders-overview.md#edit-an-existing-customer-order).</span></span>

- <span data-ttu-id="3ac70-138">**Henting** – Dette alternativet vil være tilgjengelig hvis ordren har én eller flere linjer angitt for henting i brukerens gjeldende butikk.</span><span class="sxs-lookup"><span data-stu-id="3ac70-138">**Pick up** – This option will be available if the order has one or more lines designated for pickup at the user's current store.</span></span> <span data-ttu-id="3ac70-139">Denne operasjonen starter henteflyten, slik at brukeren kan velge hvilke produkter som skal hentes, og opprette salgstransaksjoner for hentingen.</span><span class="sxs-lookup"><span data-stu-id="3ac70-139">This operation launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>

## <a name="add-notifications-to-the-recall-order-operation"></a><span data-ttu-id="3ac70-140">Legge til meldinger i operasjonen for tilbakekalling av ordre</span><span class="sxs-lookup"><span data-stu-id="3ac70-140">Add notifications to the recall order operation</span></span>

<span data-ttu-id="3ac70-141">I versjon 10.0.18 og senere kan du konfigurere POS-meldinger og direkte flisvarslinger for operasjonen **Tilbakekalling av ordre** hvis dette er ønskelig.</span><span class="sxs-lookup"><span data-stu-id="3ac70-141">In version 10.0.18 and later, you can configure POS notifications and live tile alerts for the **Order Recall** operation if desired.</span></span> <span data-ttu-id="3ac70-142">Hvis du vil ha mer informasjon, kan du se [Vise ordrevarslinger på salgsstedet](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="3ac70-142">For more information, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
