---
title: Behandle butikkbeholdning
description: "Denne artikkelen beskriver hvilke typer dokumenter du kan bruke til å styre lager."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1fd37bcd7155c61492f5f4990685203ea97bca36
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="manage-store-inventory"></a><span data-ttu-id="72c25-103">Behandle butikkbeholdning</span><span class="sxs-lookup"><span data-stu-id="72c25-103">Manage store inventory</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="72c25-104">Denne artikkelen beskriver hvilke typer dokumenter du kan bruke til å styre lager.</span><span class="sxs-lookup"><span data-stu-id="72c25-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="72c25-105">Du kan bruke følgende typer dokumenter til å styre organisasjonens lager.</span><span class="sxs-lookup"><span data-stu-id="72c25-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="72c25-106">Bestillinger</span><span class="sxs-lookup"><span data-stu-id="72c25-106">Purchase orders</span></span>
<span data-ttu-id="72c25-107">Bestillinger opprettes ved hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="72c25-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="72c25-108">Hvis et lager for detaljhandel er inkludert i bestillingshodet, kan ordren mottas i butikken ved hjelp av Detaljhandel og handel i moderne salgssted eller skysalgssted for Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="72c25-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="72c25-109">Når antallene som er mottatt i butikken, er registrert, kan de lagres lokalt for ytterligere endring.</span><span class="sxs-lookup"><span data-stu-id="72c25-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="72c25-110">Antallene kan eventuelt lagres og sendes til hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="72c25-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="72c25-111">På hovedkontoret vises antallene som ble mottatt i butikken, i **Motta nå**-feltet i bestillingen i Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="72c25-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="72c25-112">Overføringsordrer</span><span class="sxs-lookup"><span data-stu-id="72c25-112">Transfer orders</span></span>
<span data-ttu-id="72c25-113">En overføringsordre kan angi at en bestemt butikk er en lokasjon som varer kan sendes fra.</span><span class="sxs-lookup"><span data-stu-id="72c25-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="72c25-114">I dette tilfellet vises overføringsordren i butikken som en plukkforespørsel i Moderne salgssted eller Skysalgssted.</span><span class="sxs-lookup"><span data-stu-id="72c25-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="72c25-115">Når de ønskede antallene er plukket, er lagres de og sendes til hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="72c25-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="72c25-116">På hovedkontoret vises antallene som ble plukket i butikken, i **Send nå**-feltet i overføringsordren i Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="72c25-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="72c25-117">En overføringsordre kan angi at en bestemt butikk er en lokasjon som varer kan sendes til.</span><span class="sxs-lookup"><span data-stu-id="72c25-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="72c25-118">I dette tilfellet vises overføringsordren i butikken som en mottaksforespørsel i Moderne salgssted eller Skysalgssted.</span><span class="sxs-lookup"><span data-stu-id="72c25-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="72c25-119">Når antallene som er mottatt i butikken, er registrert, kan de lagres lokalt for ytterligere endring.</span><span class="sxs-lookup"><span data-stu-id="72c25-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="72c25-120">Antallene kan eventuelt lagres og sendes til hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="72c25-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="72c25-121">På hovedkontoret vises antallene som ble mottatt i butikken, i **Motta nå**-feltet i overføringsordren i Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="72c25-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="72c25-122">Lagerantall</span><span class="sxs-lookup"><span data-stu-id="72c25-122">Stock counts</span></span>
<span data-ttu-id="72c25-123">Lagertellinger kan være planlagt eller ikke planlagt.</span><span class="sxs-lookup"><span data-stu-id="72c25-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="72c25-124">Planlagte lagertellinger startes ved hovedkontoret, som angir hvilke varer som skal telles.</span><span class="sxs-lookup"><span data-stu-id="72c25-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="72c25-125">Hovedkontoret oppretter et opptellingsdokument som kan mottas i butikken, der faktisk beholdningsantall registreres i Moderne salgssted eller Skysalgssted.</span><span class="sxs-lookup"><span data-stu-id="72c25-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="72c25-126">Ikke planlagte lagertellinger startes i en butikk, og faktisk beholdningsantall oppdateres i Moderne salgssted eller Skysalgssted.</span><span class="sxs-lookup"><span data-stu-id="72c25-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="72c25-127">I motsetning til planlagte lagertellinger har ikke ikke-planlagte lagertellinger en forhåndsdefinert liste over varer.</span><span class="sxs-lookup"><span data-stu-id="72c25-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="72c25-128">Når en lagertelling av en av disse typene er fullført, lagres og sendes den til hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="72c25-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="72c25-129">Ved hovedkontoret valideres og posteres antallet.</span><span class="sxs-lookup"><span data-stu-id="72c25-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="72c25-130">Beholdningsoppslag</span><span class="sxs-lookup"><span data-stu-id="72c25-130">Inventory lookup</span></span>
<span data-ttu-id="72c25-131">Det gjeldende produktantallet på lager for flere butikker og lagre kan vises på Beholdningsoppslag-siden.</span><span class="sxs-lookup"><span data-stu-id="72c25-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="72c25-132">I tillegg til gjeldende antall på lager kan fremtidige antall tilgjengelig for ordre (ATP) vises for hver enkelt butikk.</span><span class="sxs-lookup"><span data-stu-id="72c25-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="72c25-133">Dette gjør du ved å velge butikken du vil vise ATP-Antallet for, og deretter klikker du **Vis butikktilgjengelighet**.</span><span class="sxs-lookup"><span data-stu-id="72c25-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





