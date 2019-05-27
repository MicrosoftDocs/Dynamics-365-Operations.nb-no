---
title: Synkronisere informasjon om lagernivå fra Finance and Operations til Field Service
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagernivåinformasjon fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c7dce4427810b93e0ee4f1a27881c2b1b04fb125
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535704"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="53ae0-103">Synkronisere informasjon om lagernivå fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="53ae0-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="53ae0-104">Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagernivåinformasjon fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="53ae0-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="53ae0-105">[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="53ae0-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="53ae0-106">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="53ae0-106">Templates and tasks</span></span>
<span data-ttu-id="53ae0-107">Følgende mal og underliggende oppgaver brukes til å synkronisere lagerbeholdningsnivåer fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="53ae0-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="53ae0-108">**Mal i Dataintegrasjon**</span><span class="sxs-lookup"><span data-stu-id="53ae0-108">**Template in Data integration**</span></span>
- <span data-ttu-id="53ae0-109">Produktbeholdning (Fin and Ops til Field Service)</span><span class="sxs-lookup"><span data-stu-id="53ae0-109">Product Inventory (Fin and Ops to Field Service)</span></span>
  
<span data-ttu-id="53ae0-110">**Oppgave i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="53ae0-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="53ae0-111">Produktbeholdning</span><span class="sxs-lookup"><span data-stu-id="53ae0-111">Product inventory</span></span>

<span data-ttu-id="53ae0-112">Følgende synkroniseringsoppgaver er påkrevd før synkronisering av lagernivåer kan inntreffe:</span><span class="sxs-lookup"><span data-stu-id="53ae0-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="53ae0-113">Lagre (Fin and Ops til Field Service)</span><span class="sxs-lookup"><span data-stu-id="53ae0-113">Warehouses (Fin and Ops to Field Service)</span></span> 
- <span data-ttu-id="53ae0-114">Field Service-produkter med lagerenhet (Fin and Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="53ae0-114">Field Service products with Inventory unit (Fin and Ops to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="53ae0-115">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="53ae0-115">Entity set</span></span>

| <span data-ttu-id="53ae0-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="53ae0-116">Field Service</span></span>                      | <span data-ttu-id="53ae0-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="53ae0-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="53ae0-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="53ae0-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="53ae0-119">CDS-lagerbeholdning etter lager</span><span class="sxs-lookup"><span data-stu-id="53ae0-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="53ae0-120">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="53ae0-120">Entity flow</span></span>
<span data-ttu-id="53ae0-121">Lagernivåinformasjon fra Finance and Operations sendes til Field Service for valgte produkter.</span><span class="sxs-lookup"><span data-stu-id="53ae0-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="53ae0-122">Lagernivåinformasjonen inkluderer:</span><span class="sxs-lookup"><span data-stu-id="53ae0-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="53ae0-123">Antall på lager (gjeldende registrert fysisk antall som finnes på lageret)</span><span class="sxs-lookup"><span data-stu-id="53ae0-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="53ae0-124">Antall i ordre/bestilling (totalt registrert antall i ordre, for eksempel salgsordrer)</span><span class="sxs-lookup"><span data-stu-id="53ae0-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="53ae0-125">Bestilt antall (totalt registrert bestilt antall, for eksempel kjøpsordrer)</span><span class="sxs-lookup"><span data-stu-id="53ae0-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="53ae0-126">Denne informasjonen blir registrert per frigitt produkt for hvert lager og synkroniseres basert på endringssporing, når lagernivået endres.</span><span class="sxs-lookup"><span data-stu-id="53ae0-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="53ae0-127">I Field Service oppretter integrasjonsløsningen lagerjournaler for delta, slik at nivåene i Field Service samsvarer med nivåene i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="53ae0-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="53ae0-128">Finance and Operations fungerer som malen for lagernivåer.</span><span class="sxs-lookup"><span data-stu-id="53ae0-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="53ae0-129">Så det er viktig å definere integrering for arbeidsordrer, overføringer og justeringer fra Field Service til Finance and Operations hvis denne funksjonen brukes i Field Service, sammen med synkronisering av lagernivåer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="53ae0-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="53ae0-130">Produktene og lagrene der lagernivåer styres fra Finance and Operations, kan kontrolleres med avansert spørring og filtrering (Power Query).</span><span class="sxs-lookup"><span data-stu-id="53ae0-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="53ae0-131">Det er mulig å opprette flere lagre i Field Service (med **Vedlikeholdes eksternt = Nei**) og så tilordne dem til et enkelt lager i Finance and Operations, med funksjonen for avansert spørring og filtrering.</span><span class="sxs-lookup"><span data-stu-id="53ae0-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="53ae0-132">Dette brukes i situasjoner der du vil at Field Service skal styre det detaljerte lagernivået og bare sende oppdateringer til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="53ae0-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="53ae0-133">I dette tilfellet vil ikke Field Service få lagernivåoppdateringer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="53ae0-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="53ae0-134">For tilleggsinformasjon se [Synkronisere lagerjusteringer fra Field Service til Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbeidsordrer i Field Service til salgsordrer knyttet til prosjekt i Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="53ae0-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="53ae0-135">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="53ae0-135">Field Service CRM solution</span></span>
<span data-ttu-id="53ae0-136">Enheten **Eksternt produktlager** brukes bare for serverdelen i integreringen.</span><span class="sxs-lookup"><span data-stu-id="53ae0-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="53ae0-137">Denne enheten mottar lagernivåverdiene fra Finance and Operations i integreringen og endrer deretter disse verdiene til manuelle lagerjournaler, som deretter endrer lagerproduktene på lageret.</span><span class="sxs-lookup"><span data-stu-id="53ae0-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="53ae0-138">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="53ae0-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="53ae0-139">Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="53ae0-139">Data integration</span></span>
<span data-ttu-id="53ae0-140">For at prosjektet skal fungere må du kontrollere at integreringsnøkkelen er oppdatert for msdynce_externalproductinventories.</span><span class="sxs-lookup"><span data-stu-id="53ae0-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="53ae0-141">Gå til **Dataintegrering > Tilkoblingssett**.</span><span class="sxs-lookup"><span data-stu-id="53ae0-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="53ae0-142">Velg tilkoblingssettet som brukes.</span><span class="sxs-lookup"><span data-stu-id="53ae0-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="53ae0-143">I kategorien **Integreringsnøkkel** kontrollerer du at følgende nøkler er lagt til msdynce_externalproductinventories:</span><span class="sxs-lookup"><span data-stu-id="53ae0-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="53ae0-144">msdynce_productnumber (produktnummer)</span><span class="sxs-lookup"><span data-stu-id="53ae0-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="53ae0-145">msdynce_warehouseid (lager-ID)</span><span class="sxs-lookup"><span data-stu-id="53ae0-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="53ae0-146">Dataintegrasjonsprosjekt</span><span class="sxs-lookup"><span data-stu-id="53ae0-146">Data integration project</span></span>
<span data-ttu-id="53ae0-147">Du kan bruke filtre med avansert spørring og filtrering slik at bare bestemte produkter og lagre sender lagernivåinformasjon fra Finance and Operations til Field Service.</span><span class="sxs-lookup"><span data-stu-id="53ae0-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="53ae0-148">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="53ae0-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a><span data-ttu-id="53ae0-149">Produktbeholdning (Fin and Ops til Field Service): Produktbeholdning</span><span class="sxs-lookup"><span data-stu-id="53ae0-149">Product inventory (Fin and Ops to Field Service): Product inventory</span></span>

<span data-ttu-id="53ae0-150">[![Maltilordning i Dataintegrering](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="53ae0-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
