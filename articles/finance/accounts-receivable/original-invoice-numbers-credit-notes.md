---
title: Referanser til opprinnelige fakturaer i kreditnotaer
description: Dette emnet beskriver hvordan du definerer og skriver ut de opprinnelige fakturanumrene i tilknyttede kreditnotaer.
author: ilkond
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ce06a0ce4f2a308e1917ac2c7cbc66f0494a2ec5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811516"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="df1e7-103">Referanser til opprinnelige fakturaer i kreditnotaer</span><span class="sxs-lookup"><span data-stu-id="df1e7-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="df1e7-104">I noen land og områder er det et juridisk krav at utskrevne kreditnotaer inkluderer referanser til de opprinnelige fakturaene.</span><span class="sxs-lookup"><span data-stu-id="df1e7-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="df1e7-105">Dette emnet beskriver hvordan du definerer og skriver ut de opprinnelige fakturanumrene i tilknyttede kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="df1e7-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="df1e7-106">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="df1e7-106">Prerequisites</span></span>

- <span data-ttu-id="df1e7-107">I arbeidsområdet **Funksjonsbehandling** slår du på funksjonen for **Oppsett av fakturakreditering i salgs- og prosjektfakturarapporter**.</span><span class="sxs-lookup"><span data-stu-id="df1e7-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="df1e7-108">Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="df1e7-108">For more information, see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="df1e7-109">De utskriftsbare formatene for de nødvendige dokumentene må konfigureres i utskriftsbehandling.</span><span class="sxs-lookup"><span data-stu-id="df1e7-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="df1e7-110">Funksjonaliteten som er beskrevet i dette emnet, gjelder følgende dokumenter:</span><span class="sxs-lookup"><span data-stu-id="df1e7-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="df1e7-111">**Kunde**</span><span class="sxs-lookup"><span data-stu-id="df1e7-111">**Accounts receivable**</span></span>

- <span data-ttu-id="df1e7-112">Fritekstkreditnota</span><span class="sxs-lookup"><span data-stu-id="df1e7-112">Free text credit note</span></span>
- <span data-ttu-id="df1e7-113">Kundekreditnota</span><span class="sxs-lookup"><span data-stu-id="df1e7-113">Customer credit note</span></span>

<span data-ttu-id="df1e7-114">**Prosjektstyring og regnskap**</span><span class="sxs-lookup"><span data-stu-id="df1e7-114">**Project management and accounting**</span></span>

- <span data-ttu-id="df1e7-115">Prosjektkreditnota</span><span class="sxs-lookup"><span data-stu-id="df1e7-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="df1e7-116">Konfigurere kundeparametre</span><span class="sxs-lookup"><span data-stu-id="df1e7-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="df1e7-117">Følg denne fremgangsmåten for å angi parameteren som styrer om referanser til de opprinnelige fakturaene skal skrives ut i relaterte kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="df1e7-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="df1e7-118">Gå til **Kunder** \> **Oppsett** \> **Kundeparametere**.</span><span class="sxs-lookup"><span data-stu-id="df1e7-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="df1e7-119">I kategorien **Oppdateringer**, i hurtigfanen **Faktura**, angir du alternativet **Bruk oppsettet for kreditering av fakturering i salgs- og prosjektfakturarapporter** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="df1e7-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![Konfigurere kundeparametre](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="df1e7-121">Definere referanser til opprinnelige fakturaer</span><span class="sxs-lookup"><span data-stu-id="df1e7-121">Define references to original invoices</span></span>

<span data-ttu-id="df1e7-122">Bruk følgende fremgangsmåter til å definere referanser til opprinnelige fakturaer basert på dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="df1e7-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="df1e7-123">Fritekstkreditnota</span><span class="sxs-lookup"><span data-stu-id="df1e7-123">Free text credit note</span></span>

1. <span data-ttu-id="df1e7-124">Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="df1e7-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="df1e7-125">Opprett en ny kreditnota, eller velg en eksisterende kreditnota.</span><span class="sxs-lookup"><span data-stu-id="df1e7-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="df1e7-126">Åpne fakturaen.</span><span class="sxs-lookup"><span data-stu-id="df1e7-126">Open the invoice.</span></span>
4. <span data-ttu-id="df1e7-127">I handlingsruten, på **Faktura**-fanen i **Funksjoner**-gruppen, velger du **Krediter fakturering**.</span><span class="sxs-lookup"><span data-stu-id="df1e7-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="df1e7-128">Angi referansen til den opprinnelige fakturaen, og velg årsaken til rettelsen.</span><span class="sxs-lookup"><span data-stu-id="df1e7-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![Definere referansen for en fritekstfaktura](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="df1e7-130">Kundekreditnota</span><span class="sxs-lookup"><span data-stu-id="df1e7-130">Customer credit note</span></span>

1. <span data-ttu-id="df1e7-131">Gå til **Kunder** \> **Ordrer** \> **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="df1e7-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="df1e7-132">Velg og åpne den fakturerte salgsordren som må korrigeres.</span><span class="sxs-lookup"><span data-stu-id="df1e7-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="df1e7-133">I handlingsruten, på **Selg**-fanen i **Kreditnota**-gruppen, velger du **Kreditnota**.</span><span class="sxs-lookup"><span data-stu-id="df1e7-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="df1e7-134">Angi en årsak til korrigeringen.</span><span class="sxs-lookup"><span data-stu-id="df1e7-134">Enter the reason for the correction.</span></span> <span data-ttu-id="df1e7-135">Referansen til den opprinnelige fakturaen opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="df1e7-135">The reference to the original invoice is automatically established.</span></span>

![Definere referansen for en salgsordre](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="df1e7-137">Prosjektkreditnota</span><span class="sxs-lookup"><span data-stu-id="df1e7-137">Project credit note</span></span>

1. <span data-ttu-id="df1e7-138">Gå til **Prosjektstyring og regnskap** \> **Prosjektfakturaer** \> **Prosjektfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="df1e7-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="df1e7-139">Velg og åpne prosjektfakturaen som må korrigeres.</span><span class="sxs-lookup"><span data-stu-id="df1e7-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="df1e7-140">I handlingsruten, på **Prosjektfaktura**-fanen i **Funksjoner**-gruppen, velger du **Velg for kreditnota**.</span><span class="sxs-lookup"><span data-stu-id="df1e7-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="df1e7-141">Velg **Krediter fakturering**.</span><span class="sxs-lookup"><span data-stu-id="df1e7-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="df1e7-142">Angi en årsak til korrigeringen.</span><span class="sxs-lookup"><span data-stu-id="df1e7-142">Enter the reason for the correction.</span></span> <span data-ttu-id="df1e7-143">Referansen til den opprinnelige fakturaen opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="df1e7-143">The reference to the original invoice is automatically established.</span></span>

![Definere referansen for en prosjektfaktura](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="df1e7-145">Skrive ut kreditnotaer</span><span class="sxs-lookup"><span data-stu-id="df1e7-145">Printing credit notes</span></span>

<span data-ttu-id="df1e7-146">Når du skriver ut kreditnotaer for fritekst, kunde og prosjekt, inneholder de referansen til den opprinnelige fakturaen og rettelsesårsaken.</span><span class="sxs-lookup"><span data-stu-id="df1e7-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![Utskrevet kreditnota](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="df1e7-148">Pass på at de utskriftsbare formatene til dokumentene er riktig konfigurert, under forutsetning av at referanser til opprinnelige fakturaer blir skrevet ut.</span><span class="sxs-lookup"><span data-stu-id="df1e7-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
