---
title: Oversikt over integrering med Microsoft Dynamics 365 Field Service
description: Dette emnet inneholder en oversikt over integreringen med Microsoft Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 2a5c3e49f09bf4f1f90449db10d439f563ecc2c0
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249848"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a><span data-ttu-id="908bf-103">Oversikt over integrering med Microsoft Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="908bf-103">Integration with Microsoft Dynamics 365 Field Service overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="908bf-104">Supply Chain Management gjør det mulig å synkronisere forretningsprosesser mellom Dynamics 365 Supply Chain Management og Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="908bf-104">Supply Chain Management enables synchronization of business processes between Dynamics 365 Supply Chain Management and Dynamics 365 Field Service.</span></span> <span data-ttu-id="908bf-105">Intregrasjonsscenarioene konfigureres ved hjelp av utvidbare Dataintegrator-maler og Common Data Service for å gjøre det mulig med synkronisering av forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="908bf-105">The integration scenarios are configured by using extensible Data integrator templates and Common Data Service to enable the synchronization of business processes.</span></span>
<span data-ttu-id="908bf-106">Standardmaler kan brukes til å lage tilpassede integreringsprosjekter der flere standard og egendefinerte felt, og enheter, kan tilordnes for å justere integreringen og oppfylle spesifikke forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="908bf-106">Standard templates can be used to create custom integration projects, where additional standard and custom fields and entities can be mapped to adjust the integration and meet specific business needs.</span></span> 

<span data-ttu-id="908bf-107">Field Service-integreringen bygger på eksisterende kundeemne til kontanter-funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="908bf-107">The field service integration builds on top of the existing prospect-to-cash functionality.</span></span>

![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service](./media/field-service-integration.png)

<span data-ttu-id="908bf-109">Den første fasen av integreringen mellom Field Service og Supply Chain Management fokuserer på kunne la arbeidsordrer og avtaler i Field Service faktureres i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="908bf-109">The first phase  of the integration between Field Service and Supply Chain Management is focused on enabling work orders and agreements in Field Service to be invoiced in Supply Chain Management.</span></span> <span data-ttu-id="908bf-110">Den støttede flyten starter i Field Service, der informasjonen fra arbeidsordrer synkroniseres til Supply Chain Management som salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="908bf-110">The supported flow starts in Field Service, where information from work orders is synchronized to Supply Chain Management as sales orders.</span></span> <span data-ttu-id="908bf-111">I Supply Chain Management faktureres salgsordrene for å generere fakturadokumenter.</span><span class="sxs-lookup"><span data-stu-id="908bf-111">In Supply Chain Management, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="908bf-112">I tillegg synkroniseres informasjonen fra avtalefakturaer i Field Service til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="908bf-112">In addition, the information from Field Service agreement invoices is synchronized to Supply Chain Management.</span></span> <span data-ttu-id="908bf-113">Microsoft Dynamics 365 Data integrator synkroniserer data ved hjelp av prosjekter som kan tilpasses.</span><span class="sxs-lookup"><span data-stu-id="908bf-113">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="908bf-114">Standardmaler kan brukes til å lage tilpassede integreringsprosjekter der flere standard og egendefinerte felt, og enheter, kan tilordnes for å justere integreringen og oppfylle spesifikke behov.</span><span class="sxs-lookup"><span data-stu-id="908bf-114">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="908bf-115">Den første fasen av integreringen mellom Field Service og Supply Chain Management gjør det mulig med synkronisering av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="908bf-115">The first phase of the integration between Field Service and Supply Chain Management enables synchronization of the following items:</span></span>

- [<span data-ttu-id="908bf-116">Produkter i Supply Chain Management til produkter i Field Service som inneholder produkttypeinformasjon</span><span class="sxs-lookup"><span data-stu-id="908bf-116">Products in Supply Chain Management to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="908bf-117">Arbeidsordrer i Field Service til salgsordrer i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="908bf-117">Work orders in Field Service to sales orders in Supply Chain Management</span></span>](field-service-work-order.md)
- [<span data-ttu-id="908bf-118">Fakturaer i Field Service til fritekstfakturaer i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="908bf-118">Invoices in Field Service to free text invoices in Supply Chain Management</span></span>](field-service-invoice.md)

<span data-ttu-id="908bf-119">Hvis du vil se et eksempel på hvordan du kan synkronisere en arbeidsordre mellom Field Service og Supply Chain Management, se den korte YouTube-videoen [Synkronisere en arbeidsordre med Microsoft Dynamics 365-integrering](https://www.youtube.com/watch?v=46ylO7raZAo).</span><span class="sxs-lookup"><span data-stu-id="908bf-119">To see an example of how you can synchronize a work order between Field Service and Supply Chain Management, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

## <a name="integration-with-field-service-including-inventory-and-project-information"></a><span data-ttu-id="908bf-120">Integrasjon med Field Service, inkludert informasjon om lager og prosjekt</span><span class="sxs-lookup"><span data-stu-id="908bf-120">Integration with Field Service, including inventory and project information</span></span>

<span data-ttu-id="908bf-121">Den ekstra funksjonaliteten i andre fase fokuserer på å gi teknikere innsikt i lagerinformasjon fra Supply Chain Management slik at de kan oppdatere lagernivåer og overføre materiell.</span><span class="sxs-lookup"><span data-stu-id="908bf-121">The additional functionality in this second phase focused on giving field technicians insight about the inventory information from Supply Chain Management, allowing them to update inventory levels and do material transfers.</span></span> <span data-ttu-id="908bf-122">I tillegg vil firmaer som installerer eller vedlikeholder solgte varer, dra nytte av bedre styring og synlighet i hele salgs- og serviceprosessen med integrering fra prosjekter.</span><span class="sxs-lookup"><span data-stu-id="908bf-122">In addition, companies installing or servicing sold goods will benefit from better control and visibility to the full sales and service process with integration from projects.</span></span>

### <a name="functionality-includes-integration-of"></a><span data-ttu-id="908bf-123">Funksjonalitet inkluderer integrering av:</span><span class="sxs-lookup"><span data-stu-id="908bf-123">Functionality includes integration of:</span></span>
- <span data-ttu-id="908bf-124">Lagerinformasjon</span><span class="sxs-lookup"><span data-stu-id="908bf-124">Warehouse information</span></span>
- <span data-ttu-id="908bf-125">Informasjon om lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="908bf-125">On-hand inventory information</span></span>
- <span data-ttu-id="908bf-126">Lageroverføringer</span><span class="sxs-lookup"><span data-stu-id="908bf-126">Inventory transfers</span></span>
- <span data-ttu-id="908bf-127">Lagerjusteringer</span><span class="sxs-lookup"><span data-stu-id="908bf-127">Inventory adjustments</span></span>
- <span data-ttu-id="908bf-128">Supply Chain Management-prosjekter koblet til Dynamics 365 Field Service-arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="908bf-128">Supply Chain Management projects connected with Dynamics 365 Field Service work orders</span></span>
- <span data-ttu-id="908bf-129">Dynamics 365 Field Service-arbeidsordrer med kobling til Supply Chain Management-prosjekter bruker dette prosjektnummeret i salgsordren for å tillate fakturering fra prosjektet.</span><span class="sxs-lookup"><span data-stu-id="908bf-129">Dynamics 365 Field Service work orders with link to Supply Chain Management projects, apply this project number to the sales order to allow invoicing from the project.</span></span> 

![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a><span data-ttu-id="908bf-131">Den andre fasen av integreringen mellom Field Service og Supply Chain Management gjør det mulig med synkronisering med følgende maler:</span><span class="sxs-lookup"><span data-stu-id="908bf-131">The second phase of the integration between Field Service and Supply Chain Management enables synchronization with the following templates:</span></span>
- <span data-ttu-id="908bf-132">Lagre (Supply Chain Management til Field Service) – Lagre fra Supply Chain Management til Field Service [Avansert spørring]</span><span class="sxs-lookup"><span data-stu-id="908bf-132">Warehouses (Supply Chain Management to Field Service) - Warehouses from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="908bf-133">Produktbeholdning (Supply Chain Management til Field Service) – Lagernivåinformasjon fra Supply Chain Management til Field Service [Avansert spørring]</span><span class="sxs-lookup"><span data-stu-id="908bf-133">Product Inventory (Supply Chain Management to Field Service) - Inventory level information from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="908bf-134">Lagerjustering (Field Service til Supply Chain Management) – Lagerjusteringer fra Field Service til Supply Chain Management [Avansert spørring]</span><span class="sxs-lookup"><span data-stu-id="908bf-134">Inventory Adjustment (Field Service to Supply Chain Management) - Inventory adjustments from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="908bf-135">Lageroverføringer (Field Service til Supply Chain Management) – Lageroverføringer fra Field Service til Supply Chain Management [Avansert spørring]</span><span class="sxs-lookup"><span data-stu-id="908bf-135">Inventory Transfers (Field Service to Supply Chain Management) - Inventory transfers from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="908bf-136">Prosjekter (Supply Chain Management til Field Service) – Prosjektliste fra Supply Chain Management til Field Service</span><span class="sxs-lookup"><span data-stu-id="908bf-136">Projects (Supply Chain Management to Field Service) - Project list from Supply Chain Management to Field Service</span></span> 
- <span data-ttu-id="908bf-137">Arbeidsordrer med prosjekt (Field Service til Supply Chain Management) - Arbeidsordrer i Field Service til salgsordrer i Supply Chain Management, med støtte for prosjekt [Avansert spørring]</span><span class="sxs-lookup"><span data-stu-id="908bf-137">Work Orders with Project (Field Service to Supply Chain Management) - Work orders in Field Service to Sales orders  in Supply Chain Management, with support for Project [Advanced Query]</span></span> 
- <span data-ttu-id="908bf-138">Field Service-produkter med lagerenhet (Supply Chain Management til Sales) – Salgbare frigitte produkter i Supply Chain Management til Sales-produkter for Field Service, inkludert lagerenhet</span><span class="sxs-lookup"><span data-stu-id="908bf-138">Field Service Products with Inventory unit (Supply Chain Management to Sales) - Supply Chain Management 'Sellable released products' to Sales 'Products' for Field Service, including Inventory unit</span></span> 

## <a name="system-requirements"></a><span data-ttu-id="908bf-139">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="908bf-139">System requirements</span></span>

### <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="908bf-140">Systemkrav for Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="908bf-140">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="908bf-141">Field Service-integrasjon støtter følgende versjoner:</span><span class="sxs-lookup"><span data-stu-id="908bf-141">Field Service integration supports the following versions:</span></span>

- <span data-ttu-id="908bf-142">Dynamics 365 for Finance and Operations versjon 8.1.2 (desember 2018) ble utgitt i desember 2018 og har programbyggnummer 8.1.195 med Platform update 22 (7.0.5095).</span><span class="sxs-lookup"><span data-stu-id="908bf-142">Dynamics 365 for Finance and Operations version 8.1.2 (December 2018) was released in December 2018 and has an application build number 8.1.195 with Platform update 22 (7.0.5095).</span></span> 

### <a name="system-requirements-for-field-service"></a><span data-ttu-id="908bf-143">Systemkrav for Field Service</span><span class="sxs-lookup"><span data-stu-id="908bf-143">System requirements for Field Service</span></span>
<span data-ttu-id="908bf-144">For å bruke Field Service-integrasjonsløsningen må du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="908bf-144">To use the Field Service integration solution, you must install the following components:</span></span>

- <span data-ttu-id="908bf-145">Field Service (versjon 8.2.0.286) eller en nyere versjon på Dynamics 365 9.1.x – utgitt november 2018</span><span class="sxs-lookup"><span data-stu-id="908bf-145">Field Service (version 8.2.0.286) or a later version on Dynamics 365 9.1.x - Released November 2018</span></span>
- <span data-ttu-id="908bf-146">Prospect to Cash (P2C)-løsningen for Dynamics 365, versjon 1.15.0.1 eller en nyere versjon.</span><span class="sxs-lookup"><span data-stu-id="908bf-146">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="908bf-147">Løsningen er tilgjengelig for nedlasting fra [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="908bf-147">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="908bf-148">Field Service Integration, Project and Inventory-løsningen for Dynamics 365, versjon 2.0.0.0 eller en nyere versjon.</span><span class="sxs-lookup"><span data-stu-id="908bf-148">'Field Service Integration, Project and Inventory' solution for Dynamics 365, version 2.0.0.0 or a later version.</span></span> <span data-ttu-id="908bf-149">Løsningen er tilgjengelig for nedlasting fra [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span><span class="sxs-lookup"><span data-stu-id="908bf-149">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span></span>
