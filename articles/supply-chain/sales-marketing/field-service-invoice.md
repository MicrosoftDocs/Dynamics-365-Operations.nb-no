---
title: Synkronisere avtalefakturaer i Field Service til fritekstfakturaer i Supply Chain Management
description: Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere avtalefakturaer i Dynamics 365 Field Service til friktekstfakturaer i Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 21a77a0289055285f47323803a484c012e662e3a
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102740"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="9520b-103">Synkronisere avtalefakturaer i Field Service til fritekstfakturaer i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9520b-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9520b-104">Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere avtalefakturaer i Dynamics 365 Field Service til friktekstfakturaer i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9520b-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="9520b-105">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="9520b-105">Templates and tasks</span></span>

<span data-ttu-id="9520b-106">Følgende mal og underliggende oppgaver brukes til å utføre synkronisering av avtalefakturaer fra Field Service til fritekstfakturaer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9520b-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="9520b-107">**Navnet på malen i Dataintegrasjon**</span><span class="sxs-lookup"><span data-stu-id="9520b-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="9520b-108">Avtalefakturaer (Field Service til Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="9520b-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="9520b-109">**Navnet på oppgaven i Dataintegrasjonprosjektet**</span><span class="sxs-lookup"><span data-stu-id="9520b-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="9520b-110">Fakturahoder</span><span class="sxs-lookup"><span data-stu-id="9520b-110">Invoice headers</span></span>
- <span data-ttu-id="9520b-111">Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="9520b-111">Invoice lines</span></span>

<span data-ttu-id="9520b-112">Følgende synkronisering er påkrevd før synkronisering av avtalefakturaer kan inntreffe:</span><span class="sxs-lookup"><span data-stu-id="9520b-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="9520b-113">Kontoer (Sales til Supply Chain Management) – direkte</span><span class="sxs-lookup"><span data-stu-id="9520b-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="9520b-114">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="9520b-114">Entity set</span></span>

| <span data-ttu-id="9520b-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="9520b-115">Field Service</span></span>  | <span data-ttu-id="9520b-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9520b-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="9520b-117">fakturaer</span><span class="sxs-lookup"><span data-stu-id="9520b-117">invoices</span></span>       | <span data-ttu-id="9520b-118">Fakturahoder i fritekst for Dataverse-kunde</span><span class="sxs-lookup"><span data-stu-id="9520b-118">Dataverse customer free text invoice headers</span></span> |
| <span data-ttu-id="9520b-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="9520b-119">invoicedetails</span></span> | <span data-ttu-id="9520b-120">Fakturalinjer i fritekst for Dataverse-kunde</span><span class="sxs-lookup"><span data-stu-id="9520b-120">Dataverse customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="9520b-121">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="9520b-121">Entity flow</span></span>

<span data-ttu-id="9520b-122">Fakturaer som opprettes fra en avtale i Field Service, kan synkroniseres til Supply Chain Management via et Microsoft Dataverse-dataintegreringsprosjekt.</span><span class="sxs-lookup"><span data-stu-id="9520b-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="9520b-123">Oppdateringer av disse fakturaene synkroniseres til fritekstfakturaene i Supply Chain Management hvis regnskapsstatusen for fritekstfakturaene er **Pågår**.</span><span class="sxs-lookup"><span data-stu-id="9520b-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="9520b-124">Når fritekstfakturaene blir postert i Supply Chain Management, og regnskapsstatusen oppdateres til **Fullført**, kan du ikke lenger synkronisere oppdateringer fra Field Service.</span><span class="sxs-lookup"><span data-stu-id="9520b-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="9520b-125">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="9520b-125">Field Service CRM solution</span></span>

<span data-ttu-id="9520b-126">Kolonnen **Har linjer med avtaleopprinnelse** er lagt til i **Faktura**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="9520b-126">The **Has Lines With Agreement Origin** column has been added to the **Invoice** table.</span></span> <span data-ttu-id="9520b-127">Denne kolonnen kan garantere at bare fakturaer som opprettes fra en avtale, synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="9520b-127">This column helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="9520b-128">Verdien er **sann** hvis fakturaen inneholder minst én fakturalinje som stammer fra en avtale.</span><span class="sxs-lookup"><span data-stu-id="9520b-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="9520b-129">Kolonnen **Har avtaleopprinnelse** er lagt til i **Fakturalinje**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="9520b-129">The **Has Agreement Origin** column has been added to the **Invoice Line** table.</span></span> <span data-ttu-id="9520b-130">Denne kolonnen bidrar til å garantere at bare fakturalinjer som opprettes fra en avtale, synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="9520b-130">This column helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="9520b-131">Verdien er **sann** hvis fakturalinjen stammer fra en avtale.</span><span class="sxs-lookup"><span data-stu-id="9520b-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="9520b-132">**Fakturadato** er et obligatorisk felt i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9520b-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="9520b-133">Kolonnen må derfor ha en verdi i Field Service før synkroniseringen utføres.</span><span class="sxs-lookup"><span data-stu-id="9520b-133">Therefore, the column must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="9520b-134">For å imøtekomme dette kravet legges følgende logikk til:</span><span class="sxs-lookup"><span data-stu-id="9520b-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="9520b-135">Hvis **Fakturadato**-kolonnen er tom i **Faktura**-tabellen (det vil si hvis den ikke har en verdi), blir den satt til gjeldende dato når en fakturalinje som stammer fra en avtale, legges til.</span><span class="sxs-lookup"><span data-stu-id="9520b-135">If the **Invoice Date** column is blank on the **Invoice** table (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="9520b-136">Brukeren kan endre **Fakturadato**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="9520b-136">The user can change the **Invoice Date** column.</span></span> <span data-ttu-id="9520b-137">Men når brukeren prøver å lagre en faktura som stammer fra en avtale, får vedkommende en forretningsprosessfeil hvis **Fakturadato**-kolonnen er tom på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="9520b-137">However, when the user tries to save an invoice that originates from an agreement, they receive a business process error if the **Invoice Date** column is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="9520b-138">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="9520b-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="9520b-139">I Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9520b-139">In Supply Chain Management</span></span>

<span data-ttu-id="9520b-140">En fakturaopprinnelse må være definert for integreringen for å skille fritekstfakturaene i Supply Chain Management som er opprettet fra avtalefakturaer i Field Service.</span><span class="sxs-lookup"><span data-stu-id="9520b-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="9520b-141">Når en faktura har en fakturaopprinnelse av typen **Integrering av avtalefaktura**, vises **Eksternt fakturanummer**-feltet i **Salgsfaktura**-hodet.</span><span class="sxs-lookup"><span data-stu-id="9520b-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="9520b-142">I tillegg til å vises i fakturahodet, kan **Eksternt fakturanummer**-informasjonen brukes til å sikre at fakturaer som opprettes fra Field Service-avtalefakturaer blir filtrert ut under fakturasynkronisering fra Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="9520b-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="9520b-143">Gå til **Kunder** \> **Oppsett** \> **Opprinnelseskoder for faktura**.</span><span class="sxs-lookup"><span data-stu-id="9520b-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="9520b-144">Velg **Ny** for å opprette en ny fakturaopprinnelse.</span><span class="sxs-lookup"><span data-stu-id="9520b-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="9520b-145">I **Fakturaopprinnelige**-feltet angir du et navn for fakturaopprinnelsen, for eksempel **FS**.</span><span class="sxs-lookup"><span data-stu-id="9520b-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="9520b-146">I **Beskrivelse**-feltet skriver du inn en beskrivelse, for eksempel **Avtalefakturaer i Field Service**.</span><span class="sxs-lookup"><span data-stu-id="9520b-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="9520b-147">Merk av for **Tilordning av opprinnelsestype**.</span><span class="sxs-lookup"><span data-stu-id="9520b-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="9520b-148">Sett **Opprinnelsestype for faktura**-feltet til **Integrering av avtalefaktura**.</span><span class="sxs-lookup"><span data-stu-id="9520b-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="9520b-149">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9520b-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="9520b-150">I dataintegrasjonsprosjektet</span><span class="sxs-lookup"><span data-stu-id="9520b-150">In the Data Integration project</span></span>

<span data-ttu-id="9520b-151">Oppgave: **Fakturalinjer**</span><span class="sxs-lookup"><span data-stu-id="9520b-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="9520b-152">Kontroller at standardverdien for Supply Chain Management-feltet **Visningsverdi for hovedkonto** oppdateres for å samsvare med den ønskede verdien.</span><span class="sxs-lookup"><span data-stu-id="9520b-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="9520b-153">Standardmalverdien er **401100**.</span><span class="sxs-lookup"><span data-stu-id="9520b-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9520b-154">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="9520b-154">Template mapping in Data integration</span></span>

<span data-ttu-id="9520b-155">Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="9520b-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="9520b-156">Avtalefakturaer (Field Service til Supply Chain Management): Fakturahoder</span><span class="sxs-lookup"><span data-stu-id="9520b-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="9520b-157">[![Maltilordning i Dataintegrering for fakturahoder](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="9520b-157">[![Template mapping in Data integration for invoice headers](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="9520b-158">Avtalefakturaer (Field Service til Supply Chain Management): Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="9520b-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="9520b-159">[![Maltilordning i Dataintegrering for fakturalinjer](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="9520b-159">[![Template mapping in Data integration for invoice lines](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]