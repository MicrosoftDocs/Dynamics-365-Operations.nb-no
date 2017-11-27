---
title: Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations
description: "Dette emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere kontakt (kontakter) og kontakt (kunder) fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.openlocfilehash: c838fef502f643c764fade9cd79ae770ffc36974
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="c25f8-103">Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c25f8-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="c25f8-104">Før du kan bruke kundeemnet til kontanter løsning, ha kjennskap til [Dynamics 365 dataintegrering](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="c25f8-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="c25f8-105">Dette emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere kontaktenheter (kontakter) og kontakt (kunder) fra Microsoft Dynamics 365 for Sales (Sales) til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="c25f8-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c25f8-106">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="c25f8-106">Templates and tasks</span></span>

<span data-ttu-id="c25f8-107">Følgende malene og underliggende oppgavene brukes til å synkronisere kontakt (kontakter) i Sales til kontakt (kunder) i Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="c25f8-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="c25f8-108">**Navnene på malene:**</span><span class="sxs-lookup"><span data-stu-id="c25f8-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="c25f8-109">Kontakter (Sales to Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="c25f8-109">Contacts (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="c25f8-110">Kontakter til Kunde (Sales til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="c25f8-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="c25f8-111">**Navnene på oppgavene i prosjektet:**</span><span class="sxs-lookup"><span data-stu-id="c25f8-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="c25f8-112">Kontakter</span><span class="sxs-lookup"><span data-stu-id="c25f8-112">Contacts</span></span>
    - <span data-ttu-id="c25f8-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="c25f8-113">ContactToCustomer</span></span>

<span data-ttu-id="c25f8-114">Følgende synkroniseringsoppgave kreves før synkronisering av kontakt: Kontoer (Sales til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="c25f8-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="c25f8-115">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="c25f8-115">Entity sets</span></span>

| <span data-ttu-id="c25f8-116">Salg</span><span class="sxs-lookup"><span data-stu-id="c25f8-116">Sales</span></span>    | <span data-ttu-id="c25f8-117">CDS</span><span class="sxs-lookup"><span data-stu-id="c25f8-117">CDS</span></span>     | <span data-ttu-id="c25f8-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c25f8-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="c25f8-119">Kontakter</span><span class="sxs-lookup"><span data-stu-id="c25f8-119">Contacts</span></span> | <span data-ttu-id="c25f8-120">Kontakt</span><span class="sxs-lookup"><span data-stu-id="c25f8-120">Contact</span></span> | <span data-ttu-id="c25f8-121">CDS-kontakter</span><span class="sxs-lookup"><span data-stu-id="c25f8-121">CDS Contacts</span></span>           |
| <span data-ttu-id="c25f8-122">Kontakter</span><span class="sxs-lookup"><span data-stu-id="c25f8-122">Contacts</span></span> | <span data-ttu-id="c25f8-123">Konto</span><span class="sxs-lookup"><span data-stu-id="c25f8-123">Account</span></span> | <span data-ttu-id="c25f8-124">Kunder V2</span><span class="sxs-lookup"><span data-stu-id="c25f8-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="c25f8-125">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="c25f8-125">Entity flow</span></span>

<span data-ttu-id="c25f8-126">Kontakter administreres i Sales og synkroniseres til Common Data Service (CDS) og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c25f8-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="c25f8-127">En kontakt i Sales kan bli en kontakt i CDS og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c25f8-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="c25f8-128">Den kan også bli en konto i CDS og en kunde i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c25f8-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="c25f8-129">For å finne ut om en kontakt skal plukkes i Sales for synkronisering til CDS og Finance and Operations (for eksempel kontakter i Sales &gt; Kontakt i CDS &gt; Kontakter i Finance and Operations), ser systemet på følgende egenskaper for kontakten i Sales:</span><span class="sxs-lookup"><span data-stu-id="c25f8-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="c25f8-130">**Synkronisere til konto i CDS og kunde i Finance and Operations:** Kontakter hvor **Er aktiv kunde** er satt til **Ja**</span><span class="sxs-lookup"><span data-stu-id="c25f8-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="c25f8-131">**Synkronisere til kontakt i CDS og kontakt i Finance and Operations:** Kontakter hvor **Er aktiv kunde** er satt til **Nei** og **Bedrift** (overordnet konto/kontakt) peker til en konto (ikke en kontakt)</span><span class="sxs-lookup"><span data-stu-id="c25f8-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c25f8-132">Kundeemnet til kontanter løsning for Sales</span><span class="sxs-lookup"><span data-stu-id="c25f8-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="c25f8-133">Et nytt **Er aktiv kunde**-felt er blitt lagt til for kontakten.</span><span class="sxs-lookup"><span data-stu-id="c25f8-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="c25f8-134">Dette feltet brukes til å skille mellom kontakter med salgsaktivitet og kontakter som ikke har salgsaktivitet.</span><span class="sxs-lookup"><span data-stu-id="c25f8-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="c25f8-135">**Er aktiv kunde** er satt til **Ja** bare for kontakter som har lignende tilbud, ordrer eller fakturaer.</span><span class="sxs-lookup"><span data-stu-id="c25f8-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="c25f8-136">Bare disse kontaktene synkroniseres til Finance and Operations som kunder.</span><span class="sxs-lookup"><span data-stu-id="c25f8-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="c25f8-137">Et nytt **IsCompanyAnAccount**-felt er blitt lagt til for kontakten.</span><span class="sxs-lookup"><span data-stu-id="c25f8-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="c25f8-138">Dette feltet brukes til å angi om en kontakt er koblet til et firma (overordnet konto//kontakt) av **Konto**-typen.</span><span class="sxs-lookup"><span data-stu-id="c25f8-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="c25f8-139">Denne informasjonen brukes til å identifisere kontakter som skal synkroniseres til Finance and Operations som kontakter.</span><span class="sxs-lookup"><span data-stu-id="c25f8-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="c25f8-140">Et nytt **Kontaktnummer**-felt har blitt lagt til kontakten for å garantere en naturlig og unik nøkkel for integreringen.</span><span class="sxs-lookup"><span data-stu-id="c25f8-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="c25f8-141">Når det opprettes en ny kontakt, en **Kontaktnummer**-verdi genereres automatisk ved hjelp av en nummerserie.</span><span class="sxs-lookup"><span data-stu-id="c25f8-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="c25f8-142">Verdien består av **CON**, etterfulgt av en økende nummerserie og et suffiks på seks tegn.</span><span class="sxs-lookup"><span data-stu-id="c25f8-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="c25f8-143">Her er et eksempel: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="c25f8-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="c25f8-144">Når integreringsløsningen for Sales legges til i Sales, angir et oppgraderingsskript **Kontaktnummer**-feltet for eksisterende kontakter ved hjelp av nummerserien som ble beskrevet tidligere.</span><span class="sxs-lookup"><span data-stu-id="c25f8-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="c25f8-145">Oppgraderingsskriptet angir også feltet **Er aktiv kunde** til **Ja** for alle kontaktene med salgsaktivitet.</span><span class="sxs-lookup"><span data-stu-id="c25f8-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="c25f8-146">I Finance og Operations</span><span class="sxs-lookup"><span data-stu-id="c25f8-146">In Finance and Operations</span></span> 

<span data-ttu-id="c25f8-147">Kontakter er kodet ved hjelp av egenskapen **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="c25f8-148">Denne egenskapen angir at en gitt kontakt vedlikeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="c25f8-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="c25f8-149">I så fall vedlikeholdes eksterne kontakter i Sales.</span><span class="sxs-lookup"><span data-stu-id="c25f8-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="c25f8-150">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="c25f8-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="c25f8-151">Kontakt til kontakt</span><span class="sxs-lookup"><span data-stu-id="c25f8-151">Contact to Contact</span></span>

- <span data-ttu-id="c25f8-152">Oppdater **ID for CDS-organisasjon** i tilordningen **Kilde &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="c25f8-153">Standardmalverdien for **Organization_OrganizationId [Organisasjons-ID]** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="c25f8-154">Standardmalverdien for **PrimaryAccount_Organization_OrganizationId [Organisasjons-ID]** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="c25f8-155">**Kode for adresse, land og område** er obligatorisk i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c25f8-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="c25f8-156">Hvis du vil unngå synkroniseringsfeil, kan du angi en standardverdi i tilordningen **CDS &gt; Operasjoner**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="c25f8-157">Den standardverdien brukes deretter hvis feltet er tomt i Sales.</span><span class="sxs-lookup"><span data-stu-id="c25f8-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="c25f8-158">Standardmalverdien for **PrimaryAddressCountryRegionISOCode** er **USA**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="c25f8-159">Kontroller at det finnes en verdi for følgende felt i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c25f8-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="c25f8-160">Hvis informasjonen ikke er nødvendig i Finance and Operations, kan du fjerne tilordningen fra tilordningen **CDS &gt; Mål**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="c25f8-161">**Feltnavn i Finance and Operations:** Beslutning</span><span class="sxs-lookup"><span data-stu-id="c25f8-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="c25f8-162">**Tilordning:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="c25f8-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="c25f8-163">Kontakt til kunde</span><span class="sxs-lookup"><span data-stu-id="c25f8-163">Contact to Customer</span></span>

- <span data-ttu-id="c25f8-164">Oppdater **ID for CDS-organisasjon** i tilordningen **Kilde &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="c25f8-165">Standardmalverdien for **Organization_OrganizationId [Organisasjons-ID]** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="c25f8-166">**Kode for adresse, land og område** er obligatorisk i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c25f8-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="c25f8-167">Hvis du vil unngå synkroniseringsfeil, kan du angi en standardverdi i tilordningen **CDS &gt; Mal**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="c25f8-168">Den standardverdien brukes deretter hvis feltet er tomt i Sales.</span><span class="sxs-lookup"><span data-stu-id="c25f8-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="c25f8-169">Standardmalverdien for **PrimaryAddressCountryRegionISOCode** er **USA**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="c25f8-170">**CustomerGroup** er obligatorisk i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c25f8-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="c25f8-171">Hvis du vil unngå synkroniseringsfeil, kan du angi en standardverdi i tilordningen **CDS &gt; Mal**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="c25f8-172">Den standardverdien brukes deretter hvis feltet er tomt i Sales.</span><span class="sxs-lookup"><span data-stu-id="c25f8-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="c25f8-173">Standardmalverdien for **CustomerGroupId** er **10**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="c25f8-174">Ved å legge til følgende tilordninger fra **CDS &gt; Mål** kan du redusere antallet manuelle oppdateringer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c25f8-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="c25f8-175">Du kan bruke standardverdi eller verditilordning fra for eksempel **Land/område** eller **By**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="c25f8-176">**SiteId** - Et standardområde kan også defineres for produkter i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c25f8-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="c25f8-177">Et område er nødvendig for å generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c25f8-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="c25f8-178">En malverdi for **SiteId** er ikke angitt.</span><span class="sxs-lookup"><span data-stu-id="c25f8-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="c25f8-179">**WarehouseId** - Et standardlager kan også defineres for produkter i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c25f8-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="c25f8-180">Et lager er nødvendig for å generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c25f8-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="c25f8-181">En malverdi for **WarehouseId** er ikke angitt.</span><span class="sxs-lookup"><span data-stu-id="c25f8-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="c25f8-182">**LanguageId** - et språk er nødvendig for å generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c25f8-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="c25f8-183">Standardmalverdien for **LanguageId** er **en-us**.</span><span class="sxs-lookup"><span data-stu-id="c25f8-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="c25f8-184">Tilordninge mal i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="c25f8-184">Template mapping in data integrator</span></span>

<span data-ttu-id="c25f8-185">Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.</span><span class="sxs-lookup"><span data-stu-id="c25f8-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="c25f8-186">Kontakt til kontakt</span><span class="sxs-lookup"><span data-stu-id="c25f8-186">Contact to Contact</span></span>

![Tilordninge mal i dataintegrator](./media/contacts-template-mapping-data-integrator-1.png)

![Tilordne mal for kontakter i dataintegrator](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="c25f8-189">Kontakt til kunde</span><span class="sxs-lookup"><span data-stu-id="c25f8-189">Contact to Customer</span></span>

![Tilordninge mal i dataintegrator](./media/contacts-template-mapping-data-integrator-3.png)

![Tilordne mal for kontakter i dataintegrator](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="c25f8-192">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="c25f8-192">Related topics</span></span>

[<span data-ttu-id="c25f8-193">Synkronisere produkter fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="c25f8-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="c25f8-194">Synkronisere kontoer fra Sales til kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c25f8-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="c25f8-195">Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c25f8-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="c25f8-196">Synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="c25f8-196">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="c25f8-197">Synkronisere salgsfakturahoder og -linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="c25f8-197">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)

