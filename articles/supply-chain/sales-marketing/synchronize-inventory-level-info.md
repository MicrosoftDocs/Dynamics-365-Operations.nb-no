---
title: Synkronisere informasjon om lagernivå fra Supply Chain Management til Field Service
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagernivåinformasjon fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c0db0c143abb8ce26a4a3007845050e4ddb02363
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840587"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="23ab6-103">Synkronisere informasjon om lagernivå fra Supply Chain Management til Field Service</span><span class="sxs-lookup"><span data-stu-id="23ab6-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="23ab6-104">Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagernivåinformasjon fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="23ab6-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="23ab6-105">[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="23ab6-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="23ab6-106">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="23ab6-106">Templates and tasks</span></span>
<span data-ttu-id="23ab6-107">Følgende mal og underliggende oppgaver brukes til å synkronisere lagerbeholdningsnivåer fra Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="23ab6-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="23ab6-108">**Mal i Dataintegrasjon**</span><span class="sxs-lookup"><span data-stu-id="23ab6-108">**Template in Data integration**</span></span>
- <span data-ttu-id="23ab6-109">Produktbeholdning (Supply Chain Management til Field Service)</span><span class="sxs-lookup"><span data-stu-id="23ab6-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="23ab6-110">**Oppgave i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="23ab6-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="23ab6-111">Produktbeholdning</span><span class="sxs-lookup"><span data-stu-id="23ab6-111">Product inventory</span></span>

<span data-ttu-id="23ab6-112">Følgende synkroniseringsoppgaver er påkrevd før synkronisering av lagernivåer kan inntreffe:</span><span class="sxs-lookup"><span data-stu-id="23ab6-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="23ab6-113">Lagre (Supply Chain Management til Field Service)</span><span class="sxs-lookup"><span data-stu-id="23ab6-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="23ab6-114">Field Service-produkter med lagerenhet (Supply Chain Management til Sales)</span><span class="sxs-lookup"><span data-stu-id="23ab6-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="23ab6-115">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="23ab6-115">Entity set</span></span>

| <span data-ttu-id="23ab6-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="23ab6-116">Field Service</span></span>                      | <span data-ttu-id="23ab6-117">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="23ab6-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="23ab6-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="23ab6-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="23ab6-119">Dataverse-lagerbeholdning etter lager</span><span class="sxs-lookup"><span data-stu-id="23ab6-119">Dataverse inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="23ab6-120">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="23ab6-120">Entity flow</span></span>
<span data-ttu-id="23ab6-121">Lagernivåinformasjon fra Finance and Operations sendes til Field Service for valgte produkter.</span><span class="sxs-lookup"><span data-stu-id="23ab6-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="23ab6-122">Lagernivåinformasjonen inkluderer:</span><span class="sxs-lookup"><span data-stu-id="23ab6-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="23ab6-123">Antall på lager (gjeldende registrert fysisk antall som finnes på lageret)</span><span class="sxs-lookup"><span data-stu-id="23ab6-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="23ab6-124">Antall i ordre/bestilling (totalt registrert antall i ordre, for eksempel salgsordrer)</span><span class="sxs-lookup"><span data-stu-id="23ab6-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="23ab6-125">Bestilt antall (totalt registrert bestilt antall, for eksempel kjøpsordrer)</span><span class="sxs-lookup"><span data-stu-id="23ab6-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="23ab6-126">Denne informasjonen blir registrert per frigitt produkt for hvert lager og synkroniseres basert på endringssporing, når lagernivået endres.</span><span class="sxs-lookup"><span data-stu-id="23ab6-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="23ab6-127">I Field Service oppretter integrasjonsløsningen lagerjournaler for delta, slik at nivåene i Field Service samsvarer med nivåene i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="23ab6-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="23ab6-128">Supply Chain Management fungerer som malen for lagernivåer.</span><span class="sxs-lookup"><span data-stu-id="23ab6-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="23ab6-129">Så det er viktig å definere integrering for arbeidsordrer, overføringer og justeringer fra Field Service til Supply Chain Management hvis denne funksjonen brukes i Field Service, sammen med synkronisering av lagernivåer fra Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="23ab6-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="23ab6-130">Produktene og lagrene der lagernivåer styres fra Supply Chain Management, kan kontrolleres med avansert spørring og filtrering (Power Query).</span><span class="sxs-lookup"><span data-stu-id="23ab6-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="23ab6-131">Det er mulig å opprette flere lagre i Field Service (med **Vedlikeholdes eksternt = Nei**) og så tilordne dem til et enkelt lager i Supply Chain Management, med funksjonen for avansert spørring og filtrering.</span><span class="sxs-lookup"><span data-stu-id="23ab6-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="23ab6-132">Dette brukes i situasjoner der du vil at Field Service skal styre det detaljerte lagernivået og bare sende oppdateringer til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="23ab6-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="23ab6-133">I dette tilfellet vil ikke Field Service få lagernivåoppdateringer fra Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="23ab6-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="23ab6-134">For tilleggsinformasjon se [Synkronisere lagerjusteringer fra Field Service til Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbeidsordrer i Field Service til salgsordrer knyttet til prosjekt i Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="23ab6-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="23ab6-135">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="23ab6-135">Field Service CRM solution</span></span>
<span data-ttu-id="23ab6-136">Enheten **Eksternt produktlager** brukes bare for serverdelen i integreringen.</span><span class="sxs-lookup"><span data-stu-id="23ab6-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="23ab6-137">Denne enheten mottar lagernivåverdiene fra Supply Chain Management i integreringen og endrer deretter disse verdiene til manuelle lagerjournaler, som deretter endrer lagerproduktene på lageret.</span><span class="sxs-lookup"><span data-stu-id="23ab6-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="23ab6-138">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="23ab6-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="23ab6-139">Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="23ab6-139">Data integration</span></span>
<span data-ttu-id="23ab6-140">For at prosjektet skal fungere må du kontrollere at integreringsnøkkelen er oppdatert for msdynce_externalproductinventories.</span><span class="sxs-lookup"><span data-stu-id="23ab6-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="23ab6-141">Gå til **Dataintegrering > Tilkoblingssett**.</span><span class="sxs-lookup"><span data-stu-id="23ab6-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="23ab6-142">Velg tilkoblingssettet som brukes.</span><span class="sxs-lookup"><span data-stu-id="23ab6-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="23ab6-143">I fanen **Integreringsnøkkel** kontrollerer du at følgende nøkler er lagt til msdynce_externalproductinventories:</span><span class="sxs-lookup"><span data-stu-id="23ab6-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="23ab6-144">msdynce_productnumber (produktnummer)</span><span class="sxs-lookup"><span data-stu-id="23ab6-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="23ab6-145">msdynce_warehouseid (lager-ID)</span><span class="sxs-lookup"><span data-stu-id="23ab6-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="23ab6-146">Dataintegrasjonsprosjekt</span><span class="sxs-lookup"><span data-stu-id="23ab6-146">Data integration project</span></span>
<span data-ttu-id="23ab6-147">Du kan bruke filtre med avansert spørring og filtrering slik at bare bestemte produkter og lagre sender lagernivåinformasjon fra Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="23ab6-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="23ab6-148">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="23ab6-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="23ab6-149">Produktbeholdning (Supply Chain Management til Field Service): Produktbeholdning</span><span class="sxs-lookup"><span data-stu-id="23ab6-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="23ab6-150">[![Maltilordning i Dataintegrering](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="23ab6-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]