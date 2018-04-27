---
title: Oversikt over transportstyring
description: Dette emnet gir en oversikt over transportstyringsfunksjonaliteten i Microsoft Dynamics 365 for Finance and Operations
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f4dc2c15d35d93d1563c866b20ad7f2bbb5c8457
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="transportation-management-overview"></a><span data-ttu-id="9bb16-103">Oversikt over transportstyring</span><span class="sxs-lookup"><span data-stu-id="9bb16-103">Transportation management overview</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="9bb16-104">Dette emnet gir en oversikt over transportstyringsfunksjonaliteten i Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9bb16-104">This topic gives an overview of the transportation management functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="9bb16-105">Transportstyring lar deg bruke bedriftens transport, og lar deg også identifisere leverandør- og rutingsløsninger for innkommende og utgående bestillinger.</span><span class="sxs-lookup"><span data-stu-id="9bb16-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="9bb16-106">Du kan for eksempel identifisere den raskeste ruten eller den billigste for en forsendelse.</span><span class="sxs-lookup"><span data-stu-id="9bb16-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="9bb16-107">I tabellen nedenfor beskrives hovedscenariene for bruk av Transportstyring i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9bb16-107">The following table describes the main scenarios for using Transportation management in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9bb16-108">Scenario</span><span class="sxs-lookup"><span data-stu-id="9bb16-108">Scenario</span></span></th>
<th><span data-ttu-id="9bb16-109">Hvordan Transportstyring kan hjelpe</span><span class="sxs-lookup"><span data-stu-id="9bb16-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9bb16-110">Bruk eksterne logistikkleverandører for transportaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="9bb16-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="9bb16-111">Bruk Transportstuyring til innkommende og utgående transport.</span><span class="sxs-lookup"><span data-stu-id="9bb16-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bb16-112">Firmaets egen flåte er tilgjengelige for levering/henting, og leveringsavgifter sendes videre til kunder.</span><span class="sxs-lookup"><span data-stu-id="9bb16-112">The company&#39;s own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="9bb16-113">For utgående prosesser kan du bruke Transportstyring til å finne transporttilleggene og sende dem videre til kundene.</span><span class="sxs-lookup"><span data-stu-id="9bb16-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="9bb16-114">Det er imidlertid ikke nødvendig å avstemme transportørfakturaen.</span><span class="sxs-lookup"><span data-stu-id="9bb16-114">However, the carrier invoice reconciliation process isn&#39;t required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9bb16-115">Firmaets egen flåte er tilgjengelige for levering/henting, men leveringstillegg sendes ikke videre til kunder, fordi produktprisene inkluderer transport.</span><span class="sxs-lookup"><span data-stu-id="9bb16-115">The company&#39;s own fleet is available for delivery/pickup, but delivery charges aren&#39;t passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="9bb16-116">Mye av funksjonaliteten i Transportstyring er ikke nødvendig å bruke.</span><span class="sxs-lookup"><span data-stu-id="9bb16-116">A lot of the Transportation management functionality isn&#39;t required.</span></span> <span data-ttu-id="9bb16-117">Du kan imidlertid bruke Transportstyring for å finne satsene for transport og justere salgsprisen tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="9bb16-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bb16-118">Logistikktjenesten tilbys av en annen juridisk enhet i det samme firmaet.</span><span class="sxs-lookup"><span data-stu-id="9bb16-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="9bb16-119">Du kan bruke Transportstyring ved å behandle den andre juridiske enheten som enhver annen andre transportør.</span><span class="sxs-lookup"><span data-stu-id="9bb16-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="9bb16-120">Du kan ikke automatisere de økonomiske transaksjonene mellom juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="9bb16-120">You can&#39;t automate the economic transactions between legal entities.</span></span> <span data-ttu-id="9bb16-121">Derfor må du behandle disse transaksjonene manuelt (for eksempel ved å opprette en bestilling).</span><span class="sxs-lookup"><span data-stu-id="9bb16-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="9bb16-122">I den juridiske enheten som sørger for logistikktjenestene, kan Transportstyrng brukes til å bestemme transportsatser.</span><span class="sxs-lookup"><span data-stu-id="9bb16-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a><span data-ttu-id="9bb16-123">Planlegge transport i Finance og Operations</span><span class="sxs-lookup"><span data-stu-id="9bb16-123">Planning transportation in Finance and Operations</span></span>
<span data-ttu-id="9bb16-124">I Transportstyring kan transportplanlegging baseres på ordrer eller på forsendelsene som opprettes basert på disse ordrene.</span><span class="sxs-lookup"><span data-stu-id="9bb16-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="9bb16-125">Forsendelsene finnes alltid på et bestemt tidspunkt, men de kreves ikke for planlegging av transport.</span><span class="sxs-lookup"><span data-stu-id="9bb16-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="9bb16-126">Overføringsordrer inngår i det utgående scenariet og kan planlegges sammen med salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="9bb16-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![Laste inn tegning](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="9bb16-128">Innkommende transport</span><span class="sxs-lookup"><span data-stu-id="9bb16-128">Inbound transportation</span></span>
<span data-ttu-id="9bb16-129">Når du bestiller varer fra en leverandør og varene må leveres til lageret, kan det være aktuelt å ordne med transporten av varene selv.</span><span class="sxs-lookup"><span data-stu-id="9bb16-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="9bb16-130">Du kan bruke Dynamics 365 for Operations til å planlegge transport og mottak av en innkommende last.</span><span class="sxs-lookup"><span data-stu-id="9bb16-130">You can use Finance and Operations to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="9bb16-131">Illustrasjonen nedenfor viser forretningsprosessflyten for planlegging av transport for en innkommende last.</span><span class="sxs-lookup"><span data-stu-id="9bb16-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![Forretningsprosessflyt for transport av innkommende last](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="9bb16-133">Utgående transport</span><span class="sxs-lookup"><span data-stu-id="9bb16-133">Outbound transportation</span></span>
<span data-ttu-id="9bb16-134">Du kan planlegge og behandle en utgående last for å sende bestemte varer fra lageret for et firma til en kunde.</span><span class="sxs-lookup"><span data-stu-id="9bb16-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="9bb16-135">Du kan bruke Dynamics 365 for Operations til å planlegge transport forsendelse av en utgående last.</span><span class="sxs-lookup"><span data-stu-id="9bb16-135">You can use Finance and Operations to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="9bb16-136">Illustrasjonen nedenfor viser forretningsprosessflyten for planlegging og behandling av utgående laster for forsendelse.</span><span class="sxs-lookup"><span data-stu-id="9bb16-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![Planlegge og behandle utgående laster](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="9bb16-138">Lastplanlegging</span><span class="sxs-lookup"><span data-stu-id="9bb16-138">Load building</span></span>
<span data-ttu-id="9bb16-139">Finance and Operations inneholder strategi for bygging av laster som heter Volumbasert lastplanleggingsstrategi.</span><span class="sxs-lookup"><span data-stu-id="9bb16-139">Finance and Operations provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="9bb16-140">Med denne strategien kan du bruke de maksimale verdiene som er angitt for høyde og vekt i lastmalen, eller du kan overstyre innstillingene ved å angi nye verdier.</span><span class="sxs-lookup"><span data-stu-id="9bb16-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="9bb16-141">Hvis du vil bruke denne strategien, velger du den i feltet **Strategi for lastplanlegging** i hurtigfanen **Oppsett** på siden **Arbeidsområde for lastplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="9bb16-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="9bb16-142">I tillegg kan du legge til dine egne strategier for lastplanlegging ved å opprette en ny klasse i applikasjonsobjekttreet (AOT).</span><span class="sxs-lookup"><span data-stu-id="9bb16-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>




