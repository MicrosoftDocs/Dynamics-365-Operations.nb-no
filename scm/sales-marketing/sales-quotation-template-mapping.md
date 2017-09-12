---
title: Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations
description: "Emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere salgstilbudshoder og -linjer fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
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
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 172a3da1b6d90a25ea9ebd14265e70e4a6f9bd70
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="eaac0-103">Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="eaac0-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="eaac0-104">Før du kan bruke kundeemnet til kontanter løsning, ha kjennskap til [Dynamics 365 dataintegrering](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="eaac0-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="eaac0-105">Emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere salgstilbudshoder og -linjer fra Microsoft Dynamics 365 for Sales (Sales) til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="eaac0-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="eaac0-106">Mal og oppgaver</span><span class="sxs-lookup"><span data-stu-id="eaac0-106">Template and tasks</span></span>

<span data-ttu-id="eaac0-107">Følgende malene og underliggende oppgavene brukes til å synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="eaac0-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="eaac0-108">**Navnet på malen:** Salgstilbud (Sales til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="eaac0-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="eaac0-109">**Navnene på oppgavene i prosjektet:**</span><span class="sxs-lookup"><span data-stu-id="eaac0-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="eaac0-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="eaac0-110">QuoteHeader</span></span>
    - <span data-ttu-id="eaac0-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="eaac0-111">QuoteLine</span></span>

<span data-ttu-id="eaac0-112">Følgende synkroniseringsoppgaver er påkrevd før synkronisering av salgstilbudshoder og -linjer kan inntreffe:</span><span class="sxs-lookup"><span data-stu-id="eaac0-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="eaac0-113">Produkter</span><span class="sxs-lookup"><span data-stu-id="eaac0-113">Products</span></span>
- <span data-ttu-id="eaac0-114">Kontoer (hvis brukt)</span><span class="sxs-lookup"><span data-stu-id="eaac0-114">Accounts (if used)</span></span>
- <span data-ttu-id="eaac0-115">Kontakter (hvis brukt)</span><span class="sxs-lookup"><span data-stu-id="eaac0-115">Contacts (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="eaac0-116">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="eaac0-116">Entity set</span></span>

| <span data-ttu-id="eaac0-117">Salg</span><span class="sxs-lookup"><span data-stu-id="eaac0-117">Sales</span></span>        | <span data-ttu-id="eaac0-118">CDS</span><span class="sxs-lookup"><span data-stu-id="eaac0-118">CDS</span></span>           | <span data-ttu-id="eaac0-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="eaac0-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="eaac0-120">Tilbud</span><span class="sxs-lookup"><span data-stu-id="eaac0-120">Quotes</span></span>       | <span data-ttu-id="eaac0-121">Tilbud</span><span class="sxs-lookup"><span data-stu-id="eaac0-121">Quotation</span></span>     | <span data-ttu-id="eaac0-122">Salgstilbudshoder</span><span class="sxs-lookup"><span data-stu-id="eaac0-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="eaac0-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="eaac0-123">QuoteDetails</span></span> | <span data-ttu-id="eaac0-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="eaac0-124">QuotationLine</span></span> | <span data-ttu-id="eaac0-125">CDS-salgstilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="eaac0-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="eaac0-126">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="eaac0-126">Entity flow</span></span>

<span data-ttu-id="eaac0-127">Salgstilbud opprettes i Sales og synkroniseres til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eaac0-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="eaac0-128">Salgstilbud fra Sales synkroniseres bare hvis følgende betingelser er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="eaac0-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="eaac0-129">Alle produktene i salgstilbudslinjene vedlikeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="eaac0-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="eaac0-130">Salgstilbudet er aktivt eller aktivert.</span><span class="sxs-lookup"><span data-stu-id="eaac0-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="eaac0-131">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="eaac0-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="eaac0-132">Feltet **Har bare eksternt vedlikeholdte produkter** er lagt til tilbudsenheten for konsistent sporing av om salgstilbudet består av bare eksternt vedlikeholdes produkter.</span><span class="sxs-lookup"><span data-stu-id="eaac0-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="eaac0-133">Hvis et salgstilbud har bare eksternt vedlikeholdte produkter, vedlikeholdes produktene i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eaac0-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="eaac0-134">Dette kan garantere at du ikke prøver å synkronisere salgstilbudslinjer med produkter som er ukjent for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eaac0-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="eaac0-135">Alle produkter og linjer i tilbudet oppdateres med informasjon fra **Har bare eksternt vedlikeholdte produkter** fra tilbudshodet.</span><span class="sxs-lookup"><span data-stu-id="eaac0-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="eaac0-136">Denne informasjonen finnes i feltet **Tilbud har bare eksternt vedlikeholdte produkter** på tilbudslinjeenheten.</span><span class="sxs-lookup"><span data-stu-id="eaac0-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="eaac0-137">Feltene **Rabatt**, **Gebyrer** og **Avgift** feltene kontrolleres av et sammensatt oppsett i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eaac0-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="eaac0-138">Dette oppsettet støtter for øyeblikket ikke integreringstilordning.</span><span class="sxs-lookup"><span data-stu-id="eaac0-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="eaac0-139">I den gjeldende utformingen adminstreres og håndteres feltene **Pris**, **Rabatt**, **Gebyrer** og **Avgift** av Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eaac0-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="eaac0-140">I Sales gjør løsningen at følgende felt er skrivebeskyttet, fordi verdiene ikke er synkronisert til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="eaac0-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="eaac0-141">**Skrivebeskyttede felt i salgstilbudshodet:** Rabattprosent, Rabatt, Fraktbeløp</span><span class="sxs-lookup"><span data-stu-id="eaac0-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="eaac0-142">**Skrivebeskyttede felt på salgstilbudslinjer:** Mva</span><span class="sxs-lookup"><span data-stu-id="eaac0-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="eaac0-143">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="eaac0-143">Preconditions and mapping setup</span></span>

- <span data-ttu-id="eaac0-144">Før du synkroniserer salgstilbud kan du i Sales gå til **Innstillinger** &gt; **Administrasjon** &gt; **Systeminnstillinger** &gt; **Salg** og kontrollere at feltet **Rabattberegningsmetode** er angitt til **Per enhet**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-144">Before you synchronize sales quotations, in Sales, go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="eaac0-145">Denne innstillingen garanterer at linjevarerabatten fra Sales samsvarer med innstillingen i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eaac0-145">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="eaac0-146">Ellers blir ikke rabatten riktig i Finance and Operations, fordi Finance and Operations leser rabatten som en rabatt per enhet, selv om det var en rabatt per linje i Sales.</span><span class="sxs-lookup"><span data-stu-id="eaac0-146">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>
- <span data-ttu-id="eaac0-147">I Finance and Operations går du til **Kunder** &gt; **Oppsett** &gt; **Kundeparametere**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-147">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="eaac0-148">På kategorien **Nummerserie** velger du nummerserien for salgstilbud og klkker deretter **Vis detaljer**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-148">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="eaac0-149">Deretter, under **Generelt oppsett**, angis feltet **Manuelt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-149">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="eaac0-150">I Finance and Operations går du til **Kunder** &gt; **Oppsett** &gt; **Kundeparametere**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-150">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="eaac0-151">På kategorien **Forsendelser** angir du feltet **Leveringsdatokontroll** til **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-151">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="eaac0-152">Denne innstillingen forhindrer synkronisering fra å mislykkes for salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="eaac0-152">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="eaac0-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="eaac0-153">QuoteHeader</span></span>

- <span data-ttu-id="eaac0-154">Feltet **Ønsket leveringsdato** kreves i Finance and Operations, og synkroniseringen mislykkes hvis feltet er tomt.</span><span class="sxs-lookup"><span data-stu-id="eaac0-154">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="eaac0-155">For å unngå dette problemet, hentes en standarddato fra **Kilde &gt; CDS** hvis feltet er tomt.</span><span class="sxs-lookup"><span data-stu-id="eaac0-155">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="eaac0-156">Datoen bør oppdateres til en ønsket verdi.</span><span class="sxs-lookup"><span data-stu-id="eaac0-156">The date should be updated to a preferred value.</span></span> <span data-ttu-id="eaac0-157">For øyeblikket ikke kan du angi en verdi som **I dag** for å representere dagens dato.</span><span class="sxs-lookup"><span data-stu-id="eaac0-157">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="eaac0-158">Du må angi en spesifikk dato.</span><span class="sxs-lookup"><span data-stu-id="eaac0-158">You must enter a specific date.</span></span> <span data-ttu-id="eaac0-159">Standardmalverdien for **Ønsket leveringsdato** er **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-159">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="eaac0-160">Feltet **Kode for adresse, land og område** er obligatorisk i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eaac0-160">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="eaac0-161">For å forhindre synkroniseringsfeil, kan du angi en standardverdi som skal brukes hvis feltet er tomt i Sales.</span><span class="sxs-lookup"><span data-stu-id="eaac0-161">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="eaac0-162">Denne standardverdien er også nyttig, fordi du ikke trenger for å skrive inn en verdi i feltet **Land område** for lokale adresser.</span><span class="sxs-lookup"><span data-stu-id="eaac0-162">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="eaac0-163">Det finnes ingen standardmalverdi for **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-163">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="eaac0-164">Oppdater tilordningen for **ID for CDS-organisasjon** i **Kilden &gt; CDS**, slik at den samsvarer med **CDS-organisasjon** i organisasjonsenheten:</span><span class="sxs-lookup"><span data-stu-id="eaac0-164">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="eaac0-165">Standardmalverdien for **Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-165">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="eaac0-166">Standardmalverdien for **Account_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-166">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="eaac0-167">Standardmalverdien for **InvoiceAccount_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-167">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

### <a name="quoteline"></a><span data-ttu-id="eaac0-168">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="eaac0-168">QuoteLine</span></span>

- <span data-ttu-id="eaac0-169">Oppdater tilordningen for **ID for CDS-organisasjon** i **Kilden &gt; CDS**, slik at den samsvarer med **CDS-organisasjon** i organisasjonsenheten:</span><span class="sxs-lookup"><span data-stu-id="eaac0-169">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="eaac0-170">Standardmalverdien for **Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-170">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="eaac0-171">Standardmalverdien for **Product_Organization_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-171">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="eaac0-172">Standardmalverdien for **Quotation_Organization_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-172">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="eaac0-173">Feltet **Ønsket leveringsdato** kreves i Finance and Operations, og synkroniseringen mislykkes hvis feltet er tomt.</span><span class="sxs-lookup"><span data-stu-id="eaac0-173">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="eaac0-174">For å unngå dette problemet, hentes en standarddato fra **Kilde &gt; CDS** hvis feltet er tomt.</span><span class="sxs-lookup"><span data-stu-id="eaac0-174">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="eaac0-175">Datoen bør oppdateres til en ønsket verdi.</span><span class="sxs-lookup"><span data-stu-id="eaac0-175">The date should be updated to a preferred value.</span></span> <span data-ttu-id="eaac0-176">For øyeblikket ikke kan du angi en verdi som **I dag** for å representere dagens dato.</span><span class="sxs-lookup"><span data-stu-id="eaac0-176">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="eaac0-177">Du må angi en spesifikk dato.</span><span class="sxs-lookup"><span data-stu-id="eaac0-177">You must enter a specific date.</span></span> <span data-ttu-id="eaac0-178">Standardmalverdien for **Ønsket leveringsdato** er **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-178">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="eaac0-179">Du kan legge til følgende tilordninger fra **CDS &gt; Mål** for å garantere at tilbudslinjene importeres til Finance and Operations hvis det finnes ingen standardinformasjon fra kunden eller produktet:</span><span class="sxs-lookup"><span data-stu-id="eaac0-179">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="eaac0-180">**SiteId** – et område er nødvendig for å generere tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eaac0-180">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="eaac0-181">Det finnes ingen standardmalverdi for **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-181">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="eaac0-182">**WarehouseId** – et lager er nødvendig for å behandle tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eaac0-182">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="eaac0-183">Det finnes ingen standardmalverdi for **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-183">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="eaac0-184">Pass på at den nødvendige verditilordningen for selgende måleenheten i Finance and Operations finnes i tilordnignen **CDS &gt; Mål** for **Quantity_UOM** til **SALESUNITSYMBOL**.</span><span class="sxs-lookup"><span data-stu-id="eaac0-184">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="eaac0-185">Tilordninge mal i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="eaac0-185">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="eaac0-186">Feltene **Rabatt**, **Gebyrer** og **Avgift** feltene kontrolleres av et sammensatt oppsett i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eaac0-186">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="eaac0-187">Dette oppsettet støtter for øyeblikket ikke integreringstilordning.</span><span class="sxs-lookup"><span data-stu-id="eaac0-187">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="eaac0-188">I den gjeldende utformingen håndteres feltene **Pris**, **Rabatt**, **Gebyrer** og **Avgift** av Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eaac0-188">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="eaac0-189">Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke en del av standardtilordningene.</span><span class="sxs-lookup"><span data-stu-id="eaac0-189">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="eaac0-190">Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.</span><span class="sxs-lookup"><span data-stu-id="eaac0-190">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="eaac0-191">Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.</span><span class="sxs-lookup"><span data-stu-id="eaac0-191">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="eaac0-192">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="eaac0-192">QuoteHeader</span></span>

![Tilordninge mal i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Tilordninge mal i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="eaac0-195">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="eaac0-195">QuoteLine</span></span>

![Tilordninge mal i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Tilordninge mal i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="eaac0-198">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="eaac0-198">Related topics</span></span>

[<span data-ttu-id="eaac0-199">Synkronisere produkter fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="eaac0-199">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="eaac0-200">Synkronisere kontoer fra Sales til kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="eaac0-200">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="eaac0-201">Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="eaac0-201">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



