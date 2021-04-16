---
title: Nummerere dokumenter og bilag kronologisk
description: Dette emnet beskriver hvordan du definerer og bruker kronologiske tall for dokumenter og tilknyttede bilag.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: fe533052b0e5b04a7d27b954ba644761c631d6d7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838867"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="7d748-103">Nummerere dokumenter og bilag kronologisk</span><span class="sxs-lookup"><span data-stu-id="7d748-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7d748-104">I noen land er det et juridisk krav om å nummerere dokumenter og tilknyttede bilag i kronologisk rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="7d748-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="7d748-105">Kronologien må støttes av perioder.</span><span class="sxs-lookup"><span data-stu-id="7d748-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="7d748-106">Alle numrene som tilhører tidligere perioder, må være mindre enn numrene som tilhører senere perioder.</span><span class="sxs-lookup"><span data-stu-id="7d748-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="7d748-107">For å oppfylle dette kravet er kronologisk nummereringsfunksjonalitet implementert.</span><span class="sxs-lookup"><span data-stu-id="7d748-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="7d748-108">Dette emnet beskriver hvordan du konfigurerer og bruker kronologiske tall for dokumenter og tilknyttede bilag.</span><span class="sxs-lookup"><span data-stu-id="7d748-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7d748-109">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="7d748-109">Prerequisites</span></span>

<span data-ttu-id="7d748-110">I Funksjonsbehandling-arbeidsområdet slår du på funksjonen **Kronologisk nummerering**.</span><span class="sxs-lookup"><span data-stu-id="7d748-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="7d748-111">Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7d748-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="7d748-112">Konfigurere kronologisk nummerering</span><span class="sxs-lookup"><span data-stu-id="7d748-112">Configure chronological numbering</span></span>

<span data-ttu-id="7d748-113">Kronologisk nummerering påvirker følgende dokumenter.</span><span class="sxs-lookup"><span data-stu-id="7d748-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="7d748-114">**Kunde**</span><span class="sxs-lookup"><span data-stu-id="7d748-114">**Accounts receivable**</span></span>
- <span data-ttu-id="7d748-115">Kundefaktura</span><span class="sxs-lookup"><span data-stu-id="7d748-115">Customer invoice</span></span>
- <span data-ttu-id="7d748-116">Kundefakturabilag</span><span class="sxs-lookup"><span data-stu-id="7d748-116">Customer invoice voucher</span></span>
- <span data-ttu-id="7d748-117">Salgskreditnota</span><span class="sxs-lookup"><span data-stu-id="7d748-117">Sales credit note</span></span>
- <span data-ttu-id="7d748-118">Bilag for salgskreditnota</span><span class="sxs-lookup"><span data-stu-id="7d748-118">Sales credit note voucher</span></span>
- <span data-ttu-id="7d748-119">Fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="7d748-119">Free text invoice</span></span>
- <span data-ttu-id="7d748-120">Fritekstfakturabilag</span><span class="sxs-lookup"><span data-stu-id="7d748-120">Free text invoice voucher</span></span>
- <span data-ttu-id="7d748-121">Fritekstkreditnota</span><span class="sxs-lookup"><span data-stu-id="7d748-121">Free text credit note</span></span>
- <span data-ttu-id="7d748-122">Kreditnotabilag i fritekst</span><span class="sxs-lookup"><span data-stu-id="7d748-122">Free text credit note voucher</span></span>
- <span data-ttu-id="7d748-123">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="7d748-123">Packing slip</span></span>
- <span data-ttu-id="7d748-124">Følgeseddelbilag</span><span class="sxs-lookup"><span data-stu-id="7d748-124">Packing slip voucher</span></span>
- <span data-ttu-id="7d748-125">Korrigeringsbilag for følgeseddel</span><span class="sxs-lookup"><span data-stu-id="7d748-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="7d748-126">Rentenotabilag</span><span class="sxs-lookup"><span data-stu-id="7d748-126">Interest note voucher</span></span>
- <span data-ttu-id="7d748-127">Purringsbilag</span><span class="sxs-lookup"><span data-stu-id="7d748-127">Collection letter voucher</span></span>

<span data-ttu-id="7d748-128">**Leverandører**</span><span class="sxs-lookup"><span data-stu-id="7d748-128">**Accounts payable**</span></span>
- <span data-ttu-id="7d748-129">Fakturabilag</span><span class="sxs-lookup"><span data-stu-id="7d748-129">Invoice voucher</span></span>
- <span data-ttu-id="7d748-130">Kreditnotabilag</span><span class="sxs-lookup"><span data-stu-id="7d748-130">Credit note voucher</span></span>
- <span data-ttu-id="7d748-131">Mottaksseddelbilag</span><span class="sxs-lookup"><span data-stu-id="7d748-131">Product receipt voucher</span></span>

<span data-ttu-id="7d748-132">**Prosjektstyring**</span><span class="sxs-lookup"><span data-stu-id="7d748-132">**Project management**</span></span>
- <span data-ttu-id="7d748-133">Faktura</span><span class="sxs-lookup"><span data-stu-id="7d748-133">Invoice</span></span>
- <span data-ttu-id="7d748-134">Fakturabilag</span><span class="sxs-lookup"><span data-stu-id="7d748-134">Invoice voucher</span></span>
- <span data-ttu-id="7d748-135">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="7d748-135">Credit note</span></span>
- <span data-ttu-id="7d748-136">Kreditnotabilag</span><span class="sxs-lookup"><span data-stu-id="7d748-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="7d748-137">Definere nummerserier</span><span class="sxs-lookup"><span data-stu-id="7d748-137">Define number sequences</span></span>

<span data-ttu-id="7d748-138">Hvis du vil definere nummerserier, kan du gå til **Organisasjonsstyring** > **Nummerserier** > **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="7d748-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="7d748-139">Du kan definere så mange nummerserier som du trenger for å dekke de berørte periodene for nødvendige dokumenter.</span><span class="sxs-lookup"><span data-stu-id="7d748-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="7d748-140">Angi et selskap for hver nummerserie.</span><span class="sxs-lookup"><span data-stu-id="7d748-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="7d748-141">Segmentene i nummerseriene må defineres slik at de gir kronologisk rekkefølge for perioder.</span><span class="sxs-lookup"><span data-stu-id="7d748-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="7d748-142">Segmentnavnene kan for eksempel inneholde et spesielt prefiks som identifiserer en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="7d748-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Oppsett av nummerserier](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="7d748-144">Konfigurere nummerseriegrupper</span><span class="sxs-lookup"><span data-stu-id="7d748-144">Configure number sequence groups</span></span>

<span data-ttu-id="7d748-145">Hvis du vil konfigurere nummerseriegrupper, kan du gå til **Kunde** > **Oppsett** > **Kundeparametere**.</span><span class="sxs-lookup"><span data-stu-id="7d748-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="7d748-146">I kategorien **Nummerserier** definerer du så mange nummerseriegrupper som nødvendig for å dekke de berørte periodene.</span><span class="sxs-lookup"><span data-stu-id="7d748-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="7d748-147">For hver gruppe i **Referanse**-delen velger du en av dokumentreferansene som støttes, og i **Nummerseriekode**-feltet kan du se en nummerserie som ble opprettet tidligere for den tilknyttede perioden.</span><span class="sxs-lookup"><span data-stu-id="7d748-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Oppsett av nummerseriegruppe](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="7d748-149">På samme måte konfigurerer du nummerseriegrupper i modulene **Leverandør** og **Prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="7d748-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="7d748-150">Konfigurere kronologi for nummerseriegrupper</span><span class="sxs-lookup"><span data-stu-id="7d748-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="7d748-151">Hvis du vil konfigurere kronologi for nummerseriegrupper, kan du gå til **Organisasjonsstyring** > **Nummerserier** > **Kronologiske nummerseriegrupper**.</span><span class="sxs-lookup"><span data-stu-id="7d748-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="7d748-152">Definere anvendelsesvilkår for nummerseriegrupper.</span><span class="sxs-lookup"><span data-stu-id="7d748-152">Define the applicability conditions for number sequence groups.</span></span>

![Oppsett av kronologiske numre](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="7d748-154">Felt</span><span class="sxs-lookup"><span data-stu-id="7d748-154">Field</span></span>            | <span data-ttu-id="7d748-155">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="7d748-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d748-156">Effektiv</span><span class="sxs-lookup"><span data-stu-id="7d748-156">Effective</span></span>  | <span data-ttu-id="7d748-157">Startdato for anvendelse av nummerseriegruppe.</span><span class="sxs-lookup"><span data-stu-id="7d748-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="7d748-158">Utløp</span><span class="sxs-lookup"><span data-stu-id="7d748-158">Expiration</span></span>      | <span data-ttu-id="7d748-159">Sluttdato for anvendelse av nummerseriegruppe.</span><span class="sxs-lookup"><span data-stu-id="7d748-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="7d748-160">Hvis ingen sluttdato brukes, velger du **Aldri**.</span><span class="sxs-lookup"><span data-stu-id="7d748-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="7d748-161">Nummerseriegruppe</span><span class="sxs-lookup"><span data-stu-id="7d748-161">Number sequence group</span></span> | <span data-ttu-id="7d748-162">Nummerseriegruppe som skal brukes til å generere dokumentnumre i løpet av perioden.</span><span class="sxs-lookup"><span data-stu-id="7d748-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="7d748-163">Opprinnelig nummerseriegruppe</span><span class="sxs-lookup"><span data-stu-id="7d748-163">Original number sequence group</span></span> | <span data-ttu-id="7d748-164">Denne nummerseriegruppekoden brukes for tilleggsfiltrering for tilfellene der dokumenter allerede har en bestemt *permanent* nummerseriegruppe tilordnet.</span><span class="sxs-lookup"><span data-stu-id="7d748-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="7d748-165">En tom verdi regnes som en spesifikk verdi.</span><span class="sxs-lookup"><span data-stu-id="7d748-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="7d748-166">Hvis du må ignorere en foreløpig tilordnet gruppe, bruker du **Standard**-alternativet for dette oppsettet.</span><span class="sxs-lookup"><span data-stu-id="7d748-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="7d748-167">Standard</span><span class="sxs-lookup"><span data-stu-id="7d748-167">Default</span></span> | <span data-ttu-id="7d748-168">Hvis den er aktivert, ignorerer systemet den midlertidig tilordnede dokumentnummerseriegruppen og bruker bare periodens start- og sluttdatoer til gjeldende analyse.</span><span class="sxs-lookup"><span data-stu-id="7d748-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="7d748-169">Hvis den er slått av, bruker systemet hele kombinasjonen **Gyldig** + **Utløp** + **Opprinnelig nummerseriegruppe** for valg.</span><span class="sxs-lookup"><span data-stu-id="7d748-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="7d748-170">Dokumentpostering</span><span class="sxs-lookup"><span data-stu-id="7d748-170">Document posting</span></span>
<span data-ttu-id="7d748-171">Når du posterer et dokument, tilordnes den riktige nummerseriegruppen til dokumentet, basert på dokumentets posteringsdato og brukes deretter til å generere et dokumentnummer basert på den oppdagete nummerserien.</span><span class="sxs-lookup"><span data-stu-id="7d748-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="7d748-172">Systemet gir en melding om tilordning av nummerseriegruppe.</span><span class="sxs-lookup"><span data-stu-id="7d748-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Dokumentnr.](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="7d748-174">I noen land er det allerede implementert en bestemt logikk for dokumentnummerering.</span><span class="sxs-lookup"><span data-stu-id="7d748-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="7d748-175">I dette tilfellet vil landspesifikk logikk overstyre funksjonen **Kronologisk nummerering**.</span><span class="sxs-lookup"><span data-stu-id="7d748-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
