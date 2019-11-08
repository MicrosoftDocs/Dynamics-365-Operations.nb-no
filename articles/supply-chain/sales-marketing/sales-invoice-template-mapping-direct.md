---
title: Synkronisere salgsfakturahoder og -linjer direkte fra Supply Chain Management til Sales
description: Dette emnet beskriver maler og underliggende oppgaver som brukes til å synkronisere salgsfakturahoder og -linjer direkte fra Dynamics 365 Supply Chain Management til Dynamics 365 Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.openlocfilehash: fa2772db63332319c399999bd5f747b2ac729d9e
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653281"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="c7fc6-103">Synkronisere salgsfakturahoder og -linjer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="c7fc6-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7fc6-104">Dette emnet beskriver maler og underliggende oppgaver som brukes til å synkronisere salgsfakturahoder og -linjer direkte fra Dynamics 365 Supply Chain Management til Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="c7fc6-105">Dataflyt i Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="c7fc6-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="c7fc6-106">Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="c7fc6-107">Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data om kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="c7fc6-108">Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="c7fc6-109">[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="c7fc6-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c7fc6-110">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="c7fc6-110">Templates and tasks</span></span>

<span data-ttu-id="c7fc6-111">Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="c7fc6-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="c7fc6-112">Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c7fc6-113">Følgende mal og underliggende oppgavene brukes til å synkronisere salgsfakturahoder og -linjer fra Supply Chain Management til Sales:</span><span class="sxs-lookup"><span data-stu-id="c7fc6-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Supply Chain Management to Sales:</span></span>

- <span data-ttu-id="c7fc6-114">**Navnet på malen i Dataintegrering:** Salgsfakturaer (Fin and Ops til Sales) – direkte</span><span class="sxs-lookup"><span data-stu-id="c7fc6-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="c7fc6-115">**Navnet på oppgaven i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="c7fc6-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="c7fc6-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="c7fc6-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="c7fc6-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="c7fc6-117">SalesInvoiceLine</span></span>

<span data-ttu-id="c7fc6-118">Følgende synkroniseringsoppgaver er påkrevd før synkronisering av salgsfakturahoder og -linjer kan inntreffe:</span><span class="sxs-lookup"><span data-stu-id="c7fc6-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="c7fc6-119">Produkter (Supply Chain Management til Sales) – direkte</span><span class="sxs-lookup"><span data-stu-id="c7fc6-119">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="c7fc6-120">Kontoer (Sales til Supply Chain Management) – direkte (hvis brukt)</span><span class="sxs-lookup"><span data-stu-id="c7fc6-120">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="c7fc6-121">Kontakter (Sales til Supply Chain Management) – direkte (hvis brukt)</span><span class="sxs-lookup"><span data-stu-id="c7fc6-121">Contacts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="c7fc6-122">Salgsordrehoder og -linjer (Supply Chain Management til Sales) – direkte</span><span class="sxs-lookup"><span data-stu-id="c7fc6-122">Sales order header and lines (Supply Chain Management to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="c7fc6-123">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="c7fc6-123">Entity set</span></span>

| <span data-ttu-id="c7fc6-124">Forsyningskjedeadministrasjon</span><span class="sxs-lookup"><span data-stu-id="c7fc6-124">Supply Chain Management</span></span>                              | <span data-ttu-id="c7fc6-125">Salg</span><span class="sxs-lookup"><span data-stu-id="c7fc6-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="c7fc6-126">Eksternt vedlikeholdte hoder for kundesalgsfaktura</span><span class="sxs-lookup"><span data-stu-id="c7fc6-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="c7fc6-127">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="c7fc6-127">Invoices</span></span>       |
| <span data-ttu-id="c7fc6-128">Eksternt vedlikeholdte linjer for kundesalgsfaktura</span><span class="sxs-lookup"><span data-stu-id="c7fc6-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="c7fc6-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="c7fc6-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="c7fc6-130">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="c7fc6-130">Entity flow</span></span>

<span data-ttu-id="c7fc6-131">Salgsfakturaer er opprettet i Supply Chain Management og synkronisert til Sales.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-131">Sales invoices are created in Supply Chain Management and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="c7fc6-132">Skatt knyttet til kostnader på salgsfakturahodet er for øyeblikket ikke inkludert i synkronisering fra Supply Chain Management til Sales.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Supply Chain Managements to Sales.</span></span> <span data-ttu-id="c7fc6-133">Sales støtter ikke skatteinformasjon på hodenivå.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="c7fc6-134">Mva som er knyttet til tillegg på linjenivå er imidlertid inkludert i synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c7fc6-135">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="c7fc6-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="c7fc6-136">Et **Fakturanummer**-felt er lagt til **Faktura**-enheten og vises på siden.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="c7fc6-137">Knappen **Opprett faktura** på siden **Salgsordre** er skjult fordi fakturaer vil opprettes i Supply Chain Management og synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="c7fc6-138">Siden **Faktura** kan ikke redigeres fordi fakturaer vil synkroniseres fra Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-138">The **Invoice** page can't be edited, because invoices will be synchronized from Supply Chain Management.</span></span>
- <span data-ttu-id="c7fc6-139">**Salgsordrestatus**-verdien endres automatisk til **Fakturert** når relaterte fakturaer fra Supply Chain Management er synkronisert til Sales.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synchronized to Sales.</span></span> <span data-ttu-id="c7fc6-140">Eieren av salgsordren som fakturaen ble opprettet fra, tildeles også som eier av fakturaen.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="c7fc6-141">Eieren av salgsordren kan derfor vise fakturaen.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="c7fc6-142">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="c7fc6-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="c7fc6-143">Før du synkroniserer salgsfakturaer, er det viktig å oppdatere innstillingene nedenfor i systemene.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="c7fc6-144">Oppsett i salg</span><span class="sxs-lookup"><span data-stu-id="c7fc6-144">Setup in Sales</span></span>

<span data-ttu-id="c7fc6-145">Gå til **Innstillinger** > **Administrasjon** > **Systeminnstillinger** > **Salg**, og sørger for å bruke følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="c7fc6-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="c7fc6-146">Alternativet **Bruk systemets priskalkuleringssystem** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="c7fc6-147">Feltet **Rabattkalkuleringsmetode** er satt til **Linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="c7fc6-148">Oppsett i Dataintegrasjonsprosjekt</span><span class="sxs-lookup"><span data-stu-id="c7fc6-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="c7fc6-149">Salgsfakturahode-oppgave</span><span class="sxs-lookup"><span data-stu-id="c7fc6-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="c7fc6-150">Sørg for at nødvendig tilordning finnes for **InvoiceCountryRegionId** til **BillingAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="c7fc6-151">Malverdien er en verditilordning der flere land eller områder er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="c7fc6-152">En prisliste er nødvendig for å opprette fakturaer i Sales.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="c7fc6-153">Oppdater verditilordningen for **pricelevelid.name\[Prislistenavn\]** til prislisten som brukes i Sales per valuta.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="c7fc6-154">Du kan bruke standard prisliste for en enkelt valuta.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="c7fc6-155">Hvis du har prislister i flere valutaer, kan du også bruke en verditilordning.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="c7fc6-156">Malverdien for **pricelevelid.name \[Prislistenavn\]** er en verditilordning som er basert på valuta med USD = CRM Service USA (prøve).</span><span class="sxs-lookup"><span data-stu-id="c7fc6-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="c7fc6-157">SalesInvoiceLine-oppgave</span><span class="sxs-lookup"><span data-stu-id="c7fc6-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="c7fc6-158">Sørg for at nødvendig tilordning finnes for **måleenhet**.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="c7fc6-159">Kontroller at den nødvendige verditilordningen finnes for **SalesUnitSymbol** i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-159">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>

    <span data-ttu-id="c7fc6-160">En malverdi som har en verditilordning er definert for **SalesUnitSymbol** til **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c7fc6-161">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="c7fc6-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="c7fc6-162">Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke inkludert i standardtilordningene.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="c7fc6-163">Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="c7fc6-164">Følgende illustrasjoner viser et eksempel på en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="c7fc6-165">Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-165">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="c7fc6-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="c7fc6-166">SalesInvoiceHeader</span></span>

![Maltilordning i Dataintegrering](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="c7fc6-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="c7fc6-168">SalesInvoiceLine</span></span>

![Maltilordning i Dataintegrering](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="c7fc6-170">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="c7fc6-170">Related topics</span></span>

[<span data-ttu-id="c7fc6-171">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="c7fc6-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="c7fc6-172">Synkronisere kontoer direkte fra Sales til kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c7fc6-172">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="c7fc6-173">Synkronisere produkter direkte fra Supply Chain Management til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="c7fc6-173">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="c7fc6-174">Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c7fc6-174">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="c7fc6-175">Synkronisere salgsordrehoder og -linjer direkte fra Supply Chain Management til Sales</span><span class="sxs-lookup"><span data-stu-id="c7fc6-175">Synchronize sales order headers and lines directly from Supply Chain Management to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)
