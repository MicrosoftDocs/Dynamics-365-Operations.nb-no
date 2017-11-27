---
title: Synkronisere salgsordrehoder og -linjer direkte fra Finance and Operations til Sales
description: "Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere salgsordrehoder og -linjer direkte fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="b7e3f-103">Synkronisere salgsordrehoder og -linjer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="b7e3f-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b7e3f-104">Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere salgsordrehoder og -linjer direkte fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="b7e3f-105">Dataflyt i Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="b7e3f-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="b7e3f-106">Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="b7e3f-107">Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data om kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="b7e3f-108">Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="b7e3f-109">[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="b7e3f-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b7e3f-110">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="b7e3f-110">Templates and tasks</span></span>

<span data-ttu-id="b7e3f-111">Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="b7e3f-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="b7e3f-112">Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b7e3f-113">Følgende mal og underliggende oppgaver brukes til å synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales:</span><span class="sxs-lookup"><span data-stu-id="b7e3f-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="b7e3f-114">**Navnet på malen i Dataintegrering:** Salgsordrer (Fin and Ops til Sales) – direkte</span><span class="sxs-lookup"><span data-stu-id="b7e3f-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="b7e3f-115">**Navnet på oppgaven i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="b7e3f-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="b7e3f-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="b7e3f-116">OrderHeader</span></span>
    - <span data-ttu-id="b7e3f-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="b7e3f-117">OrderLine</span></span>

<span data-ttu-id="b7e3f-118">Følgende synkroniseringsoppgaver er påkrevd før synkronisering av salgsfakturahoder og -linjer kan inntreffe:</span><span class="sxs-lookup"><span data-stu-id="b7e3f-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="b7e3f-119">Produkter (Fin and Ops til Sales) – direkte</span><span class="sxs-lookup"><span data-stu-id="b7e3f-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="b7e3f-120">Kontoer (Sales til Fin and Ops) – direkte (hvis brukt)</span><span class="sxs-lookup"><span data-stu-id="b7e3f-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="b7e3f-121">Kontakter til Kunder (Sales til Fin and Ops) – direkte (hvis brukt)</span><span class="sxs-lookup"><span data-stu-id="b7e3f-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="b7e3f-122">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="b7e3f-122">Entity set</span></span>

| <span data-ttu-id="b7e3f-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b7e3f-123">Finance and Operations</span></span>  | <span data-ttu-id="b7e3f-124">Salg</span><span class="sxs-lookup"><span data-stu-id="b7e3f-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="b7e3f-125">CDS-salgsordrehoder</span><span class="sxs-lookup"><span data-stu-id="b7e3f-125">CDS sales order headers</span></span> | <span data-ttu-id="b7e3f-126">Salgsordrer</span><span class="sxs-lookup"><span data-stu-id="b7e3f-126">SalesOrders</span></span>       |
| <span data-ttu-id="b7e3f-127">CDS-salgsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="b7e3f-127">CDS sales order lines</span></span>   | <span data-ttu-id="b7e3f-128">Salgsordredetaljer</span><span class="sxs-lookup"><span data-stu-id="b7e3f-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="b7e3f-129">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="b7e3f-129">Entity flow</span></span>

<span data-ttu-id="b7e3f-130">Salgsordrer er opprettet i Finance and Operations og synkronisert til Sales.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="b7e3f-131">Filtre i malen garanterer at kun relevante salgsordrer er inkludert i synkroniseringen:</span><span class="sxs-lookup"><span data-stu-id="b7e3f-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="b7e3f-132">Både bestilling og fakturering av kunde på salgsordren som kommer fra Sales vil inkluderes i synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="b7e3f-133">I Finance and Operations brukes feltene **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** til å spore synkroniseringen i dataenhetene.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="b7e3f-134">Salgsordren i Finance and Operations må bekreftes.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="b7e3f-135">Kun bekreftede salgsordre eller salgsordre med høyere behandlingsstatus, for eksempel **Sendt** eller **Fakturert**, synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="b7e3f-136">Etter at en salgsordre er opprettet eller endret, må den satsvise jobben **Kalkuler salgstotaler** i Finance and Operations kjøres.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="b7e3f-137">Bare salgsordrene der salgsttotalene er beregnet, blir synkronisert Sales.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="b7e3f-138">Skatt knyttet til kostnader på Salgsordrehode er for øyeblikket ikke inkludert i synkronisering fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="b7e3f-139">Sales støtter ikke skatteinformasjon på hodenivå.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="b7e3f-140">Mva som er knyttet til tillegg på linjenivå er imidlertid inkludert i synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b7e3f-141">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="b7e3f-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="b7e3f-142">Nye felt er lagt til enheten **Ordre** og vises på siden:</span><span class="sxs-lookup"><span data-stu-id="b7e3f-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="b7e3f-143">**Er behandlet eksternt** – Sett dette alternativet til **Ja** når ordren kommer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="b7e3f-144">**Behandlingsstatus** – Dette feltet viser behandlingsstatus for en ordre i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="b7e3f-145">Følgende verdier er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="b7e3f-145">The following values are available:</span></span>

    - <span data-ttu-id="b7e3f-146">Aktivt</span><span class="sxs-lookup"><span data-stu-id="b7e3f-146">Active</span></span>
    - <span data-ttu-id="b7e3f-147">Bekreftet</span><span class="sxs-lookup"><span data-stu-id="b7e3f-147">Confirmed</span></span>
    - <span data-ttu-id="b7e3f-148">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="b7e3f-148">Packing Slip</span></span>
    - <span data-ttu-id="b7e3f-149">Fakturert</span><span class="sxs-lookup"><span data-stu-id="b7e3f-149">Invoiced</span></span>
    - <span data-ttu-id="b7e3f-150">Plukket</span><span class="sxs-lookup"><span data-stu-id="b7e3f-150">Picked</span></span>
    - <span data-ttu-id="b7e3f-151">Delvis plukket</span><span class="sxs-lookup"><span data-stu-id="b7e3f-151">Partially Picked</span></span>
    - <span data-ttu-id="b7e3f-152">Delvis pakket</span><span class="sxs-lookup"><span data-stu-id="b7e3f-152">Partially Packed</span></span>
    - <span data-ttu-id="b7e3f-153">Sendt</span><span class="sxs-lookup"><span data-stu-id="b7e3f-153">Shipped</span></span>
    - <span data-ttu-id="b7e3f-154">Delvis sendt</span><span class="sxs-lookup"><span data-stu-id="b7e3f-154">Partially Shipped</span></span>
    - <span data-ttu-id="b7e3f-155">Delvis fakturert</span><span class="sxs-lookup"><span data-stu-id="b7e3f-155">Partially Invoiced</span></span>
    - <span data-ttu-id="b7e3f-156">Avbrutt</span><span class="sxs-lookup"><span data-stu-id="b7e3f-156">Cancelled</span></span>

<span data-ttu-id="b7e3f-157">Innstillingen **Har bare eksternt vedlikeholdte produkter** brukes i andre salgsordrescenarier (for eksempel synkronisering fra Sales til Finance and Operation) for å holde oversikt over om en salgsordre helt og holdent består av eksternt behandlede produkter.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="b7e3f-158">Hvis en salgsordre består av bare eksternt vedlikeholdte produkter, vedlikeholdes produktene i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="b7e3f-159">Denne innstillingen kan garantere at du ikke prøver å synkronisere salgsordrelinjer med produkter som er ukjent for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="b7e3f-160">Knappene **Opprett faktura**, **Avbryt ordre**, **Rekalkuler**, **Få produkter** og **Søk opp adresser** på siden **Salgsordre** er skjult for eksternt behandlede ordrer fordi fakturaer vil opprettes i Finance and Operations og synkronisert til Sales.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="b7e3f-161">Ordresiden kan ikke redigeres fordi salgsordreinformasjon vil bli synkronisert fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="b7e3f-162">Salgsordrestatus vil fortsatt være **Aktiv** for å garantere at endringer fra Finance and Operations kan flyte fra salgsordren i Sales.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="b7e3f-163">Dette kontrolleres ved å sette standardverdien **Statuskode \[Status\]** til **Aktiv** i Dataintegrasjonsprosjektet.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b7e3f-164">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="b7e3f-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="b7e3f-165">Før du synkroniserer salgsordrer, er det viktig å oppdatere innstillingene nedenfor i systemene.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="b7e3f-166">Oppsett i salg</span><span class="sxs-lookup"><span data-stu-id="b7e3f-166">Setup in Sales</span></span>

- <span data-ttu-id="b7e3f-167">Kontroller at tillatelser er definert for temaet som brukeren fra Sales-tilkoblingssett er tildelt til.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="b7e3f-168">Hvis du bruker demomstrasjonsdata, har brukeren vanligvis administratortilgang, men teamet har ikke administratortilgang.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="b7e3f-169">Hvis teamet ikke også har administratortilgang når du kjører prosjektet fra Dataintegrering, vil du få en feilmelding om at hovedteamet mangler.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="b7e3f-170">Gå til **Innstillinger** > **Sikkerhet** > **Team**, velg relevant team. velg **Administrer roller** og velg en rolle med ønskede tillatelser, for eksempel **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="b7e3f-171">Gå til **Innstillinger** > **Administrasjon** > **Systeminnstillinger** > **Salg**, og sørger for å bruke følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="b7e3f-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="b7e3f-172">Alternativet **Bruk systemets priskalkuleringssystem** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="b7e3f-173">Feltet **Rabattkalkuleringsmetode** er satt til **Linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="b7e3f-174">Oppsett i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b7e3f-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="b7e3f-175">Gå til **Salg og markedsføring** > **Periodiske oppgaver** > **Beregn salgstotaler**, og angi at jobben skal kjøres som en satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="b7e3f-176">Sett alternativet **Beregnede totaler for salgsordrer** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="b7e3f-177">Dette trinnet er viktig fordi kun salgsordre med kalkulerte totale salg vil synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="b7e3f-178">Hyppigheten av den satsvise jobben skal være justert med hyppigheten av salgsordensynkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="b7e3f-179">Oppsett i Dataintegrasjonsprosjekt</span><span class="sxs-lookup"><span data-stu-id="b7e3f-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="b7e3f-180">Salgshode-oppgave</span><span class="sxs-lookup"><span data-stu-id="b7e3f-180">SalesHeader task</span></span>

- <span data-ttu-id="b7e3f-181">Sørg for at nødvendig tilordning finnes for **InvoiceCountryRegionId** til **BillingAddress\_Country** og for **DeliveryCountryRegionId** til **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="b7e3f-182">Malverdien er en verditilordning der flere land eller områder er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="b7e3f-183">En prisliste er nødvendig for å opprette ordrer i Sales.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="b7e3f-184">Oppdater verditilordningen for **pricelevelid.name\[Prislistenavn\]** til prislisten som brukes i Sales per valuta.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="b7e3f-185">Du kan bruke standard prisliste for en enkelt valuta.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="b7e3f-186">Hvis du har prislister i flere valutaer, kan du også bruke en verditilordning.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="b7e3f-187">Standard malverdi for **pricelevelid.name\[(Prislistenavn)\]** er **CRM Service USA (prøve)**.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="b7e3f-188">Salgslinje-oppgave</span><span class="sxs-lookup"><span data-stu-id="b7e3f-188">SalesLine task</span></span>

- <span data-ttu-id="b7e3f-189">Sørg for at nødvendig tilordning finnes for **DeliveryCountryRegionId** til **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="b7e3f-190">Malverdien er en verditilordning der flere land eller områder er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="b7e3f-191">Kontroller at den nødvendige verditilordningen finnes for **SalesUnitSymbol** i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="b7e3f-192">En malverdi som har en verditilordning er definert for **SalesUnitSymbol** til **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b7e3f-193">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="b7e3f-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="b7e3f-194">Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke inkludert i standardtilordningene.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="b7e3f-195">Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="b7e3f-196">Følgende illustrasjoner viser et eksempel på en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="b7e3f-197">Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b7e3f-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="b7e3f-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="b7e3f-198">OrderHeader</span></span>

![Maltilordning i Dataintegrator](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="b7e3f-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="b7e3f-200">OrderLine</span></span>

![Maltilordning i Dataintegrator](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="b7e3f-202">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="b7e3f-202">Related topics</span></span>

[<span data-ttu-id="b7e3f-203">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="b7e3f-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="b7e3f-204">Synkronisere kontoer direkte fra Sales til kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b7e3f-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="b7e3f-205">Synkronisere produkter direkte fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="b7e3f-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="b7e3f-206">Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b7e3f-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="b7e3f-207">Synkronisere salgsfakturahoder og -linjer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="b7e3f-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




