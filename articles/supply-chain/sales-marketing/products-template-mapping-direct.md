---
title: Synkronisere produkter direkte fra Supply Chain Management til produkter i Sales
description: Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere produkter fra Dynamics 365 Supply Chain Management til Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: f5e91d4dac8ea6d19fa32abca4e9ff73c7cd4a88
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234999"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="4b51d-103">Synkronisere produkter direkte fra Supply Chain Management til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="4b51d-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="4b51d-104">Før du kan bruke kundeemnet til kontanter løsning må du ha kjennskap til [Integrere data til Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="4b51d-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="4b51d-105">Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere produkter direkte fra Dynamics 365 Supply Chain Management til Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="4b51d-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="4b51d-106">Dataflyt i Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="4b51d-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="4b51d-107">Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="4b51d-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="4b51d-108">Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data om kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="4b51d-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="4b51d-109">Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="4b51d-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="4b51d-110">[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="4b51d-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="4b51d-111">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="4b51d-111">Templates and tasks</span></span>

<span data-ttu-id="4b51d-112">Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for Power Apps](https://admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="4b51d-112">To access the available templates, open [Power Apps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="4b51d-113">Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.</span><span class="sxs-lookup"><span data-stu-id="4b51d-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="4b51d-114">Malen nedenfor og de underliggende oppgavene brukes til å synkronisere produkter fra Supply Chain Management til Sales.</span><span class="sxs-lookup"><span data-stu-id="4b51d-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="4b51d-115">**Navnet på malen i Dataintegrering:** Produkter (Supply Chain Management til Sales) – direkte</span><span class="sxs-lookup"><span data-stu-id="4b51d-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="4b51d-116">**Navnet på oppgaven i Dataintegrasjonprosjektet**: Produkter</span><span class="sxs-lookup"><span data-stu-id="4b51d-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="4b51d-117">Ingen synkroniseringsoppgaver kreves før produktsynkronisering kan utføres.</span><span class="sxs-lookup"><span data-stu-id="4b51d-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="4b51d-118">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="4b51d-118">Entity set</span></span>

| <span data-ttu-id="4b51d-119">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4b51d-119">Supply Chain Management</span></span>    | <span data-ttu-id="4b51d-120">Salg</span><span class="sxs-lookup"><span data-stu-id="4b51d-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="4b51d-121">Salgbare frigitte produkter</span><span class="sxs-lookup"><span data-stu-id="4b51d-121">Sellable released products</span></span> | <span data-ttu-id="4b51d-122">Produkter</span><span class="sxs-lookup"><span data-stu-id="4b51d-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="4b51d-123">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="4b51d-123">Entity flow</span></span>

<span data-ttu-id="4b51d-124">Produkter administreres i Supply Chain Management og synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="4b51d-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="4b51d-125">Sataenheten **Salgbare frigitte produkter** i Supply Chain Management eksporterer bare produkter som er *salgbare*.</span><span class="sxs-lookup"><span data-stu-id="4b51d-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="4b51d-126">salgbare produkter er produkter som inneholder informasjon som kreves for å kunne brukes på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="4b51d-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="4b51d-127">De samme reglene gjelder når et produkt er bekreftet ved å bruke **Valider**-funksjonen på siden **Frigitt produkt**.</span><span class="sxs-lookup"><span data-stu-id="4b51d-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="4b51d-128">Produktnummeret brukes som en nøkkel.</span><span class="sxs-lookup"><span data-stu-id="4b51d-128">The product number is used as a key.</span></span> <span data-ttu-id="4b51d-129">Når produktvarianter synkroniseres til Sales, har hver produktvariant én enkelt produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="4b51d-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="4b51d-130">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="4b51d-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="4b51d-131">I Sales legges det til et nytt **Vedlikeholdes eksternt**-felt på produktene for å angi at et bestemt produkt vedlikeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="4b51d-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="4b51d-132">Verdien er satt til **Ja** som standard under import til Sales.</span><span class="sxs-lookup"><span data-stu-id="4b51d-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="4b51d-133">Følgende verdier er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="4b51d-133">The following values are available:</span></span>

- <span data-ttu-id="4b51d-134">**Ja** – Produktet kommer fra Supply Chain Management og kan ikke redigeres i Sales.</span><span class="sxs-lookup"><span data-stu-id="4b51d-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="4b51d-135">**Nei** – Produktet ble lagt inn direkte i Sales.</span><span class="sxs-lookup"><span data-stu-id="4b51d-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="4b51d-136">**(Tom)** – Produktet fantes i Sales før løsningen Kundeemne til kontanter ble aktivert.</span><span class="sxs-lookup"><span data-stu-id="4b51d-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="4b51d-137">Informasjonen i feltet **Vedlikeholdes eksternt** brukes til å sikre at bare tilbud og salgsordrer med eksternt vedlikeholdte produkter synkroniseres til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4b51d-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="4b51d-138">Eksternt vedlikeholdte produkter legges automatisk til den første gyldige prislisten med samme valuta.</span><span class="sxs-lookup"><span data-stu-id="4b51d-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="4b51d-139">Prislister er ordnet alfabetisk etter navn.</span><span class="sxs-lookup"><span data-stu-id="4b51d-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="4b51d-140">Produktets salgspris fra Supply Chain Management brukes som prisen på prislisten.</span><span class="sxs-lookup"><span data-stu-id="4b51d-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="4b51d-141">Derfor må det være en prisliste i Sales for alle produktsalgsvaluta i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4b51d-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="4b51d-142">Valutaen på frigitte salgbare produkter er satt til regnskapsvalutaen i den juridiske enheten som produktet er eksportert fra.</span><span class="sxs-lookup"><span data-stu-id="4b51d-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="4b51d-143">Produktsynkronisering lykkes ikke hvis det ikke er en prisliste som har en tilhørende valuta.</span><span class="sxs-lookup"><span data-stu-id="4b51d-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="4b51d-144">Du kan kontrollere den brukte prislisten med integreringen ved å tilordne pricelevelid.name [standard prisliste (navn)] i dataintegrasjonsprosjektet.</span><span class="sxs-lookup"><span data-stu-id="4b51d-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="4b51d-145">Inndataene må være med bare små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="4b51d-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="4b51d-146">Standardverdien for en prisliste i Sales med navnet Standard, er for eksempel: Målfelt: pricelevelid.name [standard prisliste (navn)] og tilordningstype: [ { "transformType": "Standard", "defaultValue": "standard" } ].</span><span class="sxs-lookup"><span data-stu-id="4b51d-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="4b51d-147">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="4b51d-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="4b51d-148">Før du kjører synkroniseringen for første gang, må du fylle ut den spesifikke produkttabellen for eksisterende produkter i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4b51d-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="4b51d-149">Eksisterende produkter vil ikke bli synkronisert før denne jobben er fullført.</span><span class="sxs-lookup"><span data-stu-id="4b51d-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="4b51d-150">I Supply Chain Management kan du bruke Søk til å søke etter **Fyll ut tabell for spesifikt produkt**.</span><span class="sxs-lookup"><span data-stu-id="4b51d-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="4b51d-151">Velg **Fyll ut tabell for spesifikt produkt** for å kjøre jobben.</span><span class="sxs-lookup"><span data-stu-id="4b51d-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="4b51d-152">Jobben må kjøres bare én gang.</span><span class="sxs-lookup"><span data-stu-id="4b51d-152">This job must be run only one time.</span></span>

- <span data-ttu-id="4b51d-153">Pass på at den nødvendige verditilordningen for selgende måleenheten mellom Supply Chain Management og Sales finnes i tilordningen for **SalesUnitSymbol** til **DefaultUnit (Name)**.</span><span class="sxs-lookup"><span data-stu-id="4b51d-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="4b51d-154">Oppdater verditilordningen for **enhetsgruppen** (**defaultuomscheduleid.name**), slik at den samsvarer med **enhetsgruppene** i Sales.</span><span class="sxs-lookup"><span data-stu-id="4b51d-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="4b51d-155">Standard malverdi er **Standardenhet**.</span><span class="sxs-lookup"><span data-stu-id="4b51d-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="4b51d-156">Kontroller at målenheter for alle produkter fra Supply Chain Management finnes i Sales.</span><span class="sxs-lookup"><span data-stu-id="4b51d-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="4b51d-157">Kontroller at prislister finnes i Sales for alle produktsalgsvaluta i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4b51d-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="4b51d-158">Når produkter opprettes i Sales, får de statusen **Utkast** eller **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="4b51d-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="4b51d-159">Virkemåten kontrolleres under **Innstillinger** > **Administrasjon** > **Systeminnstillinger** > **Salg** i Sales.</span><span class="sxs-lookup"><span data-stu-id="4b51d-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="4b51d-160">Produkter som har statusen **Utkast** når de opprettes, må aktiveres før de kan legges til i tilbud eller salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="4b51d-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4b51d-161">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="4b51d-161">Template mapping in Data integration</span></span>

<span data-ttu-id="4b51d-162">Illustrasjonen nedenfor viser et eksempel på en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="4b51d-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="4b51d-163">Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4b51d-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Maltilordning i Dataintegrator](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="4b51d-165">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="4b51d-165">Related topics</span></span>

[<span data-ttu-id="4b51d-166">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="4b51d-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="4b51d-167">Synkronisere kontoer direkte fra Sales til kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4b51d-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="4b51d-168">Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4b51d-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="4b51d-169">Synkronisering av salgsordrer direkte mellom Sales og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4b51d-169">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="4b51d-170">Synkronisere salgsfakturahoder og -linjer direkte fra Supply Chain Management til Sales</span><span class="sxs-lookup"><span data-stu-id="4b51d-170">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]