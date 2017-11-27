---
title: Synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales
description: "Emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere salgsordrehoder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="a48ec-103">Synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="a48ec-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a48ec-104">Emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere salgsordrehoder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="a48ec-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="a48ec-105">Mal og oppgaver</span><span class="sxs-lookup"><span data-stu-id="a48ec-105">Template and tasks</span></span>

<span data-ttu-id="a48ec-106">Følgende maler og underliggende oppgaver brukes til å synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales:</span><span class="sxs-lookup"><span data-stu-id="a48ec-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="a48ec-107">**Navn på mal i Dataintegrasjon**</span><span class="sxs-lookup"><span data-stu-id="a48ec-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="a48ec-108">Salgsordrer (Fin and Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="a48ec-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="a48ec-109">**Navn på oppgaver i Dataintegrasjonprosjektet**</span><span class="sxs-lookup"><span data-stu-id="a48ec-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="a48ec-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="a48ec-110">OrderHeader</span></span>
    - <span data-ttu-id="a48ec-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="a48ec-111">OrderLine</span></span>

<span data-ttu-id="a48ec-112">Synkroniseringsoppgaver som kreves før Salgsfakturaoverskrift og linjesynk:</span><span class="sxs-lookup"><span data-stu-id="a48ec-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="a48ec-113">Produkter (Fin and Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="a48ec-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="a48ec-114">Kontoer (Sales til Fin and Ops) (hvis brukt)</span><span class="sxs-lookup"><span data-stu-id="a48ec-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="a48ec-115">Kontakter til Kunder (Sales til Fin and Ops) (hvis brukt)</span><span class="sxs-lookup"><span data-stu-id="a48ec-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="a48ec-116">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="a48ec-116">Entity set</span></span>

| <span data-ttu-id="a48ec-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a48ec-117">Finance and Operations</span></span> |    <span data-ttu-id="a48ec-118">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="a48ec-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="a48ec-119">Salg</span><span class="sxs-lookup"><span data-stu-id="a48ec-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="a48ec-120">CDS-salgsordrehoder</span><span class="sxs-lookup"><span data-stu-id="a48ec-120">CDS sales order headers</span></span>| <span data-ttu-id="a48ec-121">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="a48ec-121">SalesOrder</span></span>     | <span data-ttu-id="a48ec-122">Salgsordrer</span><span class="sxs-lookup"><span data-stu-id="a48ec-122">SalesOrders</span></span> |
| <span data-ttu-id="a48ec-123">CDS-salgsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="a48ec-123">CDS sales order lines</span></span>  | <span data-ttu-id="a48ec-124">Salgsordrelinje</span><span class="sxs-lookup"><span data-stu-id="a48ec-124">SalesOrderLine</span></span> | <span data-ttu-id="a48ec-125">Salgsordredetaljer</span><span class="sxs-lookup"><span data-stu-id="a48ec-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="a48ec-126">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="a48ec-126">Entity flow</span></span>

<span data-ttu-id="a48ec-127">Salgsordrer er opprettet i Finance and Operations og synkronisert til Sales.</span><span class="sxs-lookup"><span data-stu-id="a48ec-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="a48ec-128">Filtre i malen sikrer at kun relevante salgsordrer er inkludert i synkroniseringen:</span><span class="sxs-lookup"><span data-stu-id="a48ec-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="a48ec-129">Både bestilling og fakturering av kunde på salgsordren som kommer fra Sales vil inkluderes i synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="a48ec-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="a48ec-130">I Finance and Operations er feltene **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** brukt til å spore synkroniseringen i dataenhetene.</span><span class="sxs-lookup"><span data-stu-id="a48ec-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="a48ec-131">**Salgsordrene** i Finance and Operations må bekreftes.</span><span class="sxs-lookup"><span data-stu-id="a48ec-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="a48ec-132">Kun de bekreftede salgsordrene eller salgsordrene med høyere behandlingsstatus, for eksempel, Levering eller Fakturering, synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="a48ec-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="a48ec-133">Etter at du har opprettet eller endret en salgsordre, må batchjobben **Kalkuler salgstotaler** i Finance and Operations utføres.</span><span class="sxs-lookup"><span data-stu-id="a48ec-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="a48ec-134">Bare salgsordrene med salgstallene beregnet, blir synkronisert til CDS og Salg.</span><span class="sxs-lookup"><span data-stu-id="a48ec-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="a48ec-135">Skatt knyttet til kostnader på **Salgsordrehode** er for øyeblikket ikke inkludert i synkronisering fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="a48ec-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="a48ec-136">Dette er fordi Sales ikke støtter skatteinformasjon på hodenivå.</span><span class="sxs-lookup"><span data-stu-id="a48ec-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="a48ec-137">Skatterelaterte kostander på linjenivå inkluderes.</span><span class="sxs-lookup"><span data-stu-id="a48ec-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="a48ec-138">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="a48ec-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="a48ec-139">Nye felt er lagt til enheten **Ordre** og vises på siden:</span><span class="sxs-lookup"><span data-stu-id="a48ec-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="a48ec-140">**Er behandlet eksternt** – satt til **Ja** når ordren kommer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a48ec-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="a48ec-141">**Behandlingsstatus** – brukes for å vises behandlingsstatus for en ordre i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a48ec-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="a48ec-142">Verdier er:</span><span class="sxs-lookup"><span data-stu-id="a48ec-142">Values are:</span></span>

    - <span data-ttu-id="a48ec-143">Aktivt</span><span class="sxs-lookup"><span data-stu-id="a48ec-143">Active</span></span>
    - <span data-ttu-id="a48ec-144">Bekreftet</span><span class="sxs-lookup"><span data-stu-id="a48ec-144">Confirmed</span></span>
    - <span data-ttu-id="a48ec-145">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="a48ec-145">Packing Slip</span></span>
    - <span data-ttu-id="a48ec-146">Fakturert</span><span class="sxs-lookup"><span data-stu-id="a48ec-146">Invoiced</span></span>
    - <span data-ttu-id="a48ec-147">Plukket</span><span class="sxs-lookup"><span data-stu-id="a48ec-147">Picked</span></span>
    - <span data-ttu-id="a48ec-148">Delvis plukket</span><span class="sxs-lookup"><span data-stu-id="a48ec-148">Partially Picked</span></span>
    - <span data-ttu-id="a48ec-149">Delvis pakket</span><span class="sxs-lookup"><span data-stu-id="a48ec-149">Partially Packed</span></span>
    - <span data-ttu-id="a48ec-150">Sendt</span><span class="sxs-lookup"><span data-stu-id="a48ec-150">Shipped</span></span>
    - <span data-ttu-id="a48ec-151">Delvis sendt</span><span class="sxs-lookup"><span data-stu-id="a48ec-151">Partially Shipped</span></span>
    - <span data-ttu-id="a48ec-152">Delvis fakturert</span><span class="sxs-lookup"><span data-stu-id="a48ec-152">Partially Invoiced</span></span>
    - <span data-ttu-id="a48ec-153">Avbrutt</span><span class="sxs-lookup"><span data-stu-id="a48ec-153">Cancelled</span></span>

<span data-ttu-id="a48ec-154">Innstillingen **Har eksternt behandlede produkter** brukes i andre salgsordrescenarier (fra Sales til Finance and Operation-synkronisering) for å holde oversikt over om salgsordren helt og holdent består av **eksternt behandlede produkter**, i hvilket tilfelle produkter er vedlikeholdt i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a48ec-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="a48ec-155">Dette sikrer at du ikke prøver å synkronisere salgsordrelinjer for produkter som er ukjent for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a48ec-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="a48ec-156">Knappene **Opprett faktura**, **Avbryt ordre**, **Rekalkuler**, **Få produkter** og **Søk opp adresser** på siden **Salgsordre** er skjult for eksternt behandlede ordrer fordi fakturaer vil opprettes i Finance and Operations og synkronisert til Sales.</span><span class="sxs-lookup"><span data-stu-id="a48ec-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="a48ec-157">Ordresiden er ikke redigerbar fordi salgsordreinformasjon vil synkroniseres fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a48ec-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="a48ec-158">**Salgsordrestatus** vil fortsatt være aktiv for å sikre at endringer fra Finance and Operations kan flyte fra **Salgsordre** i Sales.</span><span class="sxs-lookup"><span data-stu-id="a48ec-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="a48ec-159">Dette kontrolleres ved å sette standard **Statuskode [Status]** til **Aktiv** i Dataintegrasjonsprosjektet.</span><span class="sxs-lookup"><span data-stu-id="a48ec-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="a48ec-160">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="a48ec-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="a48ec-161">Før synkronisering av salgsordre er det viktig å oppdatere systemet med følgende innstilling.</span><span class="sxs-lookup"><span data-stu-id="a48ec-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="a48ec-162">Oppsett i Sales</span><span class="sxs-lookup"><span data-stu-id="a48ec-162">Setup in Sales</span></span>

- <span data-ttu-id="a48ec-163">Sikre tillatelser for temaet som brukeren (fra Sales **tilkoblingssett**) er tildelt til.</span><span class="sxs-lookup"><span data-stu-id="a48ec-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="a48ec-164">Hvis du bruker demodata, har brukeren vanligvis administratortilgang, men ikke teamet.</span><span class="sxs-lookup"><span data-stu-id="a48ec-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="a48ec-165">Uten dette vil du få en feil som Hovedteamet mangler når du kjører prosjektet fra Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="a48ec-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="a48ec-166">Under **Innstillinger** > **Sikkerhet** > **Team**, velg relevant team. Klikk **Administrer roller** og velg en rolle med ønskede tillatelser, for eksempel Systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="a48ec-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="a48ec-167">Under **Oppsett** > **Administrasjon** > **Systeminnstillinger** > **Sales**, må du forsikre deg om at **Bruk systemets priskalkuleringssystem** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a48ec-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="a48ec-168">Under **Oppsett** > **Administrasjon** > **Systeminnstillinger** > **Sales**, må du forsikre deg om at **Rabattkalkuleringsmetode** er satt til **Linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="a48ec-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="a48ec-169">Oppsett i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a48ec-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="a48ec-170">Sett **Salg og markedsføring** > **Periodiske oppgaver** > **Kalkuler salgstotaler** for å kjøre en batchjobb, med **Kalkuler totaler for salgsordrer** satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a48ec-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="a48ec-171">Dette er viktig fordi kun salgsordre med kalkulerte totale salg vil synkroniseres til CDS og Sales.</span><span class="sxs-lookup"><span data-stu-id="a48ec-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="a48ec-172">Hyppigheten av batchjobben skal være justert med hyppigheten av salgsordensynkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="a48ec-172">The frequency of the batch job should be alligned with the frequency of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="a48ec-173">Oppsett i Dataintegrasjonsprosjekt</span><span class="sxs-lookup"><span data-stu-id="a48ec-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="a48ec-174">Salgshode-oppgave</span><span class="sxs-lookup"><span data-stu-id="a48ec-174">SalesHeader task</span></span>

- <span data-ttu-id="a48ec-175">Oppdater tilordning for **CDS-organisasjons-ID i Kilde** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="a48ec-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="a48ec-176">Standard malverdi for **Konto_Organisasjon_Organisasjons-ID** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="a48ec-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="a48ec-177">Standard malverdi for **InvoiceAccount_Organization_OrganizationID** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="a48ec-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="a48ec-178">Standard malverdi for **Organisasjon_Organisasjons-ID** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="a48ec-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="a48ec-179">Sørg for at nødvendig tilordning eksister i **Kilde** > **CDS for InvoiceCountryRegionId til BillingAdress_Country** og for **DeliveryCountryRegionID til DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="a48ec-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="a48ec-180">Malverdi er **ValueMap** med et antall av land tilordnet.</span><span class="sxs-lookup"><span data-stu-id="a48ec-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="a48ec-181">**Prisliste** er nødvendig for å opprette ordrer i Sales.</span><span class="sxs-lookup"><span data-stu-id="a48ec-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="a48ec-182">Oppdater **ValueMap** i **CDS** > **Destinasjon** for **pricelevelid.name [Navn på prisliste]** til **Prisliste** brukt i Sales per valuta.</span><span class="sxs-lookup"><span data-stu-id="a48ec-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="a48ec-183">Du kan bruke enten standard **Prisliste** for enkeltvaluta eller bruke **ValueMap** hvis du har **Prisliste** i flere valutaer.</span><span class="sxs-lookup"><span data-stu-id="a48ec-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="a48ec-184">Standard malverdi for **pricelevelid.name (Prislistenavn)** er CRM Service USA (prøve).</span><span class="sxs-lookup"><span data-stu-id="a48ec-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="a48ec-185">Salgslinje-oppgave</span><span class="sxs-lookup"><span data-stu-id="a48ec-185">SalesLine task</span></span>

- <span data-ttu-id="a48ec-186">Oppdater tilordning for **CDS-organisasjons-ID i Kilde** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="a48ec-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="a48ec-187">Standard malverdi for **Salgsordre_Organisasjon_Organisasjons-ID** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="a48ec-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="a48ec-188">Standard malverdi for **Produkt_Organisasjon_Organisasjons-ID** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="a48ec-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="a48ec-189">Sørg for at nødvendig tilordning eksister i **Kilde** > **CDS** for **DeliverCountryRegionID** til **DeliveryAdress_Country**.</span><span class="sxs-lookup"><span data-stu-id="a48ec-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="a48ec-190">Malverdi er **ValueMap** med et antall av land tilordnet.</span><span class="sxs-lookup"><span data-stu-id="a48ec-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="a48ec-191">Forsikre deg om at nødvendig **ValueMap** for **SalesUnitSymbol** i Finance and Operations eksisterer i **Kilde** > **CDS-tilordning**.</span><span class="sxs-lookup"><span data-stu-id="a48ec-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="a48ec-192">Malverdi med **ValueMap** er definert for **SalesUnitSymbol til Quanitiy_UOM**.</span><span class="sxs-lookup"><span data-stu-id="a48ec-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="a48ec-193">Tilordninge mal i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="a48ec-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="a48ec-194">Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke en del av standardtilordningene.</span><span class="sxs-lookup"><span data-stu-id="a48ec-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="a48ec-195">Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.</span><span class="sxs-lookup"><span data-stu-id="a48ec-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="a48ec-196">Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.</span><span class="sxs-lookup"><span data-stu-id="a48ec-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="a48ec-197">Ordrehode</span><span class="sxs-lookup"><span data-stu-id="a48ec-197">OrderHeader</span></span>

![Tilordninge mal i dataintegrator](./media/sales-order-template-mapping-data-integrator-1.png)

![Tilordninge mal i dataintegrator](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="a48ec-200">Ordrelinje</span><span class="sxs-lookup"><span data-stu-id="a48ec-200">OrderLine</span></span>

![Tilordninge mal i dataintegrator](./media/sales-order-template-mapping-data-integrator-3.png)

![Tilordninge mal i dataintegrator](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="a48ec-203">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="a48ec-203">Related topics</span></span>

[<span data-ttu-id="a48ec-204">Synkronisere produkter fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="a48ec-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="a48ec-205">Synkronisere kontoer fra Sales til kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a48ec-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="a48ec-206">Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a48ec-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="a48ec-207">Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a48ec-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="a48ec-208">Synkronisere salgsfakturahoder og -linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="a48ec-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


