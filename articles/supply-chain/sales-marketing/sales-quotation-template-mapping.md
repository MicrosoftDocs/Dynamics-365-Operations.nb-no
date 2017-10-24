---
title: Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations
description: "Emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere salgstilbudshoder og -linjer fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 9117b5af3beff7290816586f63091b12e357339c
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="50187-103">Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50187-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="50187-104">Før du kan bruke kundeemnet til kontanter løsning, ha kjennskap til [Dynamics 365 dataintegrering](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="50187-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="50187-105">Emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere salgstilbudshoder og -linjer fra Microsoft Dynamics 365 for Sales (Sales) til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="50187-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="50187-106">Mal og oppgaver</span><span class="sxs-lookup"><span data-stu-id="50187-106">Template and tasks</span></span>

<span data-ttu-id="50187-107">Følgende malene og underliggende oppgavene brukes til å synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="50187-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="50187-108">**Navnet på malen:** Salgstilbud (Sales til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="50187-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="50187-109">**Navnene på oppgavene i prosjektet:**</span><span class="sxs-lookup"><span data-stu-id="50187-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="50187-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="50187-110">QuoteHeader</span></span>
    - <span data-ttu-id="50187-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="50187-111">QuoteLine</span></span>

<span data-ttu-id="50187-112">Følgende synkroniseringsoppgaver er påkrevd før synkronisering av salgstilbudshoder og -linjer kan inntreffe:</span><span class="sxs-lookup"><span data-stu-id="50187-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="50187-113">Produkter (Fin and Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="50187-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="50187-114">Kontoer (Sales til Fin and Ops) (hvis brukt)</span><span class="sxs-lookup"><span data-stu-id="50187-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="50187-115">Kontakter til Kunder (Sales til Fin and Ops) (hvis brukt)</span><span class="sxs-lookup"><span data-stu-id="50187-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="50187-116">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="50187-116">Entity set</span></span>

| <span data-ttu-id="50187-117">Salg</span><span class="sxs-lookup"><span data-stu-id="50187-117">Sales</span></span>        | <span data-ttu-id="50187-118">CDS</span><span class="sxs-lookup"><span data-stu-id="50187-118">CDS</span></span>           | <span data-ttu-id="50187-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50187-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="50187-120">Tilbud</span><span class="sxs-lookup"><span data-stu-id="50187-120">Quotes</span></span>       | <span data-ttu-id="50187-121">Tilbud</span><span class="sxs-lookup"><span data-stu-id="50187-121">Quotation</span></span>     | <span data-ttu-id="50187-122">Salgstilbudshoder</span><span class="sxs-lookup"><span data-stu-id="50187-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="50187-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="50187-123">QuoteDetails</span></span> | <span data-ttu-id="50187-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="50187-124">QuotationLine</span></span> | <span data-ttu-id="50187-125">CDS-salgstilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="50187-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="50187-126">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="50187-126">Entity flow</span></span>

<span data-ttu-id="50187-127">Salgstilbud opprettes i Sales og synkroniseres til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50187-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="50187-128">Salgstilbud fra Sales synkroniseres bare hvis følgende betingelser er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="50187-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="50187-129">Alle produktene i salgstilbudslinjene vedlikeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="50187-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="50187-130">Salgstilbudet er aktivt eller aktivert.</span><span class="sxs-lookup"><span data-stu-id="50187-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="50187-131">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="50187-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="50187-132">Feltet **Har bare eksternt vedlikeholdte produkter** er lagt til tilbudsenheten for konsistent sporing av om salgstilbudet består av bare eksternt vedlikeholdes produkter.</span><span class="sxs-lookup"><span data-stu-id="50187-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="50187-133">Hvis et salgstilbud har bare eksternt vedlikeholdte produkter, vedlikeholdes produktene i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50187-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="50187-134">Dette kan garantere at du ikke prøver å synkronisere salgstilbudslinjer med produkter som er ukjent for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50187-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="50187-135">Alle produkter og linjer i tilbudet oppdateres med informasjon fra **Har bare eksternt vedlikeholdte produkter** fra tilbudshodet.</span><span class="sxs-lookup"><span data-stu-id="50187-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="50187-136">Denne informasjonen finnes i feltet **Tilbud har bare eksternt vedlikeholdte produkter** på tilbudslinjeenheten.</span><span class="sxs-lookup"><span data-stu-id="50187-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="50187-137">Feltene **Rabatt**, **Gebyrer** og **Avgift** feltene kontrolleres av et sammensatt oppsett i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50187-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="50187-138">Dette oppsettet støtter for øyeblikket ikke integreringstilordning.</span><span class="sxs-lookup"><span data-stu-id="50187-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="50187-139">I den gjeldende utformingen adminstreres og håndteres feltene **Pris**, **Rabatt**, **Gebyrer** og **Avgift** av Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50187-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="50187-140">I Sales gjør løsningen at følgende felt er skrivebeskyttet, fordi verdiene ikke er synkronisert til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="50187-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="50187-141">**Skrivebeskyttede felt i salgstilbudshodet:** Rabattprosent, Rabatt, Fraktbeløp</span><span class="sxs-lookup"><span data-stu-id="50187-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="50187-142">**Skrivebeskyttede felt på salgstilbudslinjer:** Mva</span><span class="sxs-lookup"><span data-stu-id="50187-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="50187-143">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="50187-143">Preconditions and mapping setup</span></span>

<span data-ttu-id="50187-144">Før synkronisering av salgsordre er det viktig å oppdatere systemet med følgende innstilling.</span><span class="sxs-lookup"><span data-stu-id="50187-144">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="50187-145">Oppsett i salg</span><span class="sxs-lookup"><span data-stu-id="50187-145">Setup in Sales</span></span>

- <span data-ttu-id="50187-146">Gå til **Innstillinger** &gt; **Administrasjon** &gt; **Systeminnstillinger** &gt; **Salg**, og forsikre deg om at feltet **Rabattberegningsmetode** er satt til **Per enhet**.</span><span class="sxs-lookup"><span data-stu-id="50187-146">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="50187-147">Denne innstillingen garanterer at linjevarerabatten fra Sales samsvarer med innstillingen i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50187-147">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="50187-148">Ellers blir ikke rabatten riktig i Finance and Operations, fordi Finance and Operations leser rabatten som en rabatt per enhet, selv om det var en rabatt per linje i Sales.</span><span class="sxs-lookup"><span data-stu-id="50187-148">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="50187-149">Oppsett i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50187-149">Setup in Finance and Operations</span></span>

- <span data-ttu-id="50187-150">Gå til **Kundefordringer** &gt; **Oppsett** &gt; **Parametere for kundefordringer**.</span><span class="sxs-lookup"><span data-stu-id="50187-150">Go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="50187-151">På kategorien **Nummerserie** velger du nummerserien for salgstilbud og klkker deretter **Vis detaljer**.</span><span class="sxs-lookup"><span data-stu-id="50187-151">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="50187-152">Deretter, under **Generelt oppsett**, angis feltet **Manuelt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="50187-152">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="50187-153">Gå til **Kundefordringer** &gt; **Oppsett** &gt; **Parametere for kundefordringer**.</span><span class="sxs-lookup"><span data-stu-id="50187-153">Go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="50187-154">På kategorien **Forsendelser** angir du feltet **Leveringsdatokontroll** til **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="50187-154">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="50187-155">Denne innstillingen forhindrer synkronisering fra å mislykkes for salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="50187-155">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="50187-156">Oppsett i Dataintegrasjonsprosjekt</span><span class="sxs-lookup"><span data-stu-id="50187-156">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="50187-157">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="50187-157">QuoteHeader</span></span>

- <span data-ttu-id="50187-158">Feltet **Ønsket leveringsdato** kreves i Finance and Operations, og synkroniseringen mislykkes hvis feltet er tomt.</span><span class="sxs-lookup"><span data-stu-id="50187-158">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="50187-159">For å unngå dette problemet, hentes en standarddato fra **Kilde &gt; CDS** hvis feltet er tomt.</span><span class="sxs-lookup"><span data-stu-id="50187-159">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="50187-160">Datoen bør oppdateres til en ønsket verdi.</span><span class="sxs-lookup"><span data-stu-id="50187-160">The date should be updated to a preferred value.</span></span> <span data-ttu-id="50187-161">For øyeblikket ikke kan du angi en verdi som **I dag** for å representere dagens dato.</span><span class="sxs-lookup"><span data-stu-id="50187-161">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="50187-162">Du må angi en spesifikk dato.</span><span class="sxs-lookup"><span data-stu-id="50187-162">You must enter a specific date.</span></span> <span data-ttu-id="50187-163">Standardmalverdien for **Ønsket leveringsdato** er **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="50187-163">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="50187-164">Feltet **Kode for adresse, land og område** er obligatorisk i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50187-164">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="50187-165">For å forhindre synkroniseringsfeil, kan du angi en standardverdi som skal brukes hvis feltet er tomt i Sales.</span><span class="sxs-lookup"><span data-stu-id="50187-165">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="50187-166">Denne standardverdien er også nyttig, fordi du ikke trenger for å skrive inn en verdi i feltet **Land område** for lokale adresser.</span><span class="sxs-lookup"><span data-stu-id="50187-166">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="50187-167">Det finnes ingen standardmalverdi for **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="50187-167">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="50187-168">Oppdater tilordningen for **ID for CDS-organisasjon** i **Kilden &gt; CDS**, slik at den samsvarer med **CDS-organisasjon** i organisasjonsenheten:</span><span class="sxs-lookup"><span data-stu-id="50187-168">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="50187-169">Standardmalverdien for **Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="50187-169">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="50187-170">Standardmalverdien for **Account_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="50187-170">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="50187-171">Standardmalverdien for **InvoiceAccount_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="50187-171">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="50187-172">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="50187-172">QuoteLine</span></span>

- <span data-ttu-id="50187-173">Oppdater tilordningen for **ID for CDS-organisasjon** i **Kilden &gt; CDS**, slik at den samsvarer med **CDS-organisasjon** i organisasjonsenheten:</span><span class="sxs-lookup"><span data-stu-id="50187-173">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="50187-174">Standardmalverdien for **Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="50187-174">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="50187-175">Standardmalverdien for **Product_Organization_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="50187-175">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="50187-176">Standardmalverdien for **Quotation_Organization_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="50187-176">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="50187-177">Feltet **Ønsket leveringsdato** kreves i Finance and Operations, og synkroniseringen mislykkes hvis feltet er tomt.</span><span class="sxs-lookup"><span data-stu-id="50187-177">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="50187-178">For å unngå dette problemet, hentes en standarddato fra **Kilde &gt; CDS** hvis feltet er tomt.</span><span class="sxs-lookup"><span data-stu-id="50187-178">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="50187-179">Datoen bør oppdateres til en ønsket verdi.</span><span class="sxs-lookup"><span data-stu-id="50187-179">The date should be updated to a preferred value.</span></span> <span data-ttu-id="50187-180">For øyeblikket ikke kan du angi en verdi som **I dag** for å representere dagens dato.</span><span class="sxs-lookup"><span data-stu-id="50187-180">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="50187-181">Du må angi en spesifikk dato.</span><span class="sxs-lookup"><span data-stu-id="50187-181">You must enter a specific date.</span></span> <span data-ttu-id="50187-182">Standardmalverdien for **Ønsket leveringsdato** er **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="50187-182">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="50187-183">Du kan legge til følgende tilordninger fra **CDS &gt; Mål** for å garantere at tilbudslinjene importeres til Finance and Operations hvis det finnes ingen standardinformasjon fra kunden eller produktet:</span><span class="sxs-lookup"><span data-stu-id="50187-183">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="50187-184">**SiteId** – et område er nødvendig for å generere tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50187-184">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="50187-185">Det finnes ingen standardmalverdi for **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="50187-185">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="50187-186">**WarehouseId** – et lager er nødvendig for å behandle tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50187-186">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="50187-187">Det finnes ingen standardmalverdi for **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="50187-187">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="50187-188">Pass på at den nødvendige verditilordningen for selgende måleenheten i Finance and Operations finnes i tilordnignen **CDS &gt; Mål** for **Quantity_UOM** til **SALESUNITSYMBOL**.</span><span class="sxs-lookup"><span data-stu-id="50187-188">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="50187-189">Tilordninge mal i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="50187-189">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="50187-190">Feltene **Rabatt**, **Gebyrer** og **Avgift** feltene kontrolleres av et sammensatt oppsett i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50187-190">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="50187-191">Dette oppsettet støtter for øyeblikket ikke integreringstilordning.</span><span class="sxs-lookup"><span data-stu-id="50187-191">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="50187-192">I den gjeldende utformingen håndteres feltene **Pris**, **Rabatt**, **Gebyrer** og **Avgift** av Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50187-192">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="50187-193">Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke en del av standardtilordningene.</span><span class="sxs-lookup"><span data-stu-id="50187-193">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="50187-194">Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.</span><span class="sxs-lookup"><span data-stu-id="50187-194">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="50187-195">Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.</span><span class="sxs-lookup"><span data-stu-id="50187-195">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="50187-196">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="50187-196">QuoteHeader</span></span>

![Tilordninge mal i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Tilordninge mal i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="50187-199">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="50187-199">QuoteLine</span></span>

![Tilordninge mal i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Tilordninge mal i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="50187-202">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="50187-202">Related topics</span></span>

[<span data-ttu-id="50187-203">Synkronisere produkter fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="50187-203">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="50187-204">Synkronisere kontoer fra Sales til kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50187-204">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="50187-205">Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50187-205">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



