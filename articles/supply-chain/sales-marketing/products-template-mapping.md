---
title: Synkronisere produkter fra Finance and Operations til produkter i Sales
description: "Dette emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations, Enterprise edition til Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 405a6cf9f3e6cc52925ff7d9f10836196343c36b
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="38b7b-103">Synkronisere produkter fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="38b7b-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="38b7b-104">Før du kan bruke kundeemnet til kontanter løsning, ha kjennskap til [Dynamics 365 dataintegrering](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="38b7b-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="38b7b-105">Dette emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations, Enterprise edition til Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="38b7b-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="38b7b-106">Mal og oppgave</span><span class="sxs-lookup"><span data-stu-id="38b7b-106">Template and task</span></span>

<span data-ttu-id="38b7b-107">Følgende maler og underliggende oppgaver brukes til å synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) til Microsoft Dynamics 365 for Sales (Sales).</span><span class="sxs-lookup"><span data-stu-id="38b7b-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="38b7b-108">Navnet på malen: Produkter (Finance and Operations til Sales)</span><span class="sxs-lookup"><span data-stu-id="38b7b-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="38b7b-109">Navnet på oppgaven i prosjektet: Produkter</span><span class="sxs-lookup"><span data-stu-id="38b7b-109">Name of task in project: Products</span></span>

<span data-ttu-id="38b7b-110">Synkronisere oppgaver som kreves synkronisering av produkt: Ingen</span><span class="sxs-lookup"><span data-stu-id="38b7b-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="38b7b-111">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="38b7b-111">Entity set</span></span>

| <span data-ttu-id="38b7b-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="38b7b-112">**Finance and Operations**</span></span> | <span data-ttu-id="38b7b-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="38b7b-113">**CDS**</span></span> | <span data-ttu-id="38b7b-114">**Salg**</span><span class="sxs-lookup"><span data-stu-id="38b7b-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="38b7b-115">Salgbare frigitte produkter</span><span class="sxs-lookup"><span data-stu-id="38b7b-115">Sellable released products</span></span> | <span data-ttu-id="38b7b-116">Produkt</span><span class="sxs-lookup"><span data-stu-id="38b7b-116">Product</span></span> | <span data-ttu-id="38b7b-117">Produkter</span><span class="sxs-lookup"><span data-stu-id="38b7b-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="38b7b-118">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="38b7b-118">Entity flow</span></span>

<span data-ttu-id="38b7b-119">Produkter administreres i Finance and Operations og synkroniseres med Sales.</span><span class="sxs-lookup"><span data-stu-id="38b7b-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="38b7b-120">Dataenheten **Salgbare frigitte produkter** i Finance and Operations eksporterer bare produkter som er salgbare, som betyr at produktene har informasjonen som kreves for å brukes på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="38b7b-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="38b7b-121">De samme reglene gjelder når et produkt er bekreftet med **Valider**-funksjonen på siden **Frigitt produkt**.</span><span class="sxs-lookup"><span data-stu-id="38b7b-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="38b7b-122">**Produktnummer** brukes som nøkkel, noe som betyr at produktvarianter synkroniseres til CDS og Sales med individuelle **produkt-ID-er** per **produktvariant**.</span><span class="sxs-lookup"><span data-stu-id="38b7b-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="38b7b-123">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="38b7b-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="38b7b-124">I Sales legges det til et nytt felt på produktene **Vedlikeholdes eksternt** for å angi at et bestemt produkt vedlikeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="38b7b-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="38b7b-125">Verdien er satt til **Ja** som standard under import til Sales.</span><span class="sxs-lookup"><span data-stu-id="38b7b-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="38b7b-126">**Vedlikeholdes eksternt = Ja**: Product stammer fra Finance and Operations og kan ikke redigeres i Sales.</span><span class="sxs-lookup"><span data-stu-id="38b7b-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="38b7b-127">**Vedlikeholdes eksternt = Nei**: Produktet angis direkte i Sales.</span><span class="sxs-lookup"><span data-stu-id="38b7b-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="38b7b-128">**Vedlikeholdes eksternt = tom**: Produktet finnes i Sales før aktivering av kundeemnet til kontantløsning.</span><span class="sxs-lookup"><span data-stu-id="38b7b-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="38b7b-129">Informasjonen i **Vedlikeholdes eksternt** brukes til å sikre at bare **tilbud** og **ordrer** med **eksternt vedlikeholdte produkter** synkroniseres til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="38b7b-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="38b7b-130">**Eksternt vedlikeholdte produkter** legges automatisk til den første gyldige **prislisten** med samme valuta.</span><span class="sxs-lookup"><span data-stu-id="38b7b-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="38b7b-131">Legg merke til at listen er sortert alfabetisk etter **navn**.</span><span class="sxs-lookup"><span data-stu-id="38b7b-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="38b7b-132">Produktets salgspris fra Finance and Operations brukes som prisen på **prislisten**.</span><span class="sxs-lookup"><span data-stu-id="38b7b-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="38b7b-133">Dette betyr at det må være en **prisliste** i Sales for hver **produktsalgsvaluta** i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="38b7b-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="38b7b-134">Valuta på frigitte salgbare produkter er satt til regnskapsvalutaen i den juridiske enheten som produktet er eksportert fra.</span><span class="sxs-lookup"><span data-stu-id="38b7b-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="38b7b-135">Produktsynkronisering kan ikke fullføres uten en **prisliste** med tilhørende valuta.</span><span class="sxs-lookup"><span data-stu-id="38b7b-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="38b7b-136">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="38b7b-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="38b7b-137">Før du kjører den første synkroniseringen, må du fylle ut den **spesifikke produkttabellen** for eksisterende produkter i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="38b7b-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="38b7b-138">Eksisterende produkter vil ikke bli synkronisert før denne jobben er fullført.</span><span class="sxs-lookup"><span data-stu-id="38b7b-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="38b7b-139">I Finance and Operations kan du bruke Søk til å søke etter **Fyll ut tabell for spesifikt produkt**.</span><span class="sxs-lookup"><span data-stu-id="38b7b-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="38b7b-140">Klikk **Fyll ut tabell for spesifikt produkt** for å kjøre jobben.</span><span class="sxs-lookup"><span data-stu-id="38b7b-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="38b7b-141">Denne jobben må bare kjøres én gang.</span><span class="sxs-lookup"><span data-stu-id="38b7b-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="38b7b-142">Pass på at den obligatoriske **ValueMap** for salg av **målenheten** i Finance and Operations finnes i **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span><span class="sxs-lookup"><span data-stu-id="38b7b-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="38b7b-143">Oppdater **ID-en for CDS-organisasjonen Organization_OrganizationId** i **Source -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="38b7b-143">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="38b7b-144">Malverdien er ORG001 som standard.</span><span class="sxs-lookup"><span data-stu-id="38b7b-144">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="38b7b-145">Oppdater **ValueMap** for **enhetsgruppen** (**defaultuomscheduleid.name**) i **CDS -\> Destination** til å samsvare med **enhetsgruppene** i Sales.</span><span class="sxs-lookup"><span data-stu-id="38b7b-145">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="38b7b-146">Malverdien er **Standardenhet** som standard.</span><span class="sxs-lookup"><span data-stu-id="38b7b-146">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="38b7b-147">Kontroller at alle målenheter for produktsalg fra Finance and Operations finnes i Sales, med verdien **CDS-plukklister**.</span><span class="sxs-lookup"><span data-stu-id="38b7b-147">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="38b7b-148">Kontroller at **Prislister** finnes i Sales for hver produktsalgsvaluta i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="38b7b-148">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="38b7b-149">Produkter kan opprettes i Sales med statusen **Utkast** eller **Aktive**.</span><span class="sxs-lookup"><span data-stu-id="38b7b-149">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="38b7b-150">Dette styres i **Systeminnstillinger** under **Salg** i Sales.</span><span class="sxs-lookup"><span data-stu-id="38b7b-150">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="38b7b-151">Produkter som er opprettet med utkaststatus, må aktiveres før de kan legges til i et **tilbud** eller en **salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="38b7b-151">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="38b7b-152">Tilordninge mal i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="38b7b-152">Template mapping in data integrator</span></span>

<span data-ttu-id="38b7b-153">Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.</span><span class="sxs-lookup"><span data-stu-id="38b7b-153">The following illustrations show an example of a template mapping in data integrator.</span></span>

![tilordne mal i dataintegrator](./media/products-template-mapping-data-integrator-1.png)

![tilordne mal for produkter i dataintegrator](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="38b7b-156">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="38b7b-156">Related topics</span></span>

[<span data-ttu-id="38b7b-157">Synkronisere kontoer fra Sales til kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="38b7b-157">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="38b7b-158">Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="38b7b-158">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="38b7b-159">Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="38b7b-159">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="38b7b-160">Synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="38b7b-160">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="38b7b-161">Synkronisere salgsfakturahoder og -linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="38b7b-161">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


