---
title: Synkronisere avtalefakturaer i Field Service til fritekstfakturaer i Finance and Operations
description: Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere avtalefakturaer i Microsoft Dynamics 365 for Field Service til friktekstfakturaer i Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560170"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="ae1c4-103">Synkronisere avtalefakturaer i Field Service til fritekstfakturaer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ae1c4-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ae1c4-104">Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere avtalefakturaer i Microsoft Dynamics 365 for Field Service til friktekstfakturaer i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ae1c4-105">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="ae1c4-105">Templates and tasks</span></span>

<span data-ttu-id="ae1c4-106">Følgende mal og underliggende oppgaver brukes til å utføre synkronisering av avtalefakturaer fra Field Service til fritekstfakturaer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="ae1c4-107">**Navnet på malen i Dataintegrasjon:**</span><span class="sxs-lookup"><span data-stu-id="ae1c4-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="ae1c4-108">Avtalefakturaer (Field Service til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="ae1c4-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="ae1c4-109">**Navnet på oppgaven i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="ae1c4-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="ae1c4-110">Fakturahoder</span><span class="sxs-lookup"><span data-stu-id="ae1c4-110">Invoice headers</span></span>
- <span data-ttu-id="ae1c4-111">Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="ae1c4-111">Invoice lines</span></span>

<span data-ttu-id="ae1c4-112">Følgende synkronisering er påkrevd før synkronisering av avtalefakturaer kan inntreffe:</span><span class="sxs-lookup"><span data-stu-id="ae1c4-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="ae1c4-113">Kontoer (Sales til Fin and Ops) – direkte</span><span class="sxs-lookup"><span data-stu-id="ae1c4-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="ae1c4-114">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="ae1c4-114">Entity set</span></span>

| <span data-ttu-id="ae1c4-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="ae1c4-115">Field Service</span></span>  | <span data-ttu-id="ae1c4-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ae1c4-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="ae1c4-117">fakturaer</span><span class="sxs-lookup"><span data-stu-id="ae1c4-117">invoices</span></span>       | <span data-ttu-id="ae1c4-118">Fakturahoder i fritekst for CDS-kunde</span><span class="sxs-lookup"><span data-stu-id="ae1c4-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="ae1c4-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="ae1c4-119">invoicedetails</span></span> | <span data-ttu-id="ae1c4-120">Fakturalinjer i fritekst for CDS-kunde</span><span class="sxs-lookup"><span data-stu-id="ae1c4-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="ae1c4-121">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="ae1c4-121">Entity flow</span></span>

<span data-ttu-id="ae1c4-122">Fakturaer som opprettes fra en avtale i Field Service, kan synkroniseres til Finance and Operations via et Common Data Service (CDS)-dataintegreringsprosjekt.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="ae1c4-123">Oppdateringer av disse fakturaene synkroniseres til fritekstfakturaene i Finance and Operations hvis regnskapsstatusen for fritekstfakturaene er **Pågår**.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="ae1c4-124">Når fritekstfakturaene blir postert i Finance and Operations, og regnskapsstatusen oppdateres til **Fullført**, kan du ikke lenger synkronisere oppdateringer fra Field Service.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="ae1c4-125">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="ae1c4-125">Field Service CRM solution</span></span>

<span data-ttu-id="ae1c4-126">**Har linjer med avtaleopprinnelse**-feltet er lagt til i **Faktura**-enheten.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="ae1c4-127">Dette feltet kan garantere at bare fakturaer som opprettes fra en avtale, synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="ae1c4-128">Verdien er **sann** hvis fakturaen inneholder minst én fakturalinje som stammer fra en avtale.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="ae1c4-129">**Har avtaleopprinnelse**-feltet er lagt til i **Fakturalinje**-enheten.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="ae1c4-130">Dette feltet kan garantere at bare fakturalinjer som opprettes fra en avtale, synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="ae1c4-131">Verdien er **sann** hvis fakturalinjen stammer fra en avtale.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="ae1c4-132">**Fakturadato** er et obligatorisk felt i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="ae1c4-133">Feltet må derfor ha en verdi i Field Service før synkroniseringen utføres.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="ae1c4-134">For å imøtekomme dette kravet legges følgende logikk til:</span><span class="sxs-lookup"><span data-stu-id="ae1c4-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="ae1c4-135">Hvis **Fakturadato**-feltet er tomt på **Faktura**-enheten (det vil si hvis det ikke har en verdi), blir den satt til gjeldende dato når en fakturalinje som stammer fra en avtale, er lagt til.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="ae1c4-136">Brukeren kan endre **Fakturadato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="ae1c4-137">Men når brukeren prøver å lagre en faktura som stammer fra en avtale, får han eller hun en forretningsprosessfeil hvis **Fakturadato**-feltet er tomt på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="ae1c4-138">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="ae1c4-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="ae1c4-139">I Finance og Operations</span><span class="sxs-lookup"><span data-stu-id="ae1c4-139">In Finance and Operations</span></span>

<span data-ttu-id="ae1c4-140">En fakturaopprinnelse må være definert for integreringen for å skille fritekstfakturaene i Finance and Operations som er opprettet fra avtalefakturaer i Field Service.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="ae1c4-141">Når en faktura har en fakturaopprinnelse av typen **Integrering av avtalefaktura**, vises **Eksternt fakturanummer**-feltet i **Salgsfaktura**-hodet.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="ae1c4-142">I tillegg til å vises i fakturahodet, kan **Eksternt fakturanummer**-informasjonen brukes til å sikre at fakturaer som opprettes fra Field Service-avtalefakturaer blir filtrert ut under fakturasynkronisering fra Finance and Operations til Field Service.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="ae1c4-143">Gå til **Kunder** \> **Oppsett** \> **Opprinnelseskoder for faktura**.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="ae1c4-144">Velg **Ny** for å opprette en ny fakturaopprinnelse.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="ae1c4-145">I **Fakturaopprinnelige**-feltet angir du et navn for fakturaopprinnelsen, for eksempel **FS**.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="ae1c4-146">I **Beskrivelse**-feltet skriver du inn en beskrivelse, for eksempel **Avtalefakturaer i Field Service**.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="ae1c4-147">Merk av for **Tilordning av opprinnelsestype**.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="ae1c4-148">Sett **Opprinnelsestype for faktura**-feltet til **Integrering av avtalefaktura**.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="ae1c4-149">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="ae1c4-150">I dataintegrasjonsprosjektet</span><span class="sxs-lookup"><span data-stu-id="ae1c4-150">In the Data Integration project</span></span>

<span data-ttu-id="ae1c4-151">Oppgave: **Fakturalinjer**</span><span class="sxs-lookup"><span data-stu-id="ae1c4-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="ae1c4-152">Kontroller at standardverdien for Finance and Operations-feltet **Visningsverdi for hovedkonto** oppdateres for å samsvare med den ønskede verdien.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="ae1c4-153">Standardmalverdien er **401100**.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ae1c4-154">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="ae1c4-154">Template mapping in Data integration</span></span>

<span data-ttu-id="ae1c4-155">Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a><span data-ttu-id="ae1c4-156">Avtalefakturaer (Field Service til Fin and Ops): Fakturahoder</span><span class="sxs-lookup"><span data-stu-id="ae1c4-156">Agreement invoices (Field Service to Fin and Ops): Invoice headers</span></span>

<span data-ttu-id="ae1c4-157">[![Maltilordning i Dataintegrering](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="ae1c4-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a><span data-ttu-id="ae1c4-158">Avtalefakturaer (Field Service til Fin and Ops): Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="ae1c4-158">Agreement invoices (Field Service to Fin and Ops): Invoice lines</span></span>

<span data-ttu-id="ae1c4-159">[![Maltilordning i Dataintegrering](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="ae1c4-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>
