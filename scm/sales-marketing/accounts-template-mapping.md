---
title: Synkronisere kontoer fra Sales til kunder i Finance and Operations
description: "Emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere kontoer fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.openlocfilehash: b497f078d9786a5c7630e924da6bb04cad37f5e9
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="a8603-103">Synkronisere kontoer fra Sales til kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a8603-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a8603-104">Før du kan bruke kundeemnet til kontanter løsning, ha kjennskap til [Dynamics 365 dataintegrering](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="a8603-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="a8603-105">Emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere kontoer fra Microsoft Dynamics 365 for Sales (Sales) til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="a8603-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="a8603-106">Mal og oppgave</span><span class="sxs-lookup"><span data-stu-id="a8603-106">Template and task</span></span>

<span data-ttu-id="a8603-107">Følgende malene og underliggende oppgavene brukes til å synkronisere kontoer fra Sales til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a8603-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="a8603-108">**Navnet på malen:** Kontoer (Sales til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="a8603-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="a8603-109">**Navnet på oppgaven i prosjektet:** Kontoer - Konto - Kunder</span><span class="sxs-lookup"><span data-stu-id="a8603-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="a8603-110">Synkronisere oppgaver som kreves før konto / kunde synkronisering: Ingen</span><span class="sxs-lookup"><span data-stu-id="a8603-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="a8603-111">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="a8603-111">Entity set</span></span>

| <span data-ttu-id="a8603-112">Salg</span><span class="sxs-lookup"><span data-stu-id="a8603-112">Sales</span></span>    | <span data-ttu-id="a8603-113">CDS</span><span class="sxs-lookup"><span data-stu-id="a8603-113">CDS</span></span>     | <span data-ttu-id="a8603-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a8603-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="a8603-115">Kontoer</span><span class="sxs-lookup"><span data-stu-id="a8603-115">Accounts</span></span> | <span data-ttu-id="a8603-116">Konto</span><span class="sxs-lookup"><span data-stu-id="a8603-116">Account</span></span> | <span data-ttu-id="a8603-117">Kunder</span><span class="sxs-lookup"><span data-stu-id="a8603-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="a8603-118">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="a8603-118">Entity flow</span></span>

<span data-ttu-id="a8603-119">Kontoer administreres i Sales og synkroniseres med Finance and Operations som kunder.</span><span class="sxs-lookup"><span data-stu-id="a8603-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="a8603-120">Egenskapen **Vedlikeholdes eksternt** på disse kundene er satt til **Ja** til å spore kunder som kommer fra ordrer.</span><span class="sxs-lookup"><span data-stu-id="a8603-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="a8603-121">Denne informasjonen brukes til å filtrere fakturaer som synkroniseres til Sales under fakturering.</span><span class="sxs-lookup"><span data-stu-id="a8603-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="a8603-122">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="a8603-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="a8603-123">**Kontonummer**-feltet er bare tilgjengelig på **Konto**-siden.</span><span class="sxs-lookup"><span data-stu-id="a8603-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="a8603-124">Det er gjort en naturlig og unik nøkkel for å støtte integrering.</span><span class="sxs-lookup"><span data-stu-id="a8603-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="a8603-125">Funksjonen for naturlig nøkkel i CRM-løsningen (Customer Relationship Management) kan påvirke kunder som bruker allerede **Kontonummer**-feltet, men som ikke bruker unike **Kontonummer**-verdier per konto.</span><span class="sxs-lookup"><span data-stu-id="a8603-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="a8603-126">Integreringsløsningen støtter for øyeblikket ikke denne saken.</span><span class="sxs-lookup"><span data-stu-id="a8603-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="a8603-127">Når en ny konto opprettes, hvis en **Kontonummer**-verdi ikke finnes fra før, den genereres automatisk ved hjelp av en nummerserie.</span><span class="sxs-lookup"><span data-stu-id="a8603-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="a8603-128">Verdien består av **ACC**, etterfulgt av en økende nummerserie og et suffiks på seks tegn.</span><span class="sxs-lookup"><span data-stu-id="a8603-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="a8603-129">Her er et eksempel: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="a8603-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="a8603-130">Når det brukes integration-løsning for Sales, angir et oppgraderingsskript **Kontonummer** for eksisterende kontoer i Sales.</span><span class="sxs-lookup"><span data-stu-id="a8603-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="a8603-131">Hvis det finnes ingen **Kontonummer**-verdier, nummerserien som ble omtalt tidligere brukes.</span><span class="sxs-lookup"><span data-stu-id="a8603-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="a8603-132">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="a8603-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="a8603-133">**CustomerGroupId** må oppdateres til en gyldig verdi i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8603-133">**CustomerGroupId** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="a8603-134">Du kan angi en standardverdi, eller du kan angi verdien ved hjelp av en verditilordningen.</span><span class="sxs-lookup"><span data-stu-id="a8603-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="a8603-135">Standardmalverdien er **10**.</span><span class="sxs-lookup"><span data-stu-id="a8603-135">The default template value is **10**.</span></span>
- <span data-ttu-id="a8603-136">**Kode for adresse, land og område** er obligatorisk i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8603-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="a8603-137">Hvis du vil unngå synkroniseringsfeil, kan du angi en standardverdi.</span><span class="sxs-lookup"><span data-stu-id="a8603-137">To avoid synchronization errors, you can specify a default value.</span></span> <span data-ttu-id="a8603-138">Den standardverdien brukes deretter hvis feltet er tomt i Sales.</span><span class="sxs-lookup"><span data-stu-id="a8603-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="a8603-139">Standardmalverdien for **AddressCountryRegionISOCode** er **USA**.</span><span class="sxs-lookup"><span data-stu-id="a8603-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="a8603-140">Standardmalverdien for **DeliveryAddressCountryRegionISOCode** er **USA**.</span><span class="sxs-lookup"><span data-stu-id="a8603-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="a8603-141">Ved å legge til følgende tilordninger fra **CDS &gt; Mål** kan du redusere antallet manuelle oppdateringer som kreves i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8603-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="a8603-142">Du kan bruke standardverdi eller verditilordning fra for eksempel **Land/område** eller **By**.</span><span class="sxs-lookup"><span data-stu-id="a8603-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="a8603-143">**SiteId** – et område er nødvendig for å generere tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8603-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="a8603-144">Et standardområde kan hentes fra produktet eller fra kunden fra ordrehodet.</span><span class="sxs-lookup"><span data-stu-id="a8603-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="a8603-145">Standardmalverdien for **SiteId** er **1**.</span><span class="sxs-lookup"><span data-stu-id="a8603-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="a8603-146">**WarehouseId** – et lager er nødvendig for å behandle tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8603-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="a8603-147">Et standardlager kan hentes fra produktet eller fra kunden fra ordrehodet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8603-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="a8603-148">Standardmalverdien for **WarehouseId** er **13**.</span><span class="sxs-lookup"><span data-stu-id="a8603-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="a8603-149">**LanguageId** – et språk er nødvendig for å generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8603-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="a8603-150">Som standard brukes språket fra ordrehodet fra kunden.</span><span class="sxs-lookup"><span data-stu-id="a8603-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="a8603-151">Standardmalverdien for **LanguageId** er **en-us**.</span><span class="sxs-lookup"><span data-stu-id="a8603-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="a8603-152">Oppdater ID- en for CDS-organisasjonen (**Organization_OrganizationId**) i tilordningen av **Kilde &gt;CDS**.</span><span class="sxs-lookup"><span data-stu-id="a8603-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="a8603-153">Standardmalverdien er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="a8603-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="a8603-154">Tilordninge mal i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="a8603-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="a8603-155">Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke inkludert i standardtilordningene.</span><span class="sxs-lookup"><span data-stu-id="a8603-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="a8603-156">Hvis du vil tilordne disse feltene, må du definere en verditilordning.</span><span class="sxs-lookup"><span data-stu-id="a8603-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="a8603-157">Verditilordninger er spesifikke for dataene i organisasjoner som enheten synkroniseres mellom.</span><span class="sxs-lookup"><span data-stu-id="a8603-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="a8603-158">Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.</span><span class="sxs-lookup"><span data-stu-id="a8603-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Tilordninge mal i dataintegrator](./media/accounts-template-mapping-data-integrator-1.png)

![Tilordne mal for kontoer i dataintegrator](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="a8603-161">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="a8603-161">Related topics</span></span>

[<span data-ttu-id="a8603-162">Synkronisere produkter fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="a8603-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="a8603-163">Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a8603-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="a8603-164">Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a8603-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)




