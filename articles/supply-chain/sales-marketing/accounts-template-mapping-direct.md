---
title: Synkronisere kontoer direkte fra Sales til kunder i Supply Chain Management
description: Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere forretningsforbindelser fra Dynamics 365 Sales til Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 8aa03f94e0fb89a6d34ce014dbb6004a1a666327
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529216"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="a4dc6-103">Synkronisere kontoer direkte fra Sales til kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a4dc6-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="a4dc6-104">Før du kan bruke kundeemnet til kontanter løsning må du ha kjennskap til [Integrere data til Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="a4dc6-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="a4dc6-105">Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere forretningsforbindelser direkte fra Dynamics 365 Sales til Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="a4dc6-106">Dataflyt i Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="a4dc6-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="a4dc6-107">Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="a4dc6-108">Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data om kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="a4dc6-109">Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="a4dc6-110">[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="a4dc6-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a4dc6-111">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="a4dc6-111">Templates and tasks</span></span>

<span data-ttu-id="a4dc6-112">Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for Power Apps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="a4dc6-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="a4dc6-113">Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a4dc6-114">Følgende maler og underliggende oppgaver brukes til å synkronisere kontoer fra Sales til Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="a4dc6-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="a4dc6-115">**Navnet på malen i Dataintegrering:** Kontoer (Sales til Fin and Ops) – direkte</span><span class="sxs-lookup"><span data-stu-id="a4dc6-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="a4dc6-116">**Navnet på oppgaven i prosjektet:** Kontoer - Kunder</span><span class="sxs-lookup"><span data-stu-id="a4dc6-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="a4dc6-117">Ingen synkroniseringsoppgaver kreves før konto-/kundesynkronisering kan utføres.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="a4dc6-118">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="a4dc6-118">Entity set</span></span>

| <span data-ttu-id="a4dc6-119">Salg</span><span class="sxs-lookup"><span data-stu-id="a4dc6-119">Sales</span></span>    | <span data-ttu-id="a4dc6-120">Forsyningskjedeadministrasjon</span><span class="sxs-lookup"><span data-stu-id="a4dc6-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="a4dc6-121">Kontoer</span><span class="sxs-lookup"><span data-stu-id="a4dc6-121">Accounts</span></span> | <span data-ttu-id="a4dc6-122">Kunder V2</span><span class="sxs-lookup"><span data-stu-id="a4dc6-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="a4dc6-123">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="a4dc6-123">Entity flow</span></span>

<span data-ttu-id="a4dc6-124">Kontoer administreres i Sales og synkroniseres med Supply Chain Management som kunder.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="a4dc6-125">Egenskapen **Vedlikeholdes eksternt** på disse kundene er satt til **Ja** til å spore kunder som kommer fra ordrer.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="a4dc6-126">Denne informasjonen brukes til å filtrere fakturaer som synkroniseres til Sales under fakturering.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="a4dc6-127">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="a4dc6-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="a4dc6-128">**Kontonummer**-feltet er bare tilgjengelig på **Konto**-siden.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="a4dc6-129">Det er gjort en naturlig og unik nøkkel for å støtte integrering.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="a4dc6-130">Funksjonen for naturlig nøkkel i CRM-løsningen (Customer Relationship Management) kan påvirke kunder som bruker allerede **Kontonummer**-feltet, men som ikke bruker unike **Kontonummer**-verdier per konto.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="a4dc6-131">Integreringsløsningen støtter for øyeblikket ikke denne saken.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="a4dc6-132">Når en ny konto opprettes, hvis en **Kontonummer**-verdi ikke finnes fra før, den genereres automatisk ved hjelp av en nummerserie.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="a4dc6-133">Verdien består av **ACC**, etterfulgt av en økende nummerserie og et suffiks på seks tegn.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="a4dc6-134">Her er et eksempel: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="a4dc6-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="a4dc6-135">Når det brukes integration-løsning for Sales, angir et oppgraderingsskript **Kontonummer** for eksisterende kontoer i Sales.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="a4dc6-136">Hvis det finnes ingen **Kontonummer**-verdier, nummerserien som ble omtalt tidligere brukes.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="a4dc6-137">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="a4dc6-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="a4dc6-138">Tilordningen **CustomerGroupId** må oppdateres til en gyldig verdi i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="a4dc6-139">Du kan angi en standardverdi, eller du kan angi verdien ved hjelp av en verditilordningen.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="a4dc6-140">Standardmalverdien er **10**.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-140">The default template value is **10**.</span></span>

- <span data-ttu-id="a4dc6-141">Ved å legge til følgende tilordninger kan du redusere antallet manuelle oppdateringer som kreves i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="a4dc6-142">Du kan bruke standardverdi eller verditilordning fra for eksempel **Land/område** eller **By**.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="a4dc6-143">**SiteId** – et område er nødvendig for å generere tilbud og salgsordrelinjer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="a4dc6-144">Et standardområde kan hentes fra produktet eller fra kunden fra ordrehodet.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="a4dc6-145">Standardmalverdien er **1**.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="a4dc6-146">**WarehouseId** – et lager er nødvendig for å behandle tilbud og salgsordrelinjer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="a4dc6-147">Et standardlager kan hentes fra produktet eller fra kunden fra ordrehodet i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="a4dc6-148">Standardmalverdien er **13**.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="a4dc6-149">**LanguageId** – et språk er nødvendig for å generere tilbud og salgsordrer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="a4dc6-150">Som standard brukes språket fra ordrehodet fra kunden.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="a4dc6-151">Standardmalverdien er **en-us**.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a4dc6-152">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="a4dc6-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="a4dc6-153">Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke inkludert i standardtilordningene.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="a4dc6-154">Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="a4dc6-155">Følgende illustrasjoner viser et eksempel på en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="a4dc6-156">Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a4dc6-156">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Maltilordning i Dataintegrering](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="a4dc6-158">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="a4dc6-158">Related topics</span></span>


[<span data-ttu-id="a4dc6-159">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="a4dc6-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="a4dc6-160">Synkronisere kontoer direkte fra Sales til kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a4dc6-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="a4dc6-161">Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a4dc6-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="a4dc6-162">Synkronisering av salgsordrer direkte mellom Sales og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a4dc6-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="a4dc6-163">Synkronisere salgsfakturahoder og -linjer direkte fra Supply Chain Management til Sales</span><span class="sxs-lookup"><span data-stu-id="a4dc6-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

