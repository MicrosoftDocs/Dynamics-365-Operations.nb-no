---
title: Delvis levering av en transportlast
description: Dette emnet forklarer hvordan du kan delvis levere en last og utsette planleggingen av kapasitet for lasten.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e92a15cf4e2694eba1804184a02a7fd13159799e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215660"
---
# <a name="partial-shipment-of-a-transport-load"></a><span data-ttu-id="c247a-103">Delvis levering av en transportlast</span><span class="sxs-lookup"><span data-stu-id="c247a-103">Partial shipment of a transport load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c247a-104">Ved å sette opp delvis levering av laster, kan du håndtere laster der kapasiteten ikke kan fastslås før alle salgslinjene er lagt til en last.</span><span class="sxs-lookup"><span data-stu-id="c247a-104">By setting up partial shipment of loads, you can handle loads where the capacity can't be determined until all the sales lines have been added to a load.</span></span> <span data-ttu-id="c247a-105">Prosessen kan deretter fullføres når det nøyaktige pallantallet er kjent.</span><span class="sxs-lookup"><span data-stu-id="c247a-105">The process can then be finalized when the exact pallet count is known.</span></span> <span data-ttu-id="c247a-106">Du trenger derfor ikke avgjøre hvilke paller som skal tilordnes til hvilken transport før tidspunktet når en transport fysisk lastes ut av lageret.</span><span class="sxs-lookup"><span data-stu-id="c247a-106">Therefore, you don't have to decide which pallets will be assigned to which transport until the moment when a transport is being physically loaded out of the staged inventory.</span></span>

<span data-ttu-id="c247a-107">Denne funksjonen gir et alternativ til en mer fast struktur der du må bestemme hvilke paller som skal tilordnes til hvilken transport før plukkearbeidet eller lastearbeidet kan opprettes.</span><span class="sxs-lookup"><span data-stu-id="c247a-107">This feature offers an alternative to the enforcement of a more rigid structure, where you must determine which pallets will be assigned to which transport before picking work or loading work can be created.</span></span> <span data-ttu-id="c247a-108">I stedet kan brukere konfigurere individuelle laster for en delleveringsbekreftelse.</span><span class="sxs-lookup"><span data-stu-id="c247a-108">Instead, users can configure individual loads for a partial shipment confirmation.</span></span> <span data-ttu-id="c247a-109">Transportlasteprosessene for disse lastene kan deretter utføres.</span><span class="sxs-lookup"><span data-stu-id="c247a-109">The transport loading processes for those loads can then occur.</span></span> <span data-ttu-id="c247a-110">Derfor kan transportplanleggingsavdelingen planlegge laster uten å måtte vurdere kapasiteten til individuelle transporter.</span><span class="sxs-lookup"><span data-stu-id="c247a-110">Therefore, the transportation planning department can plan loads without having to consider the capacity of individual transports.</span></span>

<span data-ttu-id="c247a-111">Når lastingen utføres, kan medarbeidere definere en ny transportlast som en pall kan lastes til.</span><span class="sxs-lookup"><span data-stu-id="c247a-111">At the time of loading, workers can define a new transport load that a pallet can be loaded to.</span></span> <span data-ttu-id="c247a-112">De kan også identifisere en eksisterende transportlast.</span><span class="sxs-lookup"><span data-stu-id="c247a-112">Alternatively, they can identify an existing transport load.</span></span> <span data-ttu-id="c247a-113">Disse dataene kan registreres via en mobilenhet.</span><span class="sxs-lookup"><span data-stu-id="c247a-113">This data can be recorded via a mobile device.</span></span> <span data-ttu-id="c247a-114">Derfor kan flere lagermedarbeidere laste beholdning fra de samme lastene eller ulike laster til samme lastebil.</span><span class="sxs-lookup"><span data-stu-id="c247a-114">Therefore, several warehouse workers can load inventory from the same loads or different loads onto the same truck.</span></span> <span data-ttu-id="c247a-115">Lastene kan deretter helt eller delvis leveres.</span><span class="sxs-lookup"><span data-stu-id="c247a-115">The loads can then be fully or partially shipped.</span></span>

> [!NOTE] 
> <span data-ttu-id="c247a-116">Hvis du vil laste beholdning fra en last til en bestemt transportlast og delvis sende lasten, må arbeid genereres ved hjelp av en lasteklasse i en arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="c247a-116">In order to load inventory from a load to a specific transport load and partially ship the load, work must be generated by using a loading class in a work template.</span></span> <span data-ttu-id="c247a-117">Vanlig plukkarbeid av typen **Plukking** kan ikke lastes til en transportlast som en lastebil.</span><span class="sxs-lookup"><span data-stu-id="c247a-117">Ordinary picking work of the **Picking** type can't be loaded to a transport load such as a truck.</span></span>

## <a name="set-up-transport-loads-for-partial-shipment"></a><span data-ttu-id="c247a-118">Definere transportlaster for delvis forsendelse</span><span class="sxs-lookup"><span data-stu-id="c247a-118">Set up transport loads for partial shipment</span></span>

<span data-ttu-id="c247a-119">Oppsettet for delvis forsendelse av laster består av følgende to fremgangsmåter.</span><span class="sxs-lookup"><span data-stu-id="c247a-119">The setup for partial shipment of loads consists of the following two procedures.</span></span>

### <a name="set-the-loading-strategy"></a><span data-ttu-id="c247a-120">Angi lastestrategien</span><span class="sxs-lookup"><span data-stu-id="c247a-120">Set the loading strategy</span></span>

<span data-ttu-id="c247a-121">Du må aktivere delvis lasting ved å angi lastestrategien.</span><span class="sxs-lookup"><span data-stu-id="c247a-121">You must enable partial loading by setting the loading strategy.</span></span> <span data-ttu-id="c247a-122">Du kan angi lastestrategien når du har opprettet en last.</span><span class="sxs-lookup"><span data-stu-id="c247a-122">You can set the loading strategy after you've created a load.</span></span>

1. <span data-ttu-id="c247a-123">Velg **Lagerstyring** \> **Laster** \> **Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="c247a-123">Select **Warehouse management** \> **Loads** \> **All loads**.</span></span>
2. <span data-ttu-id="c247a-124">Velg en last, og klikk deretter **Hode**.</span><span class="sxs-lookup"><span data-stu-id="c247a-124">Select a load, and then click **Header**.</span></span>
3. <span data-ttu-id="c247a-125">I **Lastestrategi**-feltet velger du **Levering med delvis last tillatt**.</span><span class="sxs-lookup"><span data-stu-id="c247a-125">In the **Loading strategy** field, select **Partial load shipping allowed**.</span></span>

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a><span data-ttu-id="c247a-126">Opprette et menyelement for lasting av transportlaster</span><span class="sxs-lookup"><span data-stu-id="c247a-126">Create a menu item for loading of transport loads</span></span>

<span data-ttu-id="c247a-127">Du må opprette et nytt menyelement som gjør at transportlaster kan lastes.</span><span class="sxs-lookup"><span data-stu-id="c247a-127">You must create a new menu item that enables transport loads to be loaded.</span></span> <span data-ttu-id="c247a-128">En transportlast lar deg gruppere arbeidslinjer fra en last til flere laster.</span><span class="sxs-lookup"><span data-stu-id="c247a-128">A transport load lets you group work lines from one load or multiple loads.</span></span> <span data-ttu-id="c247a-129">Alt som er lagt til transportlasten, kan deretter sendes ved hjelp av en mobil skanner.</span><span class="sxs-lookup"><span data-stu-id="c247a-129">Everything that is added to the transport load can then be shipped by using a mobile scanner.</span></span>

1. <span data-ttu-id="c247a-130">Velg **Lagerstyring** \> **Oppsett** \> **Mobilenhet** \> **Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="c247a-130">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="c247a-131">Velg **Ny**, og deretter i **Modus**-feltet, velg **Arbeid**.</span><span class="sxs-lookup"><span data-stu-id="c247a-131">Select **New**, and then, in the **Mode** field, select **Work**.</span></span>
3. <span data-ttu-id="c247a-132">Angi alternativet **Bruk eksisterende arbeid** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c247a-132">Set the **Use existing work** option to **Yes**.</span></span>
4. <span data-ttu-id="c247a-133">Gå til kategorien **Generelt**, og velg **Transportlasting** i feltet **Styrt av**.</span><span class="sxs-lookup"><span data-stu-id="c247a-133">On the **General** tab, in the **Directed by** field, select **Transport loading**.</span></span>
5. <span data-ttu-id="c247a-134">Hvis du vil aktivere forsendelsesbekreftelse på en mobil skanner, velger **Transportlast** i **Tillatt type forsendelsesbekreftelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c247a-134">To enable shipment confirmation on a mobile scanner, in the **Allowed ship confirmation type** field, select **Transport load**.</span></span>

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a><span data-ttu-id="c247a-135">Bekrefte foresendelse av en transportlast fra klienten</span><span class="sxs-lookup"><span data-stu-id="c247a-135">Confirm shipment of a transport load from the client</span></span>

<span data-ttu-id="c247a-136">I dette oppsettet kan du bekrefte en transportlast som inkluderer en full last eller en delvis lastet last som skal sendes.</span><span class="sxs-lookup"><span data-stu-id="c247a-136">This setup lets you confirm a transport load that includes a full load or a partially loaded load to be shipped.</span></span>

1. <span data-ttu-id="c247a-137">Velg **Lagerstyring** \> **Laster** \> **Transportlaster**.</span><span class="sxs-lookup"><span data-stu-id="c247a-137">Select **Warehouse management** \> **Loads** \> **Transport loads**.</span></span>
2. <span data-ttu-id="c247a-138">Velg **Transport** i **Send og motta**-kategorien i **Bekreft**-gruppen.</span><span class="sxs-lookup"><span data-stu-id="c247a-138">On the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Transport**.</span></span>
