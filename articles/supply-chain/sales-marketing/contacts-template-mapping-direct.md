---
title: Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Finance and Operations
description: "Dette emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere kontakt (kontakter)- og kontakt (kunder)-enheter fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.openlocfilehash: 8de9a920f384b69c9b3764a0431208bbdcb395bf
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="15dc6-103">Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="15dc6-103">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="15dc6-104">Før du kan bruke kundeemnet til kontanter løsning, må du ha kjennskap til [Dynamics 365-dataintegrering](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="15dc6-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="15dc6-105">Dette emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere kontakt (kontakter)- og kontakt (kunder)-enheter direkte fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="15dc6-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) entities directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="15dc6-106">Dataflyt i Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="15dc6-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="15dc6-107">Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="15dc6-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="15dc6-108">Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data om kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="15dc6-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="15dc6-109">Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="15dc6-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="15dc6-110">[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="15dc6-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="15dc6-111">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="15dc6-111">Templates and tasks</span></span>

<span data-ttu-id="15dc6-112">Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="15dc6-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="15dc6-113">Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.</span><span class="sxs-lookup"><span data-stu-id="15dc6-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="15dc6-114">Følgende malene og underliggende oppgavene brukes til å synkronisere kontakt (kontakter)-enheter i Sales til kontakt (kunder)-enheter i Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="15dc6-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) entities in Sales to Contact (Customers) entities in Finance and Operations:</span></span>

- <span data-ttu-id="15dc6-115">**Navnet på malen i Dataintegrering**:</span><span class="sxs-lookup"><span data-stu-id="15dc6-115">**Names of the templates in Data integration:**</span></span>

    - <span data-ttu-id="15dc6-116">Kontakter (Sales til Fin and Ops) – direkte</span><span class="sxs-lookup"><span data-stu-id="15dc6-116">Contacts (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="15dc6-117">Kontakter til Kunde (Sales til Fin and Ops) – direkte</span><span class="sxs-lookup"><span data-stu-id="15dc6-117">Contacts to Customer (Sales to Fin and Ops) - Direct</span></span>

- <span data-ttu-id="15dc6-118">**Navnet på oppgaven i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="15dc6-118">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="15dc6-119">Kontakter</span><span class="sxs-lookup"><span data-stu-id="15dc6-119">Contacts</span></span>
    - <span data-ttu-id="15dc6-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="15dc6-120">ContactToCustomer</span></span>

<span data-ttu-id="15dc6-121">Følgende synkroniseringsoppgave kreves før synkronisering av kontakt kan utføres: Kontoer (Sales til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="15dc6-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="15dc6-122">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="15dc6-122">Entity sets</span></span>

| <span data-ttu-id="15dc6-123">Salg</span><span class="sxs-lookup"><span data-stu-id="15dc6-123">Sales</span></span>    | <span data-ttu-id="15dc6-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="15dc6-124">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="15dc6-125">Kontakter</span><span class="sxs-lookup"><span data-stu-id="15dc6-125">Contacts</span></span> | <span data-ttu-id="15dc6-126">CDS-kontakter</span><span class="sxs-lookup"><span data-stu-id="15dc6-126">CDS Contacts</span></span>           |
| <span data-ttu-id="15dc6-127">Kontakter</span><span class="sxs-lookup"><span data-stu-id="15dc6-127">Contacts</span></span> | <span data-ttu-id="15dc6-128">Kunder V2</span><span class="sxs-lookup"><span data-stu-id="15dc6-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="15dc6-129">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="15dc6-129">Entity flow</span></span>

<span data-ttu-id="15dc6-130">Kontakter administreres i Sales og synkroniseres til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="15dc6-130">Contacts are managed in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="15dc6-131">En kontakt i Sales kan bli en kontakt eller kunde i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="15dc6-131">A contact in Sales can become either a contact or a customer in Finance and Operations.</span></span> <span data-ttu-id="15dc6-132">For å fastslå om en kontakt i Sales skal synkroniseres med Finance and Operations som en kontakt eller en kunde, vurderer systemet følgende egenskaper for kontakten i Sales:</span><span class="sxs-lookup"><span data-stu-id="15dc6-132">To determine whether a contact in Sales should be synchronized to Finance and Operations as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="15dc6-133">**Synkronisere til en kunde i Finance and Operations**: Kontakter hvor **Er aktiv kunde** er satt til **Ja**</span><span class="sxs-lookup"><span data-stu-id="15dc6-133">**Synchronization to a customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="15dc6-134">**Synkronisere til en kontakt i Finance and Operations**: Kontakter hvor **Er aktiv kunde** er satt til **Nei** og **Bedrift** (overordnet konto/kontakt) peker til en konto (ikke en kontakt)</span><span class="sxs-lookup"><span data-stu-id="15dc6-134">**Synchronization to a contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="15dc6-135">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="15dc6-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="15dc6-136">Et nytt **Er aktiv kunde**-felt er blitt lagt til for kontakten.</span><span class="sxs-lookup"><span data-stu-id="15dc6-136">A new **Is Active Customer** field has been added to the contact.</span></span> <span data-ttu-id="15dc6-137">Dette feltet brukes til å skille mellom kontakter med salgsaktivitet og kontakter som ikke har salgsaktivitet.</span><span class="sxs-lookup"><span data-stu-id="15dc6-137">This field is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="15dc6-138">**Er aktiv kunde** er satt til **Ja** bare for kontakter som har lignende tilbud, ordrer eller fakturaer.</span><span class="sxs-lookup"><span data-stu-id="15dc6-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="15dc6-139">Bare disse kontaktene synkroniseres til Finance and Operations som kunder.</span><span class="sxs-lookup"><span data-stu-id="15dc6-139">Only those contacts are synchronized to Finance and Operations as customers.</span></span>

<span data-ttu-id="15dc6-140">Et nytt **IsCompanyAnAccount**-felt er blitt lagt til for kontakten.</span><span class="sxs-lookup"><span data-stu-id="15dc6-140">A new **IsCompanyAnAccount** field has been added to the contact.</span></span> <span data-ttu-id="15dc6-141">Dette feltet brukes til å angi om en kontakt er koblet til et firma (overordnet konto//kontakt) av **Konto**-typen.</span><span class="sxs-lookup"><span data-stu-id="15dc6-141">This field indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="15dc6-142">Denne informasjonen brukes til å identifisere kontakter som skal synkroniseres til Finance and Operations som kontakter.</span><span class="sxs-lookup"><span data-stu-id="15dc6-142">This information is used to identify contacts that should be synchronized to Finance and Operations as contacts.</span></span>

<span data-ttu-id="15dc6-143">Et nytt **Kontaktnummer**-felt har blitt lagt til kontakten for å garantere en naturlig og unik nøkkel for integreringen.</span><span class="sxs-lookup"><span data-stu-id="15dc6-143">A new **Contact Number** field has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="15dc6-144">Når det opprettes en ny kontakt, en **Kontaktnummer**-verdi genereres automatisk ved hjelp av en nummerserie.</span><span class="sxs-lookup"><span data-stu-id="15dc6-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="15dc6-145">Verdien består av **CON**, etterfulgt av en økende nummerserie og et suffiks på seks tegn.</span><span class="sxs-lookup"><span data-stu-id="15dc6-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="15dc6-146">Her er et eksempel: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="15dc6-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="15dc6-147">Når integreringsløsningen for Sales legges til, angir et oppgraderingsskript **Kontaktnummer**-feltet for eksisterende kontakter ved hjelp av nummerserien som ble beskrevet tidligere.</span><span class="sxs-lookup"><span data-stu-id="15dc6-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** field for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="15dc6-148">Oppgraderingsskriptet angir også feltet **Er aktiv kunde** til **Ja** for alle kontaktene med salgsaktivitet.</span><span class="sxs-lookup"><span data-stu-id="15dc6-148">The upgrade script also sets the **Is Active Customer** field to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="15dc6-149">I Finance og Operations</span><span class="sxs-lookup"><span data-stu-id="15dc6-149">In Finance and Operations</span></span>

<span data-ttu-id="15dc6-150">Kontakter er kodet ved hjelp av egenskapen **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="15dc6-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="15dc6-151">Denne egenskapen angir at en gitt kontakt vedlikeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="15dc6-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="15dc6-152">I så fall vedlikeholdes eksterne kontakter i Sales.</span><span class="sxs-lookup"><span data-stu-id="15dc6-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="15dc6-153">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="15dc6-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="15dc6-154">Kontakt til kunde</span><span class="sxs-lookup"><span data-stu-id="15dc6-154">Contact to customer</span></span>

- <span data-ttu-id="15dc6-155">**CustomerGroup** er obligatorisk i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="15dc6-155">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="15dc6-156">Hvis du vil unngå synkroniseringsfeil, kan du angi en standardverdi i tilordningen.</span><span class="sxs-lookup"><span data-stu-id="15dc6-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="15dc6-157">Den standardverdien brukes deretter hvis feltet er tomt i Sales.</span><span class="sxs-lookup"><span data-stu-id="15dc6-157">That default value is then used if the field is left blank in Sales.</span></span>

    <span data-ttu-id="15dc6-158">Standardmalverdien er **10**.</span><span class="sxs-lookup"><span data-stu-id="15dc6-158">The default template value is **10**.</span></span>

- <span data-ttu-id="15dc6-159">Ved å legge til følgende tilordninger kan du redusere antallet manuelle oppdateringer som kreves i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="15dc6-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="15dc6-160">Du kan bruke standardverdi eller verditilordning fra for eksempel **Land/område** eller **By**.</span><span class="sxs-lookup"><span data-stu-id="15dc6-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="15dc6-161">**SiteId** – Et standardområde kan også defineres for produkter i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="15dc6-161">**SiteId** – A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="15dc6-162">Et område er nødvendig for å generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="15dc6-162">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="15dc6-163">En malverdi for **SiteId** er ikke angitt.</span><span class="sxs-lookup"><span data-stu-id="15dc6-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="15dc6-164">**WarehouseId** – Et standardlager kan også defineres for produkter i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="15dc6-164">**WarehouseId** – A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="15dc6-165">Et lager er nødvendig for å generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="15dc6-165">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="15dc6-166">En malverdi for **WarehouseId** er ikke angitt.</span><span class="sxs-lookup"><span data-stu-id="15dc6-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="15dc6-167">**LanguageId** – et språk er nødvendig for å generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="15dc6-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span>
    
        <span data-ttu-id="15dc6-168">Standardmalverdien er **en-us**.</span><span class="sxs-lookup"><span data-stu-id="15dc6-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="15dc6-169">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="15dc6-169">Template mapping in Data integration</span></span>

<span data-ttu-id="15dc6-170">Følgende illustrasjoner viser et eksempel på en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="15dc6-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="15dc6-171">Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="15dc6-171">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="15dc6-172">Kontakt til kontakt</span><span class="sxs-lookup"><span data-stu-id="15dc6-172">Contact to contact</span></span>

![Maltilordning i Dataintegrator](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="15dc6-174">Kontakt til kunde</span><span class="sxs-lookup"><span data-stu-id="15dc6-174">Contact to customer</span></span>

![Maltilordning i Dataintegrator](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="15dc6-176">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="15dc6-176">Related topics</span></span>

[<span data-ttu-id="15dc6-177">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="15dc6-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="15dc6-178">Synkronisere kontoer direkte fra Sales til kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="15dc6-178">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="15dc6-179">Synkronisere produkter direkte fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="15dc6-179">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="15dc6-180">Synkronisere salgsordrehoder og -linjer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="15dc6-180">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)

[<span data-ttu-id="15dc6-181">Synkronisere salgsfakturahoder og -linjer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="15dc6-181">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)



