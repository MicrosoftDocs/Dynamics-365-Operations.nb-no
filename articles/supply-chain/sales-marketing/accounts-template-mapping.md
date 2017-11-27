---
title: Synkronisere kontoer fra Sales til kunder i Finance and Operations
description: "Emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere kontoer fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="dedfb-103">Synkronisere kontoer fra Sales til kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dedfb-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="dedfb-104">Før du kan bruke kundeemnet til kontanter løsning, ha kjennskap til [Dynamics 365 dataintegrering](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="dedfb-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="dedfb-105">Emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere kontoer fra Microsoft Dynamics 365 for Sales (Sales) til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="dedfb-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="dedfb-106">Mal og oppgave</span><span class="sxs-lookup"><span data-stu-id="dedfb-106">Template and task</span></span>

<span data-ttu-id="dedfb-107">Følgende malene og underliggende oppgavene brukes til å synkronisere kontoer fra Sales til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="dedfb-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="dedfb-108">**Navnet på malen:** Kontoer (Sales til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="dedfb-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="dedfb-109">**Navnet på oppgaven i prosjektet:** Kontoer - Konto - Kunder</span><span class="sxs-lookup"><span data-stu-id="dedfb-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="dedfb-110">Synkronisere oppgaver som kreves før konto / kunde synkronisering: Ingen</span><span class="sxs-lookup"><span data-stu-id="dedfb-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="dedfb-111">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="dedfb-111">Entity set</span></span>

| <span data-ttu-id="dedfb-112">Salg</span><span class="sxs-lookup"><span data-stu-id="dedfb-112">Sales</span></span>    | <span data-ttu-id="dedfb-113">CDS</span><span class="sxs-lookup"><span data-stu-id="dedfb-113">CDS</span></span>     | <span data-ttu-id="dedfb-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dedfb-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="dedfb-115">Kontoer</span><span class="sxs-lookup"><span data-stu-id="dedfb-115">Accounts</span></span> | <span data-ttu-id="dedfb-116">Konto</span><span class="sxs-lookup"><span data-stu-id="dedfb-116">Account</span></span> | <span data-ttu-id="dedfb-117">Kunder</span><span class="sxs-lookup"><span data-stu-id="dedfb-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="dedfb-118">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="dedfb-118">Entity flow</span></span>

<span data-ttu-id="dedfb-119">Kontoer administreres i Sales og synkroniseres med Finance and Operations som kunder.</span><span class="sxs-lookup"><span data-stu-id="dedfb-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="dedfb-120">Egenskapen **Vedlikeholdes eksternt** på disse kundene er satt til **Ja** til å spore kunder som kommer fra ordrer.</span><span class="sxs-lookup"><span data-stu-id="dedfb-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="dedfb-121">Denne informasjonen brukes til å filtrere fakturaer som synkroniseres til Sales under fakturering.</span><span class="sxs-lookup"><span data-stu-id="dedfb-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="dedfb-122">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="dedfb-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="dedfb-123">**Kontonummer**-feltet er bare tilgjengelig på **Konto**-siden.</span><span class="sxs-lookup"><span data-stu-id="dedfb-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="dedfb-124">Det er gjort en naturlig og unik nøkkel for å støtte integrering.</span><span class="sxs-lookup"><span data-stu-id="dedfb-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="dedfb-125">Funksjonen for naturlig nøkkel i CRM-løsningen (Customer Relationship Management) kan påvirke kunder som bruker allerede **Kontonummer**-feltet, men som ikke bruker unike **Kontonummer**-verdier per konto.</span><span class="sxs-lookup"><span data-stu-id="dedfb-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="dedfb-126">Integreringsløsningen støtter for øyeblikket ikke denne saken.</span><span class="sxs-lookup"><span data-stu-id="dedfb-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="dedfb-127">Når en ny konto opprettes, hvis en **Kontonummer**-verdi ikke finnes fra før, den genereres automatisk ved hjelp av en nummerserie.</span><span class="sxs-lookup"><span data-stu-id="dedfb-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="dedfb-128">Verdien består av **ACC**, etterfulgt av en økende nummerserie og et suffiks på seks tegn.</span><span class="sxs-lookup"><span data-stu-id="dedfb-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="dedfb-129">Her er et eksempel: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="dedfb-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="dedfb-130">Når det brukes integration-løsning for Sales, angir et oppgraderingsskript **Kontonummer** for eksisterende kontoer i Sales.</span><span class="sxs-lookup"><span data-stu-id="dedfb-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="dedfb-131">Hvis det finnes ingen **Kontonummer**-verdier, nummerserien som ble omtalt tidligere brukes.</span><span class="sxs-lookup"><span data-stu-id="dedfb-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="dedfb-132">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="dedfb-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="dedfb-133">**CustomerGroupId**-tilordning fra **CDS&gt;-destinasjon** må oppdateres til en gyldig verdi for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dedfb-133">**CustomerGroupId** mapping from **CDS &gt; Destination** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="dedfb-134">Du kan angi en standardverdi, eller du kan angi verdien ved hjelp av en verditilordningen.</span><span class="sxs-lookup"><span data-stu-id="dedfb-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="dedfb-135">Standardmalverdien er **10**.</span><span class="sxs-lookup"><span data-stu-id="dedfb-135">The default template value is **10**.</span></span>
- <span data-ttu-id="dedfb-136">**Kode for adresse, land og område** er obligatorisk i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dedfb-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="dedfb-137">For å unngå synkroniseringsfeil kan du angi en standardverdi i kartleggingen fra **CDS&gt;-destinasjon**.</span><span class="sxs-lookup"><span data-stu-id="dedfb-137">To avoid synchronization errors, you can specify a default value in the mapping from **CDS &gt; Destination**.</span></span> <span data-ttu-id="dedfb-138">Den standardverdien brukes deretter hvis feltet er tomt i Sales.</span><span class="sxs-lookup"><span data-stu-id="dedfb-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="dedfb-139">Standardmalverdien for **AddressCountryRegionISOCode** er **USA**.</span><span class="sxs-lookup"><span data-stu-id="dedfb-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="dedfb-140">Standardmalverdien for **DeliveryAddressCountryRegionISOCode** er **USA**.</span><span class="sxs-lookup"><span data-stu-id="dedfb-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="dedfb-141">Ved å legge til følgende tilordninger fra **CDS &gt; Mål** kan du redusere antallet manuelle oppdateringer som kreves i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dedfb-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="dedfb-142">Du kan bruke standardverdi eller verditilordning fra for eksempel **Land/område** eller **By**.</span><span class="sxs-lookup"><span data-stu-id="dedfb-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="dedfb-143">**SiteId** – et område er nødvendig for å generere tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dedfb-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="dedfb-144">Et standardområde kan hentes fra produktet eller fra kunden fra ordrehodet.</span><span class="sxs-lookup"><span data-stu-id="dedfb-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="dedfb-145">Standardmalverdien for **SiteId** er **1**.</span><span class="sxs-lookup"><span data-stu-id="dedfb-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="dedfb-146">**WarehouseId** – et lager er nødvendig for å behandle tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dedfb-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="dedfb-147">Et standardlager kan hentes fra produktet eller fra kunden fra ordrehodet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dedfb-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="dedfb-148">Standardmalverdien for **WarehouseId** er **13**.</span><span class="sxs-lookup"><span data-stu-id="dedfb-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="dedfb-149">**LanguageId** – et språk er nødvendig for å generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dedfb-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="dedfb-150">Som standard brukes språket fra ordrehodet fra kunden.</span><span class="sxs-lookup"><span data-stu-id="dedfb-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="dedfb-151">Standardmalverdien for **LanguageId** er **en-us**.</span><span class="sxs-lookup"><span data-stu-id="dedfb-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="dedfb-152">Oppdater ID- en for CDS-organisasjonen (**Organization_OrganizationId**) i tilordningen av **Kilde &gt;CDS**.</span><span class="sxs-lookup"><span data-stu-id="dedfb-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="dedfb-153">Standardmalverdien er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="dedfb-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="dedfb-154">Tilordninge mal i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="dedfb-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="dedfb-155">Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke inkludert i standardtilordningene.</span><span class="sxs-lookup"><span data-stu-id="dedfb-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="dedfb-156">Hvis du vil tilordne disse feltene, må du definere en verditilordning.</span><span class="sxs-lookup"><span data-stu-id="dedfb-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="dedfb-157">Verditilordninger er spesifikke for dataene i organisasjoner som enheten synkroniseres mellom.</span><span class="sxs-lookup"><span data-stu-id="dedfb-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="dedfb-158">Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.</span><span class="sxs-lookup"><span data-stu-id="dedfb-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Tilordninge mal i dataintegrator](./media/accounts-template-mapping-data-integrator-1.png)

![Tilordne mal for kontoer i dataintegrator](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="dedfb-161">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="dedfb-161">Related topics</span></span>

[<span data-ttu-id="dedfb-162">Synkronisere produkter fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="dedfb-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="dedfb-163">Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dedfb-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="dedfb-164">Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dedfb-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="dedfb-165">Synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="dedfb-165">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="dedfb-166">Synkronisere salgsfakturahoder og -linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="dedfb-166">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)




