---
title: Synkronisere salgstilbudshoder og -linjer direkte fra Sales til Finance and Operations
description: "Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere salgstilbudshoder og -linjer direkte fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a18c8f2c335dee723c104648f8c7c1b79ea569d5
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="03c66-103">Synkronisere salgstilbudshoder og -linjer direkte fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="03c66-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03c66-104">Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere salgstilbudshoder og -linjer direkte fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="03c66-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="03c66-105">Før du kan bruke kundeemnet til kontanter løsning, må du ha kjennskap til [Dynamics 365-dataintegrering](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="03c66-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="03c66-106">Mal og oppgaver</span><span class="sxs-lookup"><span data-stu-id="03c66-106">Template and tasks</span></span>

<span data-ttu-id="03c66-107">Følgende mal og underliggende oppgavene brukes til å synkronisere salgstilbudshoder og -linjer direkte fra Sales til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="03c66-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="03c66-108">**Navnet på malen i Dataintegrering:** Salgstilbud (Sales til Fin and Ops) – direkte</span><span class="sxs-lookup"><span data-stu-id="03c66-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="03c66-109">**Navnet på oppgaven i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="03c66-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="03c66-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="03c66-110">QuoteHeader</span></span>
    - <span data-ttu-id="03c66-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="03c66-111">QuoteLine</span></span>

<span data-ttu-id="03c66-112">Følgende synkroniseringsoppgaver er påkrevd før synkronisering av salgstilbudshoder og -linjer kan inntreffe:</span><span class="sxs-lookup"><span data-stu-id="03c66-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="03c66-113">Produkter (Fin and Ops til Sales) – direkte</span><span class="sxs-lookup"><span data-stu-id="03c66-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="03c66-114">Kontoer (Sales til Fin and Ops) – direkte (hvis brukt)</span><span class="sxs-lookup"><span data-stu-id="03c66-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="03c66-115">Kontakter til Kunder (Sales til Fin and Ops) – direkte (hvis brukt)</span><span class="sxs-lookup"><span data-stu-id="03c66-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="03c66-116">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="03c66-116">Entity set</span></span>

| <span data-ttu-id="03c66-117">Salg</span><span class="sxs-lookup"><span data-stu-id="03c66-117">Sales</span></span>        | <span data-ttu-id="03c66-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="03c66-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="03c66-119">Tilbud</span><span class="sxs-lookup"><span data-stu-id="03c66-119">Quotes</span></span>       | <span data-ttu-id="03c66-120">CDS-salgstilbudshode</span><span class="sxs-lookup"><span data-stu-id="03c66-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="03c66-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="03c66-121">QuoteDetails</span></span> | <span data-ttu-id="03c66-122">CDS-salgstilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="03c66-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="03c66-123">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="03c66-123">Entity flow</span></span>

<span data-ttu-id="03c66-124">Salgstilbud opprettes i Sales og synkroniseres til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="03c66-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="03c66-125">Salgstilbud fra Sales synkroniseres bare hvis følgende betingelser er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="03c66-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="03c66-126">Alle tilbudsproduktene i salgstilbudet vedlikeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="03c66-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="03c66-127">Når du har klikket på **Aktiver tilbud**, er salgstilbudet aktivert.</span><span class="sxs-lookup"><span data-stu-id="03c66-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="03c66-128">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="03c66-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="03c66-129">Feltet **Har bare eksternt vedlikeholdte produkter** er lagt til **tilbudsenheten** for konsistent sporing av om salgstilbudet består av bare eksternt vedlikeholdes produkter.</span><span class="sxs-lookup"><span data-stu-id="03c66-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="03c66-130">Hvis et salgstilbud har bare eksternt vedlikeholdte produkter, vedlikeholdes produktene i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="03c66-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="03c66-131">Dette kan garantere at du ikke prøver å synkronisere salgstilbudslinjer med produkter som er ukjent for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="03c66-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="03c66-132">Alle tilbudsprodukter i salgstilbudet oppdateres med informasjon fra **Har bare eksternt vedlikeholdte produkter** fra salgstilbudshodet.</span><span class="sxs-lookup"><span data-stu-id="03c66-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="03c66-133">Denne informasjonen finnes i feltet **Tilbud har bare eksternt vedlikeholdte produkter** på **QuoteDetails**-enheten.</span><span class="sxs-lookup"><span data-stu-id="03c66-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="03c66-134">En rabatt kan legges til tilbudsproduktet og vil bli synkronisert til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="03c66-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="03c66-135">Feltene **Rabatt**, **Gebyrer** og **Avgift** feltene på hodet kontrolleres av et oppsett i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="03c66-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="03c66-136">Dette oppsettet støtter for øyeblikket ikke integreringstilordning.</span><span class="sxs-lookup"><span data-stu-id="03c66-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="03c66-137">I den gjeldende utformingen adminstreres og vedlikeholdes feltene **Pris**, **Rabatt**, **Gebyrer** og **Avgift** i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="03c66-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="03c66-138">I Sales gjør løsningen at følgende felt er skrivebeskyttet, fordi verdiene ikke er synkronisert til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="03c66-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="03c66-139">Skrivebeskyttede felt i salgstilbudshodet: **Rabattprosent**, **Rabatt** og **Fraktbeløp**</span><span class="sxs-lookup"><span data-stu-id="03c66-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="03c66-140">Skrivebeskyttede felt på tilbudsprodukter: **Mva**</span><span class="sxs-lookup"><span data-stu-id="03c66-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="03c66-141">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="03c66-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="03c66-142">Før salgstilbud synkroniseres, er det viktig at du oppdaterer innstillingene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="03c66-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="03c66-143">Oppsett i salg</span><span class="sxs-lookup"><span data-stu-id="03c66-143">Setup in Sales</span></span>

- <span data-ttu-id="03c66-144">Kontroller at tillatelser er definert for temaet som brukeren fra Sales-tilkoblingssett er tildelt til.</span><span class="sxs-lookup"><span data-stu-id="03c66-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="03c66-145">Hvis du bruker demomstrasjonsdata, har brukeren vanligvis administratortilgang, men teamet har ikke administratortilgang.</span><span class="sxs-lookup"><span data-stu-id="03c66-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="03c66-146">Hvis teamet ikke har administratortilgang når du kjører prosjektet fra Dataintegrering, vil du få en feilmelding om at hovedteamet mangler.</span><span class="sxs-lookup"><span data-stu-id="03c66-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="03c66-147">Hvis du vil angi tillatelser for teamet, kan du gå til **Innstillinger** &gt; **Sikkerhet** &gt; **Team** og velge det aktuelle teamet.</span><span class="sxs-lookup"><span data-stu-id="03c66-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="03c66-148">Velg **Administrer roller**, og velg deretter en rolle som har de ønskede tillatelsene, for eksempel **Systemansvarlig**.</span><span class="sxs-lookup"><span data-stu-id="03c66-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="03c66-149">Gå til **Innstillinger** &gt; **Administrasjon** &gt; **Systeminnstillinger** &gt; **Salg**, og sørger for å bruke følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="03c66-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="03c66-150">Alternativet **Bruk systemets priskalkuleringssystem** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="03c66-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="03c66-151">Feltet **Rabattkalkuleringsmetode** er satt til **Linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="03c66-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="03c66-152">Oppsett i Dataintegrasjonsprosjekt</span><span class="sxs-lookup"><span data-stu-id="03c66-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="03c66-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="03c66-153">QuoteHeader</span></span>

- <span data-ttu-id="03c66-154">Sørg for at nødvendig tilordning finnes for **Shipto\_country** til **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="03c66-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="03c66-155">I den tilordnede verdien kan du definere en standardverdi som brukes hvis verdien er tom.</span><span class="sxs-lookup"><span data-stu-id="03c66-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="03c66-156">La venstre side være tom, og sett høyre side til ønsket land eller område.</span><span class="sxs-lookup"><span data-stu-id="03c66-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="03c66-157">På denne måten kan har du ikke skrive inn landet eller området for nasjonale ordrer.</span><span class="sxs-lookup"><span data-stu-id="03c66-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="03c66-158">Malverdien er en verditilordning der flere land eller områder er tilordnet, og der en tom verdi er verdien for **US**.</span><span class="sxs-lookup"><span data-stu-id="03c66-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="03c66-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="03c66-159">QuoteLine</span></span>

- <span data-ttu-id="03c66-160">Kontroller at den nødvendige verditilordningen finnes for **SalesUnitSymbol** i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="03c66-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="03c66-161">Kontroller at de nødvendige enhetene er definert i Sales.</span><span class="sxs-lookup"><span data-stu-id="03c66-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="03c66-162">En malverdi som har en verditilordningen er definert for **oumid.name** til **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="03c66-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="03c66-163">Valgfritt: Du kan legge til følgende tilordninger for å garantere at salgstilbudslinjene importeres til Finance and Operations hvis det finnes ingen standardinformasjon fra kunden eller produktet:</span><span class="sxs-lookup"><span data-stu-id="03c66-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="03c66-164">**SiteId** – et område er nødvendig for å generere tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="03c66-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="03c66-165">Det finnes ingen standardmalverdi for **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="03c66-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="03c66-166">**WarehouseId** – et lager er nødvendig for å behandle tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="03c66-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="03c66-167">Det finnes ingen standardmalverdi for **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="03c66-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="03c66-168">Tilordninge mal i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="03c66-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="03c66-169">Feltene **Rabatt**, **Gebyrer** og **Avgift** feltene kontrolleres av et sammensatt oppsett i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="03c66-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="03c66-170">Dette oppsettet støtter for øyeblikket ikke integreringstilordning.</span><span class="sxs-lookup"><span data-stu-id="03c66-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="03c66-171">I den gjeldende utformingen håndteres feltene **Pris**, **Rabatt**, **Gebyrer** og **Avgift** av Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="03c66-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="03c66-172">Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke en del av standardtilordningene.</span><span class="sxs-lookup"><span data-stu-id="03c66-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="03c66-173">Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.</span><span class="sxs-lookup"><span data-stu-id="03c66-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="03c66-174">Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.</span><span class="sxs-lookup"><span data-stu-id="03c66-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="03c66-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="03c66-175">QuoteHeader</span></span>

![Tilordninge mal i dataintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="03c66-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="03c66-177">QuoteLine</span></span>

![Tilordninge mal i dataintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="03c66-179">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="03c66-179">Related topics</span></span>

[<span data-ttu-id="03c66-180">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="03c66-180">Prospect to cash</span></span>](prospect-to-cash.md)


