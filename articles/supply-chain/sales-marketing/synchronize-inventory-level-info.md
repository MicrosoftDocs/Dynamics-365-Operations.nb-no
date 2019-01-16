---
title: "Synkronisere informasjon om lagernivå fra Finance and Operations til Field Service"
description: "Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere lagernivåinformasjon fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: nb-no
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="e3fbe-103">Synkronisere informasjon om lagernivå fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="e3fbe-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e3fbe-104">Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere lagernivåinformasjon fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e3fbe-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e3fbe-105">[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="e3fbe-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e3fbe-106">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="e3fbe-106">Templates and tasks</span></span>
<span data-ttu-id="e3fbe-107">Følgende mal og underliggende oppgaver brukes til å synkronisere lagerbeholdningsnivåer fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e3fbe-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e3fbe-108">**Navnet på malen i Dataintegrasjon:**</span><span class="sxs-lookup"><span data-stu-id="e3fbe-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="e3fbe-109">Produktbeholdning (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="e3fbe-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="e3fbe-110">**Navnet på oppgaven i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="e3fbe-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="e3fbe-111">Produktbeholdning</span><span class="sxs-lookup"><span data-stu-id="e3fbe-111">Product inventory</span></span>

<span data-ttu-id="e3fbe-112">Følgende synkroniseringsoppgaver er påkrevd før synkronisering av lagernivåer kan inntreffe:</span><span class="sxs-lookup"><span data-stu-id="e3fbe-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="e3fbe-113">Lagre (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="e3fbe-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="e3fbe-114">Field Service-produkter med lagerenhet (Finance and Operations til Sales)</span><span class="sxs-lookup"><span data-stu-id="e3fbe-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="e3fbe-115">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="e3fbe-115">Entity set</span></span>

| <span data-ttu-id="e3fbe-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="e3fbe-116">Field Service</span></span>                      | <span data-ttu-id="e3fbe-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e3fbe-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="e3fbe-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="e3fbe-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="e3fbe-119">CDS-lagerbeholdning etter lager</span><span class="sxs-lookup"><span data-stu-id="e3fbe-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="e3fbe-120">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="e3fbe-120">Entity flow</span></span>
<span data-ttu-id="e3fbe-121">Lagernivåinformasjon fra Finance and Operations sendes til Field Service for valgte produkter.</span><span class="sxs-lookup"><span data-stu-id="e3fbe-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="e3fbe-122">Lagernivåinformasjonen omfatter:</span><span class="sxs-lookup"><span data-stu-id="e3fbe-122">The inventory level information include:</span></span> 
- <span data-ttu-id="e3fbe-123">Antall på lager (gjeldende registrert fysisk antall som finnes på lageret)</span><span class="sxs-lookup"><span data-stu-id="e3fbe-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="e3fbe-124">Antall i ordre/bestilling (totalt registrert antall i ordre – det vil si salgsordrer)</span><span class="sxs-lookup"><span data-stu-id="e3fbe-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="e3fbe-125">Bestilt antall (totalt registrert bestilt antall – det vil si kjøpsordrer)</span><span class="sxs-lookup"><span data-stu-id="e3fbe-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="e3fbe-126">Denne informasjonen blir registrert per frigitt produkt for hvert lager og synkroniseres basert på endringssporing, når lagernivået endres.</span><span class="sxs-lookup"><span data-stu-id="e3fbe-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="e3fbe-127">I Field Service oppretter integrasjonsløsningen lagerjournaler for delta, for å få nivåene i Field Service til å samsvare med nivåene i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e3fbe-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="e3fbe-128">Finance and Operations fungerer som malen for lagernivåer.</span><span class="sxs-lookup"><span data-stu-id="e3fbe-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="e3fbe-129">Så det er viktig å definere integrering for arbeidsordrer, overføringer og justeringer fra Field Service til Finance and Operations hvis denne funksjonen brukes i Field Service, sammen med synkronisering av lagernivåer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e3fbe-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="e3fbe-130">Produktene og lagrene der lagernivåer styres fra Finance and Operations, kan kontrolleres med avansert spørring og filtrering (Power Query).</span><span class="sxs-lookup"><span data-stu-id="e3fbe-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="e3fbe-131">Obs!  Det er mulig å opprette flere lagre i Field Service (med Vedlikeholdes eksternt = Nei) og så tilordne dem til et enkelt lager i Finance and Operations, med funksjonen for avansert spørring og filtrering.</span><span class="sxs-lookup"><span data-stu-id="e3fbe-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="e3fbe-132">Dette brukes i situasjoner der du vil at Field Service skal styre det detaljerte lagernivået og bare sende oppdateringer til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e3fbe-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="e3fbe-133">I dette tilfellet vil ikke Field Service få lagernivåoppdateringer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e3fbe-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="e3fbe-134">Se tilleggsinformasjon i Synkronisere lagerjusteringer fra Field Service til Finance and Operations og Synkronisere arbeidsordrer i Field Service til salgsordrer knyttet til prosjekt i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e3fbe-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="e3fbe-135">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="e3fbe-135">Field Service CRM solution</span></span>
<span data-ttu-id="e3fbe-136">Den eksterne produktlagerenheten er en ny enhet som bare brukes for serverdelen i integreringen.</span><span class="sxs-lookup"><span data-stu-id="e3fbe-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="e3fbe-137">Den mottar lagernivåverdiene fra Finance and Operations i integreringen og endrer deretter disse verdiene til manuelle lagerjournaler, som deretter endrer lagerproduktene på lageret.</span><span class="sxs-lookup"><span data-stu-id="e3fbe-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e3fbe-138">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="e3fbe-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="e3fbe-139">I dataintegrasjonsprosjektet</span><span class="sxs-lookup"><span data-stu-id="e3fbe-139">In the Data Integration project</span></span>
<span data-ttu-id="e3fbe-140">Bruk filtre med avansert spørring og filtrering for å kontrollere at bare ønskede produkter og lagre sender lagernivåinformasjon fra Finance and Operations til Field Service.</span><span class="sxs-lookup"><span data-stu-id="e3fbe-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e3fbe-141">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="e3fbe-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="e3fbe-142">Produktbeholdning (Finance and Operations til Field Service): Produktbeholdning</span><span class="sxs-lookup"><span data-stu-id="e3fbe-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="e3fbe-143">[![Maltilordning i Dataintegrering](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="e3fbe-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

