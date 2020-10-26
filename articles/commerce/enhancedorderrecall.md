---
title: Tilbakekall ordre-operasjon i POS
description: Dette emnet inneholder funksjoner som er tilgjengelige for forbedrede sider for tilbakekalling av ordrer i POS.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 41944fb7819b5527f6bc023a60acd9450d9e43c2
ms.sourcegitcommit: 25909c6ad3616e4f75a2fe006057dda18d7cc856
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974844"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="ba23b-103">Tilbakekall ordre-operasjon i POS</span><span class="sxs-lookup"><span data-stu-id="ba23b-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ba23b-104">Tilbakekall ordre-operasjonen i Commerce-salgsstedet (POS) inneholder oppdaterte funksjoner for ordresøk og -filtrering og ordrespesifikk informasjon.</span><span class="sxs-lookup"><span data-stu-id="ba23b-104">The Recall order operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="ba23b-105">Denne funksjonen er tilgjengelig i Commerce versjon 10.0.15 og nyere.</span><span class="sxs-lookup"><span data-stu-id="ba23b-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="ba23b-106">Hvis du vil aktivere denne funksjonaliteten, aktiverer du funksjonen **Forbedret tilbakekall ordre-operasjon i POS** i arbeidsområdet **Funksjonsbehandling** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ba23b-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="ba23b-107">Når du har aktivert funksjonen, bør du vurdere å oppdatere [skjermoppsettene](pos-screen-layouts.md) i POS for å dra nytte av noen av de endrede funksjonene.</span><span class="sxs-lookup"><span data-stu-id="ba23b-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="ba23b-108">Konfigurasjon av knappen for **Tilbakekall ordre** -operasjonen lar organisasjoner distribuere operasjonen med en forhåndsdefinert visning.</span><span class="sxs-lookup"><span data-stu-id="ba23b-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Konfigurasjon for knappegruppe](media/recallorderbuttongrid.png)

<span data-ttu-id="ba23b-110">Visningsalternativene er som følger:</span><span class="sxs-lookup"><span data-stu-id="ba23b-110">The display options are as follows.</span></span>
- <span data-ttu-id="ba23b-111">**Ingen** – Dette alternativet distribuerer operasjonen uten en bestemt visning.</span><span class="sxs-lookup"><span data-stu-id="ba23b-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="ba23b-112">Når en bruker åpner operasjonen med denne konfigurasjonen, blir de bedt om å søke etter og finne ordrer, eller velge fra et forhåndsdefinert ordrefilter.</span><span class="sxs-lookup"><span data-stu-id="ba23b-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="ba23b-113">**Ordrer som skal oppfylles** – Når en bruker starter operasjonen, kjøres en spørring automatisk for å søke etter og vise en liste over ordrer som skal oppfylles av butikken.</span><span class="sxs-lookup"><span data-stu-id="ba23b-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="ba23b-114">Disse ordrene er konfigurert for henting i butikk eller butikkforsendelse, og linjene i disse ordrene er ennå ikke plukket eller pakket.</span><span class="sxs-lookup"><span data-stu-id="ba23b-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="ba23b-115">**Ordrer som skal hentes** – Når en bruker starter operasjonen, kjøres en spørring automatisk for å søke etter og vise en liste over ordrer som er konfigurert for henting i butikk i brukerens gjeldende butikk.</span><span class="sxs-lookup"><span data-stu-id="ba23b-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="ba23b-116">**Ordrer som skal leveres** – Når en bruker starter operasjonen, kjøres en spørring automatisk for å søke etter og vise en liste over ordrer som er konfigurert for levering fra brukerens gjeldende butikk.</span><span class="sxs-lookup"><span data-stu-id="ba23b-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="ba23b-117">Når du starter **Tilbakekall ordre** -operasjonen fra POS og visningen er konfigurert til **Ingen** , kan en bruker søke etter og hente ordrer på én av måtene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="ba23b-117">When launching the **Recall order** operation from POS, if the display is configured to **None** , a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="ba23b-118">Skanne ordrestrekkoder.</span><span class="sxs-lookup"><span data-stu-id="ba23b-118">Scan order barcodes.</span></span> <span data-ttu-id="ba23b-119">Dette søker etter samsvarende felt for ordrenummer, kanalreferanse og kvitterings-ID.</span><span class="sxs-lookup"><span data-stu-id="ba23b-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="ba23b-120">Velg **Søk etter ordrer** - eller **Søk og filtrer** -ikonet på applinjen for å bruke filtreringsmekanismen til å finne ordrer som oppfyller filterkriteriene.</span><span class="sxs-lookup"><span data-stu-id="ba23b-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="ba23b-121">Velg fra et forhåndsdefinert filter fra rullegardinmenyen **Vis ordrer** (ordrer som skal oppfylles, ordrer som skal hentes, eller ordrer som skal leveres).</span><span class="sxs-lookup"><span data-stu-id="ba23b-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="ba23b-123">Når søkekriteriene er brukt, vil appen vise en liste over samsvarende salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="ba23b-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="ba23b-125">En bruker kan velge en ordre i listen for å vise flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="ba23b-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="ba23b-126">Informasjonspanelet til høyre på skjermen viser informasjon om den valgte ordren, inkludert ordrelinjedetaljer, leveringsdetaljer og oppfyllingsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="ba23b-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="ba23b-127">Fra applinjen kan en bruker velge en operasjon.</span><span class="sxs-lookup"><span data-stu-id="ba23b-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="ba23b-128">Det kan hende at bestemte operasjoner ikke er aktivert, avhengig av statusen for ordren.</span><span class="sxs-lookup"><span data-stu-id="ba23b-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="ba23b-129">**Retur** – Utfører en retur for én eller flere fakturaer som er knyttet til den valgte kundeordren.</span><span class="sxs-lookup"><span data-stu-id="ba23b-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="ba23b-130">**Avbryt** – Utsteder en fullstendig annullering av den valgte salgsordren.</span><span class="sxs-lookup"><span data-stu-id="ba23b-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="ba23b-131">**Oppfyll** – Overfører brukeren til siden for ordreoppfylling som blir forhåndsfiltrert for den valgte ordren.</span><span class="sxs-lookup"><span data-stu-id="ba23b-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="ba23b-132">Bare ordrelinjer som er åpne for oppfyllelse av brukerens butikk for den valgte ordren, vises.</span><span class="sxs-lookup"><span data-stu-id="ba23b-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="ba23b-133">**Rediger** – Lar brukere gjøre endringer i den valgte kundeordren.</span><span class="sxs-lookup"><span data-stu-id="ba23b-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="ba23b-134">**Hent** – Starter henteflyten, slik at brukeren kan velge hvilke produkter som skal hentes, og opprette salgstransaksjoner for hentingen.</span><span class="sxs-lookup"><span data-stu-id="ba23b-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>
