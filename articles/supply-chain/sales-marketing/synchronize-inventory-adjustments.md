---
title: "Synkronisere lageroverføringer og -justeringer fra Field Service til Finance and Operations"
description: "Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere beholdningsjusteringer og -overføringer fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: nb-no
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="a6d8d-103">Synkronisere lagerjusteringer fra Field Service til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6d8d-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a6d8d-104">Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere beholdningsjusteringer og -overføringer fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="a6d8d-105">[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="a6d8d-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a6d8d-106">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="a6d8d-106">Templates and tasks</span></span>
<span data-ttu-id="a6d8d-107">Følgende mal og underliggende oppgaver brukes til å synkronisere beholdningsjusteringer og -overføringer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="a6d8d-108">**Navn på malene i Dataintegrasjon:**</span><span class="sxs-lookup"><span data-stu-id="a6d8d-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="a6d8d-109">Lagerjustering (Field Service til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="a6d8d-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="a6d8d-110">Lageroverføringer (Field Service til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="a6d8d-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="a6d8d-111">**Navn på oppgavene i Dataintegrasjonprosjektene**:</span><span class="sxs-lookup"><span data-stu-id="a6d8d-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="a6d8d-112">Lagerjusteringer</span><span class="sxs-lookup"><span data-stu-id="a6d8d-112">Inventory Adjustments</span></span>
- <span data-ttu-id="a6d8d-113">Lageroverføringer</span><span class="sxs-lookup"><span data-stu-id="a6d8d-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="a6d8d-114">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="a6d8d-114">Entity set</span></span>
| <span data-ttu-id="a6d8d-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="a6d8d-115">Field Service</span></span>                     | <span data-ttu-id="a6d8d-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6d8d-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="a6d8d-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="a6d8d-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="a6d8d-118">Overskrifter og linjer i CDS-lagerjusteringsjournal</span><span class="sxs-lookup"><span data-stu-id="a6d8d-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="a6d8d-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="a6d8d-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="a6d8d-120">Overskrifter og linjer i CDS-lageroverføringsjournal</span><span class="sxs-lookup"><span data-stu-id="a6d8d-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="a6d8d-121">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="a6d8d-121">Entity flow</span></span>
<span data-ttu-id="a6d8d-122">Lagerjusteringer og -overføringer som er gjort i Field Service, synkroniseres til Finance and Operations når **posteringsstatusen** endres fra Opprettet til Postert.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="a6d8d-123">Når dette skjer, låses justerings- eller overføringsordren og blir skrivebeskyttet siden justeringer og overføringer kan posteres i Finance and Operations og derfor ikke kan endres.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="a6d8d-124">Du kan definere en satsvis jobb i Finance and Operations for å postere automatisk lagerjournalene for justeringene og overføringene som genereres med integreringen.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="a6d8d-125">Se forutsetning under for mer informasjon om hvordan du aktiverer den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="a6d8d-126">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="a6d8d-126">Field Service CRM solution</span></span> 
<span data-ttu-id="a6d8d-127">Feltet Lagerenhet er lagt til produktenheten.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="a6d8d-128">Dette feltet er nødvendig ettersom salgs- og lagerenheten ikke alltid er den samme i Operations, og for lagerbeholdningen i Operations trenger vi lagerenheten.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="a6d8d-129">Når du angir produktet for et lagerjusteringsprodukt for både lagerjusteringer og lageroverføringer, hentes enheten fra verdien for lagerprodukt for produkter.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="a6d8d-130">Hvis en verdi blir funnet, låses Enhet-feltet for lagerjusteringsproduktet.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="a6d8d-131">Posteringsstatusfeltet er lagt til både enheten for lagerjustering og enheten for lageroverføring.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="a6d8d-132">Dette feltet brukes som filter for når en justering eller overføring sendes til Operations.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="a6d8d-133">Feltet settes som standard til Opprettet (1), og blir dermed ikke sendt til Operations.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="a6d8d-134">Når du endrer det til Postert (2), sendes det til Operations, men du vil da ikke lenger kunne endre noe i justeringen eller overføringen eller legge til nye linjer i den.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="a6d8d-135">Feltet Nummerserie er lagt til produktenheten for lagerjustering.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="a6d8d-136">Dette feltet gjør at integreringen har et unikt nummer, slik at integreringen vet når opprettinger og oppdateringer skal gjøres.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="a6d8d-137">Når du oppretter det første lagerjusteringsproduktet, opprettes det en ny post i P2C Autonummer-enheten for å vedlikeholde nummerserien og prefikset som brukes.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="a6d8d-138">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="a6d8d-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="a6d8d-139">I Finance og Operations</span><span class="sxs-lookup"><span data-stu-id="a6d8d-139">In Finance and Operations</span></span>
<span data-ttu-id="a6d8d-140">Integreringslagerjournalene som genereres i integreringen, kan posteres automatisk med en satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="a6d8d-141">Dette aktiveres fra: Lagerstyring > Periodiske oppgaver > CDS-integrering > Poster lagerjournaler for integrering</span><span class="sxs-lookup"><span data-stu-id="a6d8d-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a6d8d-142">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="a6d8d-142">Template mapping in Data integration</span></span>

<span data-ttu-id="a6d8d-143">Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="a6d8d-144">Lagerjustering (Field Service til Finance and Operations): Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="a6d8d-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="a6d8d-145">[![Maltilordning i Dataintegrering](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="a6d8d-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="a6d8d-146">Lageroverføring (Field Service til Finance and Operations): Lageroverføring</span><span class="sxs-lookup"><span data-stu-id="a6d8d-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="a6d8d-147">[![Maltilordning i Dataintegrering](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="a6d8d-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

