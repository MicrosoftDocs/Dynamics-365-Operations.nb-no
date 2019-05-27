---
title: Definere og behandle gjentakende fakturaer
description: Denne artikkelen forklarer hvordan du konfigurerer og behandler gjentakende fakturaer. Du kan bruke gjentakende fakturaer hvis du må fakturere kunder for det samme beløpet regelmessig.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac9e836b0baa24c40554844ea4f3288b80e0c654
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571735"
---
# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="ab59f-104">Definere og behandle gjentakende fakturaer</span><span class="sxs-lookup"><span data-stu-id="ab59f-104">Set up and process recurring invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab59f-105">Denne artikkelen forklarer hvordan du konfigurerer og behandler gjentakende fakturaer.</span><span class="sxs-lookup"><span data-stu-id="ab59f-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="ab59f-106">Du kan bruke gjentakende fakturaer hvis du må fakturere kunder for det samme beløpet regelmessig.</span><span class="sxs-lookup"><span data-stu-id="ab59f-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

<a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="ab59f-107">Opprette en mal for gjentakende fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="ab59f-107">Create a recurring free text invoice template</span></span>
---------------------------------------------

<span data-ttu-id="ab59f-108">Hvis du vil fakturere kunder for de samme tjenestene med jevne mellomrom, må du definere en mal for fritekstfaktura som kan brukes på nytt til å opprette fakturaene.</span><span class="sxs-lookup"><span data-stu-id="ab59f-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="ab59f-109">Denne malen inneholder følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="ab59f-109">This template contains the following information:</span></span>

-   <span data-ttu-id="ab59f-110">Hodeinformasjon, for eksempel avgiftsgrupper, betalingsbetingelser og betalingsmåten</span><span class="sxs-lookup"><span data-stu-id="ab59f-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="ab59f-111">Linjeinformasjon, for eksempel tjenestebeskrivelse, inntektskontoer, enhetspris og fakturabeløp</span><span class="sxs-lookup"><span data-stu-id="ab59f-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="ab59f-112">Tillegg for levering eller håndtering</span><span class="sxs-lookup"><span data-stu-id="ab59f-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="ab59f-113">Regnskapsdistribusjoner sammen med informasjon om finansdimensjon, for eksempel kostsentre og forretningsenheter</span><span class="sxs-lookup"><span data-stu-id="ab59f-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="ab59f-114">Du oppretter i praksis en hel faktura og lagrer den som en mal.</span><span class="sxs-lookup"><span data-stu-id="ab59f-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="ab59f-115">Du kan definere malene ved hjelp av siden **Gjentakende fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="ab59f-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="ab59f-116">Tilordne en mal for fritekstfaktura til en kunde og angi gjentakelsesdetaljer</span><span class="sxs-lookup"><span data-stu-id="ab59f-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="ab59f-117">Når malen er opprettet, må du tilordne den til kundene du vil fakturere.</span><span class="sxs-lookup"><span data-stu-id="ab59f-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="ab59f-118">I tillegg må du angi når og hvor ofte fakturaen skal brukes.</span><span class="sxs-lookup"><span data-stu-id="ab59f-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="ab59f-119">Du kan tilordne malene i **Faktura**-fanen på **Kunder**-siden.</span><span class="sxs-lookup"><span data-stu-id="ab59f-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="ab59f-120">Legg til malen i listen, og oppdater følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="ab59f-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="ab59f-121">Startdatoen og eventuelt sluttdatoen for den gjentakende fakturaen</span><span class="sxs-lookup"><span data-stu-id="ab59f-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="ab59f-122">Frekvensen for den gjentakende faktureringen (for eksempel hver dag eller én gang i måneden)</span><span class="sxs-lookup"><span data-stu-id="ab59f-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="ab59f-123">Det maksimale faktureringsbeløpet (hvis denne informasjonen er nødvendig)</span><span class="sxs-lookup"><span data-stu-id="ab59f-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="ab59f-124">En kunde kan ha flere maler som har forskjellige frekvenser.</span><span class="sxs-lookup"><span data-stu-id="ab59f-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="ab59f-125">Generere gjentakende fakturaer</span><span class="sxs-lookup"><span data-stu-id="ab59f-125">Generate the recurring invoices</span></span>
<span data-ttu-id="ab59f-126">På siden **Gjentakende fakturaer**er det en oppgave som behandler maler for gjentakende faktura.</span><span class="sxs-lookup"><span data-stu-id="ab59f-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="ab59f-127">Du angir fakturadatoen og malen du vil generere fakturaer fra.</span><span class="sxs-lookup"><span data-stu-id="ab59f-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="ab59f-128">Fakturaer genereres og tilordnes ett gjentakende ID-nummer for hver gruppe med fakturaer som behandles.</span><span class="sxs-lookup"><span data-stu-id="ab59f-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>

<a name="post-recurring-free-text-invoices"></a><span data-ttu-id="ab59f-129">Postere gjentakende fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="ab59f-129">Post recurring free text invoices</span></span>
---------------------------------

<span data-ttu-id="ab59f-130">Når gjentakende fakturaer er generert, vises ID-ene for fakturagjentakelse i en posteringsoppgave på siden **Gjentakende fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="ab59f-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="ab59f-131">Du kan vise alle fakturaene for en gjentakelses- ID ved å klikke koblingen.</span><span class="sxs-lookup"><span data-stu-id="ab59f-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="ab59f-132">Du kan slette enkeltfakturaer under gjennomgangen av fakturaer for gjentakelses-ID-en.</span><span class="sxs-lookup"><span data-stu-id="ab59f-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="ab59f-133">Kundens innstillinger for gjentakelse tilbakestilles for denne malen, slik at den kan genereres på nytt senere.</span><span class="sxs-lookup"><span data-stu-id="ab59f-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="ab59f-134">Du kan postere én, mange eller alle fakturaer for en gjentakelses-ID.</span><span class="sxs-lookup"><span data-stu-id="ab59f-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="ab59f-135">Hvis arbeidsflyter er aktivert, må du klikke **Send** før du kan postere fakturaene.</span><span class="sxs-lookup"><span data-stu-id="ab59f-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>

<a name="print-recurring-free-text-invoices"></a><span data-ttu-id="ab59f-136">Skrive ut gjentakende fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="ab59f-136">Print recurring free text invoices</span></span>
----------------------------------

<span data-ttu-id="ab59f-137">Når gjentakende fakturaer er postert, kan du skrive ut fakturaene på listesiden for fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="ab59f-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="ab59f-138">Du kan skrive ut fakturaene som er valgt, eller du kan velge et område med fakturaer som skal skrives ut.</span><span class="sxs-lookup"><span data-stu-id="ab59f-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>



