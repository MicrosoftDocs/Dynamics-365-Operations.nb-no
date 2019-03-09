---
title: Synkronisere produkter direkte fra Finance and Operations til produkter i Sales
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
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
ms.openlocfilehash: feb9fbc066162e2caa9fc5dbaeec2c063ae23060
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "348256"
---
# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="cdf02-103">Synkronisere produkter direkte fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="cdf02-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="cdf02-104">Før du kan bruke kundeemnet til kontanter løsning må du ha kjennskap til [Integrere data til Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="cdf02-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="cdf02-105">Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere produkter direkte fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="cdf02-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="cdf02-106">Dataflyt i Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="cdf02-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="cdf02-107">Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="cdf02-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="cdf02-108">Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data om kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="cdf02-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="cdf02-109">Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="cdf02-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="cdf02-110">[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="cdf02-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cdf02-111">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="cdf02-111">Templates and tasks</span></span>

<span data-ttu-id="cdf02-112">Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="cdf02-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="cdf02-113">Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.</span><span class="sxs-lookup"><span data-stu-id="cdf02-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="cdf02-114">Følgende mal og underliggende oppgavene brukes til å synkronisere produkter fra til Finance and Operations til sales.</span><span class="sxs-lookup"><span data-stu-id="cdf02-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="cdf02-115">**Navnet på malen i Dataintegrering:** Produkter (Fin and Ops til Sales) – direkte</span><span class="sxs-lookup"><span data-stu-id="cdf02-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="cdf02-116">**Navnet på oppgaven i Dataintegrasjonprosjektet**: Produkter</span><span class="sxs-lookup"><span data-stu-id="cdf02-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="cdf02-117">Ingen synkroniseringsoppgaver kreves før produktsynkronisering kan utføres.</span><span class="sxs-lookup"><span data-stu-id="cdf02-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="cdf02-118">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="cdf02-118">Entity set</span></span>

| <span data-ttu-id="cdf02-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cdf02-119">Finance and Operations</span></span>     | <span data-ttu-id="cdf02-120">Salg</span><span class="sxs-lookup"><span data-stu-id="cdf02-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="cdf02-121">Salgbare frigitte produkter</span><span class="sxs-lookup"><span data-stu-id="cdf02-121">Sellable released products</span></span> | <span data-ttu-id="cdf02-122">Produkter</span><span class="sxs-lookup"><span data-stu-id="cdf02-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="cdf02-123">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="cdf02-123">Entity flow</span></span>

<span data-ttu-id="cdf02-124">Produkter administreres i Finance and Operations og synkroniseres med Sales.</span><span class="sxs-lookup"><span data-stu-id="cdf02-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="cdf02-125">Sataenheten **Salgbare frigitte produkter** i Finance and Operations eksporterer bare produkter som er *salgbare*.</span><span class="sxs-lookup"><span data-stu-id="cdf02-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="cdf02-126">salgbare produkter er produkter som inneholder informasjon som kreves for å kunne brukes på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="cdf02-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="cdf02-127">De samme reglene gjelder når et produkt er bekreftet ved å bruke **Valider**-funksjonen på siden **Frigitt produkt**.</span><span class="sxs-lookup"><span data-stu-id="cdf02-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="cdf02-128">Produktnummeret brukes som en nøkkel.</span><span class="sxs-lookup"><span data-stu-id="cdf02-128">The product number is used as a key.</span></span> <span data-ttu-id="cdf02-129">Når produktvarianter synkroniseres til Sales, har hver produktvariant én enkelt produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="cdf02-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="cdf02-130">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="cdf02-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="cdf02-131">I Sales legges det til et nytt **Vedlikeholdes eksternt**-felt på produktene for å angi at et bestemt produkt vedlikeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="cdf02-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="cdf02-132">Verdien er satt til **Ja** som standard under import til Sales.</span><span class="sxs-lookup"><span data-stu-id="cdf02-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="cdf02-133">Følgende verdier er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="cdf02-133">The following values are available:</span></span>

- <span data-ttu-id="cdf02-134">**Ja** – Produktet kommer fra Finance and Operations, og kan ikke redigeres i Sales.</span><span class="sxs-lookup"><span data-stu-id="cdf02-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="cdf02-135">**Nei** – Produktet ble lagt inn direkte i Sales.</span><span class="sxs-lookup"><span data-stu-id="cdf02-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="cdf02-136">**(Tom)** – Produktet fantes i Sales før løsningen Kundeemne til kontanter ble aktivert.</span><span class="sxs-lookup"><span data-stu-id="cdf02-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="cdf02-137">Informasjonen i feltet **Vedlikeholdes eksternt** brukes til å garantere at bare tilbud og salgsordrer med eksternt vedlikeholdte produkter synkroniseres til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cdf02-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="cdf02-138">Eksternt vedlikeholdte produkter legges automatisk til den første gyldige prislisten med samme valuta.</span><span class="sxs-lookup"><span data-stu-id="cdf02-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="cdf02-139">Prislister er ordnet alfabetisk etter navn.</span><span class="sxs-lookup"><span data-stu-id="cdf02-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="cdf02-140">Produktets salgspris fra Finance and Operations brukes som prisen på prislisten.</span><span class="sxs-lookup"><span data-stu-id="cdf02-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="cdf02-141">Derfor må det være en prisliste i Sales for alle produktsalgsvaluta i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cdf02-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="cdf02-142">Valutaen på frigitte salgbare produkter er satt til regnskapsvalutaen i den juridiske enheten som produktet er eksportert fra.</span><span class="sxs-lookup"><span data-stu-id="cdf02-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="cdf02-143">Produktsynkronisering lykkes ikke hvis det ikke er en prisliste som har en tilhørende valuta.</span><span class="sxs-lookup"><span data-stu-id="cdf02-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="cdf02-144">Du kan kontrollere den brukte prislisten med integreringen ved å tilordne pricelevelid.name [standard prisliste (navn)] i dataintegrasjonsprosjektet.</span><span class="sxs-lookup"><span data-stu-id="cdf02-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="cdf02-145">Inndataene må være med bare små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="cdf02-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="cdf02-146">Standardverdien for en prisliste i Sales med navnet Standard, er for eksempel: Målfelt: pricelevelid.name [standard prisliste (navn)] og tilordningstype: [ { "transformType": "Standard", "defaultValue": "standard" } ].</span><span class="sxs-lookup"><span data-stu-id="cdf02-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="cdf02-147">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="cdf02-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="cdf02-148">Før du kjører synkroniseringen for første gang, må du fylle ut den spesifikke produkttabellen for eksisterende produkter i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cdf02-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="cdf02-149">Eksisterende produkter vil ikke bli synkronisert før denne jobben er fullført.</span><span class="sxs-lookup"><span data-stu-id="cdf02-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="cdf02-150">I Finance and Operations kan du bruke Søk til å søke etter **Fyll ut tabell for spesifikt produkt**.</span><span class="sxs-lookup"><span data-stu-id="cdf02-150">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="cdf02-151">Velg **Fyll ut tabell for spesifikt produkt** for å kjøre jobben.</span><span class="sxs-lookup"><span data-stu-id="cdf02-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="cdf02-152">Jobben må kjøres bare én gang.</span><span class="sxs-lookup"><span data-stu-id="cdf02-152">This job must be run only one time.</span></span>

- <span data-ttu-id="cdf02-153">Pass på at den nødvendige verditilordningen for selgende måleenheten mellom Finance and Operations og Sales finnes i tilordnignen for **SalesUnitSymbol** til **DefaultUnit (Name)**.</span><span class="sxs-lookup"><span data-stu-id="cdf02-153">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="cdf02-154">Oppdater verditilordningen for **enhetsgruppen** (**defaultuomscheduleid.name**), slik at den samsvarer med **enhetsgruppene** i Sales.</span><span class="sxs-lookup"><span data-stu-id="cdf02-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="cdf02-155">Standard malverdi er **Standardenhet**.</span><span class="sxs-lookup"><span data-stu-id="cdf02-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="cdf02-156">Kontroller at målenheter for alle produkter fra Finance and Operations finnes i Sales.</span><span class="sxs-lookup"><span data-stu-id="cdf02-156">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="cdf02-157">Kontroller at prislister finnes i Sales for alle produktsalgsvaluta i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cdf02-157">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="cdf02-158">Når produkter opprettes i Sales, får de statusen **Utkast** eller **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="cdf02-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="cdf02-159">Virkemåten kontrolleres under **Innstillinger** > **Administrasjon** > **Systeminnstillinger** > **Salg** i Sales.</span><span class="sxs-lookup"><span data-stu-id="cdf02-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="cdf02-160">Produkter som har statusen **Utkast** når de opprettes, må aktiveres før de kan legges til i tilbud eller salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="cdf02-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cdf02-161">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="cdf02-161">Template mapping in Data integration</span></span>

<span data-ttu-id="cdf02-162">Illustrasjonen nedenfor viser et eksempel på en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="cdf02-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="cdf02-163">Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cdf02-163">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Maltilordning i Dataintegrator](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="cdf02-165">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="cdf02-165">Related topics</span></span>

[<span data-ttu-id="cdf02-166">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="cdf02-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="cdf02-167">Synkronisere kontoer direkte fra Sales til kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cdf02-167">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="cdf02-168">Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cdf02-168">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="cdf02-169">Synkronisere salgsordrehoder og -linjer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="cdf02-169">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="cdf02-170">Synkronisere salgsfakturahoder og -linjer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="cdf02-170">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)



