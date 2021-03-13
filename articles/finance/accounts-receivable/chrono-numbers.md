---
title: Nummerere dokumenter og bilag kronologisk
description: Dette emnet beskriver hvordan du definerer og bruker kronologiske tall for dokumenter og tilknyttede bilag.
author: ikond
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 31745632de7339d167ac9f18f02e6611e1a78b28
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104422"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="fd030-103">Nummerere dokumenter og bilag kronologisk</span><span class="sxs-lookup"><span data-stu-id="fd030-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="fd030-104">I noen land er det et juridisk krav om å nummerere dokumenter og tilknyttede bilag i kronologisk rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="fd030-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="fd030-105">Kronologien må støttes av perioder.</span><span class="sxs-lookup"><span data-stu-id="fd030-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="fd030-106">Alle numrene som tilhører tidligere perioder, må være mindre enn numrene som tilhører senere perioder.</span><span class="sxs-lookup"><span data-stu-id="fd030-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="fd030-107">For å oppfylle dette kravet er kronologisk nummereringsfunksjonalitet implementert.</span><span class="sxs-lookup"><span data-stu-id="fd030-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="fd030-108">Dette emnet beskriver hvordan du konfigurerer og bruker kronologiske tall for dokumenter og tilknyttede bilag.</span><span class="sxs-lookup"><span data-stu-id="fd030-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fd030-109">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="fd030-109">Prerequisites</span></span>

<span data-ttu-id="fd030-110">I Funksjonsbehandling-arbeidsområdet slår du på funksjonen **Kronologisk nummerering**.</span><span class="sxs-lookup"><span data-stu-id="fd030-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="fd030-111">Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fd030-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="fd030-112">Konfigurere kronologisk nummerering</span><span class="sxs-lookup"><span data-stu-id="fd030-112">Configure chronological numbering</span></span>

<span data-ttu-id="fd030-113">Kronologisk nummerering påvirker følgende dokumenter.</span><span class="sxs-lookup"><span data-stu-id="fd030-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="fd030-114">**Kunde**</span><span class="sxs-lookup"><span data-stu-id="fd030-114">**Accounts receivable**</span></span>
- <span data-ttu-id="fd030-115">Kundefaktura</span><span class="sxs-lookup"><span data-stu-id="fd030-115">Customer invoice</span></span>
- <span data-ttu-id="fd030-116">Kundefakturabilag</span><span class="sxs-lookup"><span data-stu-id="fd030-116">Customer invoice voucher</span></span>
- <span data-ttu-id="fd030-117">Salgskreditnota</span><span class="sxs-lookup"><span data-stu-id="fd030-117">Sales credit note</span></span>
- <span data-ttu-id="fd030-118">Bilag for salgskreditnota</span><span class="sxs-lookup"><span data-stu-id="fd030-118">Sales credit note voucher</span></span>
- <span data-ttu-id="fd030-119">Fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="fd030-119">Free text invoice</span></span>
- <span data-ttu-id="fd030-120">Fritekstfakturabilag</span><span class="sxs-lookup"><span data-stu-id="fd030-120">Free text invoice voucher</span></span>
- <span data-ttu-id="fd030-121">Fritekstkreditnota</span><span class="sxs-lookup"><span data-stu-id="fd030-121">Free text credit note</span></span>
- <span data-ttu-id="fd030-122">Kreditnotabilag i fritekst</span><span class="sxs-lookup"><span data-stu-id="fd030-122">Free text credit note voucher</span></span>
- <span data-ttu-id="fd030-123">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="fd030-123">Packing slip</span></span>
- <span data-ttu-id="fd030-124">Følgeseddelbilag</span><span class="sxs-lookup"><span data-stu-id="fd030-124">Packing slip voucher</span></span>
- <span data-ttu-id="fd030-125">Korrigeringsbilag for følgeseddel</span><span class="sxs-lookup"><span data-stu-id="fd030-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="fd030-126">Rentenotabilag</span><span class="sxs-lookup"><span data-stu-id="fd030-126">Interest note voucher</span></span>
- <span data-ttu-id="fd030-127">Purringsbilag</span><span class="sxs-lookup"><span data-stu-id="fd030-127">Collection letter voucher</span></span>

<span data-ttu-id="fd030-128">**Leverandører**</span><span class="sxs-lookup"><span data-stu-id="fd030-128">**Accounts payable**</span></span>
- <span data-ttu-id="fd030-129">Fakturabilag</span><span class="sxs-lookup"><span data-stu-id="fd030-129">Invoice voucher</span></span>
- <span data-ttu-id="fd030-130">Kreditnotabilag</span><span class="sxs-lookup"><span data-stu-id="fd030-130">Credit note voucher</span></span>
- <span data-ttu-id="fd030-131">Mottaksseddelbilag</span><span class="sxs-lookup"><span data-stu-id="fd030-131">Product receipt voucher</span></span>

<span data-ttu-id="fd030-132">**Prosjektstyring**</span><span class="sxs-lookup"><span data-stu-id="fd030-132">**Project management**</span></span>
- <span data-ttu-id="fd030-133">Faktura</span><span class="sxs-lookup"><span data-stu-id="fd030-133">Invoice</span></span>
- <span data-ttu-id="fd030-134">Fakturabilag</span><span class="sxs-lookup"><span data-stu-id="fd030-134">Invoice voucher</span></span>
- <span data-ttu-id="fd030-135">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="fd030-135">Credit note</span></span>
- <span data-ttu-id="fd030-136">Kreditnotabilag</span><span class="sxs-lookup"><span data-stu-id="fd030-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="fd030-137">Definere nummerserier</span><span class="sxs-lookup"><span data-stu-id="fd030-137">Define number sequences</span></span>

<span data-ttu-id="fd030-138">Hvis du vil definere nummerserier, kan du gå til **Organisasjonsstyring** > **Nummerserier** > **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="fd030-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="fd030-139">Du kan definere så mange nummerserier som du trenger for å dekke de berørte periodene for nødvendige dokumenter.</span><span class="sxs-lookup"><span data-stu-id="fd030-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="fd030-140">Angi et selskap for hver nummerserie.</span><span class="sxs-lookup"><span data-stu-id="fd030-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="fd030-141">Segmentene i nummerseriene må defineres slik at de gir kronologisk rekkefølge for perioder.</span><span class="sxs-lookup"><span data-stu-id="fd030-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="fd030-142">Segmentnavnene kan for eksempel inneholde et spesielt prefiks som identifiserer en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="fd030-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Oppsett av nummerserier](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="fd030-144">Konfigurere nummerseriegrupper</span><span class="sxs-lookup"><span data-stu-id="fd030-144">Configure number sequence groups</span></span>

<span data-ttu-id="fd030-145">Hvis du vil konfigurere nummerseriegrupper, kan du gå til **Kunde** > **Oppsett** > **Kundeparametere**.</span><span class="sxs-lookup"><span data-stu-id="fd030-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="fd030-146">I kategorien **Nummerserier** definerer du så mange nummerseriegrupper som nødvendig for å dekke de berørte periodene.</span><span class="sxs-lookup"><span data-stu-id="fd030-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="fd030-147">For hver gruppe i **Referanse**-delen velger du en av dokumentreferansene som støttes, og i **Nummerseriekode**-feltet kan du se en nummerserie som ble opprettet tidligere for den tilknyttede perioden.</span><span class="sxs-lookup"><span data-stu-id="fd030-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Oppsett av nummerseriegruppe](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="fd030-149">På samme måte konfigurerer du nummerseriegrupper i modulene **Leverandør** og **Prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="fd030-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="fd030-150">Konfigurere kronologi for nummerseriegrupper</span><span class="sxs-lookup"><span data-stu-id="fd030-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="fd030-151">Hvis du vil konfigurere kronologi for nummerseriegrupper, kan du gå til **Organisasjonsstyring** > **Nummerserier** > **Kronologiske nummerseriegrupper**.</span><span class="sxs-lookup"><span data-stu-id="fd030-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="fd030-152">Definere anvendelsesvilkår for nummerseriegrupper.</span><span class="sxs-lookup"><span data-stu-id="fd030-152">Define the applicability conditions for number sequence groups.</span></span>

![Oppsett av kronologiske numre](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="fd030-154">Felt</span><span class="sxs-lookup"><span data-stu-id="fd030-154">Field</span></span>            | <span data-ttu-id="fd030-155">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fd030-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd030-156">Effektiv</span><span class="sxs-lookup"><span data-stu-id="fd030-156">Effective</span></span>  | <span data-ttu-id="fd030-157">Startdato for anvendelse av nummerseriegruppe.</span><span class="sxs-lookup"><span data-stu-id="fd030-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="fd030-158">Utløp</span><span class="sxs-lookup"><span data-stu-id="fd030-158">Expiration</span></span>      | <span data-ttu-id="fd030-159">Sluttdato for anvendelse av nummerseriegruppe.</span><span class="sxs-lookup"><span data-stu-id="fd030-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="fd030-160">Hvis ingen sluttdato brukes, velger du **Aldri**.</span><span class="sxs-lookup"><span data-stu-id="fd030-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="fd030-161">Nummerseriegruppe</span><span class="sxs-lookup"><span data-stu-id="fd030-161">Number sequence group</span></span> | <span data-ttu-id="fd030-162">Nummerseriegruppe som skal brukes til å generere dokumentnumre i løpet av perioden.</span><span class="sxs-lookup"><span data-stu-id="fd030-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="fd030-163">Opprinnelig nummerseriegruppe</span><span class="sxs-lookup"><span data-stu-id="fd030-163">Original number sequence group</span></span> | <span data-ttu-id="fd030-164">Denne nummerseriegruppekoden brukes for tilleggsfiltrering for tilfellene der dokumenter allerede har en bestemt *permanent* nummerseriegruppe tilordnet.</span><span class="sxs-lookup"><span data-stu-id="fd030-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="fd030-165">En tom verdi regnes som en spesifikk verdi.</span><span class="sxs-lookup"><span data-stu-id="fd030-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="fd030-166">Hvis du må ignorere en foreløpig tilordnet gruppe, bruker du **Standard**-alternativet for dette oppsettet.</span><span class="sxs-lookup"><span data-stu-id="fd030-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="fd030-167">Standard</span><span class="sxs-lookup"><span data-stu-id="fd030-167">Default</span></span> | <span data-ttu-id="fd030-168">Hvis den er aktivert, ignorerer systemet den midlertidig tilordnede dokumentnummerseriegruppen og bruker bare periodens start- og sluttdatoer til gjeldende analyse.</span><span class="sxs-lookup"><span data-stu-id="fd030-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="fd030-169">Hvis den er slått av, bruker systemet hele kombinasjonen **Gyldig** + **Utløp** + **Opprinnelig nummerseriegruppe** for valg.</span><span class="sxs-lookup"><span data-stu-id="fd030-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="fd030-170">Dokumentpostering</span><span class="sxs-lookup"><span data-stu-id="fd030-170">Document posting</span></span>
<span data-ttu-id="fd030-171">Når du posterer et dokument, tilordnes den riktige nummerseriegruppen til dokumentet, basert på dokumentets posteringsdato og brukes deretter til å generere et dokumentnummer basert på den oppdagete nummerserien.</span><span class="sxs-lookup"><span data-stu-id="fd030-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="fd030-172">Systemet gir en melding om tilordning av nummerseriegruppe.</span><span class="sxs-lookup"><span data-stu-id="fd030-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Dokumentnr.](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="fd030-174">I noen land er det allerede implementert en bestemt logikk for dokumentnummerering.</span><span class="sxs-lookup"><span data-stu-id="fd030-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="fd030-175">I dette tilfellet vil landspesifikk logikk overstyre funksjonen **Kronologisk nummerering**.</span><span class="sxs-lookup"><span data-stu-id="fd030-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>
