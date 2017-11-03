---
title: Synkronisere salgsfakturahoder og -linjer fra Finance and Operations til Sales
description: "Emnet diskuterer maler og underliggende oppgaver som brukes til å synkronisere salgsfakturahoder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales."
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
ms.openlocfilehash: 22ab02555dcac850b18aac9564af41d6c627eade
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="f4b0b-103">Synkronisere salgsfakturahoder og -linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="f4b0b-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f4b0b-104">Emnet diskuterer maler og underliggende oppgaver som brukes til å synkronisere salgsfakturahoder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="f4b0b-105">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="f4b0b-105">Templates and tasks</span></span>

<span data-ttu-id="f4b0b-106">Følgende maler og underliggende oppgaver brukes til å synkronisere salgsfakturahoder og -linjer fra Finance and Operations til Sales:</span><span class="sxs-lookup"><span data-stu-id="f4b0b-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="f4b0b-107">**Navnet på malen i Dataintegrasjon**</span><span class="sxs-lookup"><span data-stu-id="f4b0b-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="f4b0b-108">Salgsfaktura (Fin and Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="f4b0b-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="f4b0b-109">**Navnet på oppgaven i Dataintegrasjonprosjektet**</span><span class="sxs-lookup"><span data-stu-id="f4b0b-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="f4b0b-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="f4b0b-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="f4b0b-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="f4b0b-111">SalesInvoiceLine</span></span>

<span data-ttu-id="f4b0b-112">Synkroniseringsoppgaver som kreves før Salgsfakturaoverskrift og linjesynkronisering:</span><span class="sxs-lookup"><span data-stu-id="f4b0b-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="f4b0b-113">Produkter (Fin and Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="f4b0b-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="f4b0b-114">Kontoer (Sales til Fin and Ops) (hvis brukt)</span><span class="sxs-lookup"><span data-stu-id="f4b0b-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="f4b0b-115">Kontakter (Sales til Fin and Ops) (hvis brukt)</span><span class="sxs-lookup"><span data-stu-id="f4b0b-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="f4b0b-116">Salgsordrehoder og -linjer (Fin and Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="f4b0b-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="f4b0b-117">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="f4b0b-117">Entity set</span></span>

| <span data-ttu-id="f4b0b-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f4b0b-118">Finance and Operations</span></span>                               | <span data-ttu-id="f4b0b-119">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="f4b0b-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="f4b0b-120">Salg</span><span class="sxs-lookup"><span data-stu-id="f4b0b-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="f4b0b-121">Eksternt vedlikeholdte hoder for kundesalgsfaktura</span><span class="sxs-lookup"><span data-stu-id="f4b0b-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="f4b0b-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="f4b0b-122">SalesInvoice</span></span>     | <span data-ttu-id="f4b0b-123">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="f4b0b-123">Invoices</span></span>       |
| <span data-ttu-id="f4b0b-124">Eksternt vedlikeholdte linjer for kundesalgsfaktura</span><span class="sxs-lookup"><span data-stu-id="f4b0b-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="f4b0b-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="f4b0b-125">SalesInvoiceLine</span></span> | <span data-ttu-id="f4b0b-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="f4b0b-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="f4b0b-127">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="f4b0b-127">Entity flow</span></span>

<span data-ttu-id="f4b0b-128">Salgsfakturaer er opprettet i Finance and Operations og synkronisert til Sales.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="f4b0b-129">Skatt knyttet til avgifter på **Salgsfakturahode** er for øyeblikket ikke inkludert i synkronisering fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="f4b0b-130">Dette er fordi Sales ikke støtter skatteinformasjon på hodenivå.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="f4b0b-131">Skatterelaterte kostander på linjenivå inkluderes.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="f4b0b-132">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="f4b0b-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="f4b0b-133">Et **Fakturanummerfelt** er lagt til **Faktura**-enheten og vises på siden.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="f4b0b-134">Knappen **Opprett faktura** på siden **Salgsordre** er skjult fordi fakturaer vil opprettes i Finance and Operations og synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="f4b0b-135">Siden **Faktura** kan ikke redigeres fordi fakturaer vil synkroniseres fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="f4b0b-136">**Salgsordrestatus** endres automatisk til **Fakturert** når relaterte fakturaer fra Finance and Operations er synkronisert til Sales.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="f4b0b-137">Også eieren av salgsordren fra hvilken fakturaen ble opprettet, er tildelt som eier av fakturaen.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="f4b0b-138">Dette gir eieren av salgsordren muligheten til å se fakturaen.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="f4b0b-139">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="f4b0b-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="f4b0b-140">Før du synkroniserer salgsfakturaer, er det viktig å oppdatere systemene med følgende innstilling:</span><span class="sxs-lookup"><span data-stu-id="f4b0b-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="f4b0b-141">Oppsett i Sales</span><span class="sxs-lookup"><span data-stu-id="f4b0b-141">Setup in Sales</span></span>

- <span data-ttu-id="f4b0b-142">Under **Oppsett** > **Administrasjon** > **Systeminnstillinger** > **Sales**, må du forsikre deg om at **Bruk systemets priskalkuleringssystem** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="f4b0b-143">Under **Oppsett** > **Administrasjon** > **Systeminnstillinger** > **Sales**, må du forsikre deg om at **Rabattkalkuleringsmetode** er satt til **Linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="f4b0b-144">Oppsett i Dataintegrasjonsprosjekt</span><span class="sxs-lookup"><span data-stu-id="f4b0b-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="f4b0b-145">Salgsfakturahode-oppgave</span><span class="sxs-lookup"><span data-stu-id="f4b0b-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="f4b0b-146">Oppdater tilordning for **CDS-organisasjons-ID** i **Kilde** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="f4b0b-147">Standard malverdi for **Salgsordre_Organisasjon_Organisasjons-ID** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="f4b0b-148">Standard malverdi for **Konto_Organisasjon_Organisasjons-ID** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="f4b0b-149">Standard malverdi for **Organisasjon_Organisasjons-ID** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="f4b0b-150">Forsikre deg om at nødvendig tilordning eksisterer i **Kilde** > **CDS for InvoiceCountryRegionId** til **BillingAdress_Country**.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="f4b0b-151">Malverdi er **ValueMap** med et antall av land tilordnet.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="f4b0b-152">**Prisliste** er nødvendig for å opprette fakturaer i Sales.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="f4b0b-153">Oppdater **ValueMap** i **CDS** > **-destinasjon for pricelevelid.name (Prislistenavn)** til **Prisliste** som brukes i Sales per valuta.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="f4b0b-154">Du kan enten bruke standard **Prisliste** for enkeltvaluta eller bruke **ValueMap** hvis du har **Prisliste** i flere valutaer.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="f4b0b-155">Malverdi for **pricelevelid.name (Prislistenavn)** er **ValueMap** basert på **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="f4b0b-156">usd: CRM-service USA (prøve)</span><span class="sxs-lookup"><span data-stu-id="f4b0b-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="f4b0b-157">SalesInvoiceLine-oppgave</span><span class="sxs-lookup"><span data-stu-id="f4b0b-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="f4b0b-158">Forsikre deg om at nødvendig tilordning eksisterer i **Kilde** > **CDS for måleenhet**.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="f4b0b-159">Forsikre deg om at nødvendig **ValueMap** for **SalesUnitSymbol** i Finance and Operations eksisterer i **Kilde** > **CDS-tilordning**.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="f4b0b-160">Malverdi med **ValueMap** er definert for **SalesUnitSymbol til Quanitiy_UOM**.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="f4b0b-161">Oppdater tilordning for **CDS-organisasjons-ID i Kilde** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="f4b0b-162">Standard malverdi for **Salgsfaktura_Organisasjon_Organisasjons-ID** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="f4b0b-163">Standard malverdi for **Produkt_Organisasjon_Organisasjons-ID** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="f4b0b-164">Maltilordning i Dataintegrator</span><span class="sxs-lookup"><span data-stu-id="f4b0b-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="f4b0b-165">**Betalingsbetingelser**, **Fraktbetingelser**, **Leveringsbetingelser**, **Forsendelsesmetode**, og **Leveringsmetode** er ikke en del av standard tilordning.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="f4b0b-166">Tilordning av disse feltene krever at verditilordning settes opp, noe som er spesifikt for dataene i organisasjonene mellom hvilke enheten som synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="f4b0b-167">Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.</span><span class="sxs-lookup"><span data-stu-id="f4b0b-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Tilordninge mal i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Tilordninge mal i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Tilordninge mal i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Tilordninge mal i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="f4b0b-172">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="f4b0b-172">Related topics</span></span>

[<span data-ttu-id="f4b0b-173">Synkronisere produkter fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="f4b0b-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="f4b0b-174">Synkronisere kontoer fra Sales til kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f4b0b-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="f4b0b-175">Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f4b0b-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="f4b0b-176">Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f4b0b-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="f4b0b-177">Synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="f4b0b-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


