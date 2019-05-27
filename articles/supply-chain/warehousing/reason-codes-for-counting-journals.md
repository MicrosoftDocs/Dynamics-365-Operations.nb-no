---
title: Årsakskoder for lagertelling
description: Dette emnet beskriver hvordan du konfigurerer og bruker årsakskoder for tellingsoppgaver.
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f4332432ad73861cd9b6b6452685d3175ace56b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569412"
---
# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="9e5ae-103">Årsakskoder for lagertelling</span><span class="sxs-lookup"><span data-stu-id="9e5ae-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e5ae-104">Med årsakskoder kan du analysere resultatene av tellingen og eventuelle avvik som oppstår under denne prosessen.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="9e5ae-105">Du kan angi årsaken for å gjøre tellingen, for eksempel en skadet pall eller en lagerjustering som er basert på lagereksempler.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="9e5ae-106">Anbefaling</span><span class="sxs-lookup"><span data-stu-id="9e5ae-106">Recommendation</span></span>

<span data-ttu-id="9e5ae-107">Før du definerer systemet, anbefaler vi at du definerer en strategi for å arbeide med årsakskoder.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="9e5ae-108">Du kan for eksempel prøve å svare på følgende spørsmål:</span><span class="sxs-lookup"><span data-stu-id="9e5ae-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="9e5ae-109">Skal årsakskoder være obligatoriske på lagre?</span><span class="sxs-lookup"><span data-stu-id="9e5ae-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="9e5ae-110">Skal årsakskoder være obligatoriske eller valgfrie for noen varer?</span><span class="sxs-lookup"><span data-stu-id="9e5ae-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="9e5ae-111">Hvor mange årsakskoder trenger du?</span><span class="sxs-lookup"><span data-stu-id="9e5ae-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="9e5ae-112">Hvordan skal brukerne av strekkodeskannere bruke årsakskoder?</span><span class="sxs-lookup"><span data-stu-id="9e5ae-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="9e5ae-113">Skal årsakskodene være forhåndsvalgt, være obligatoriske eller ikke redigerbare?</span><span class="sxs-lookup"><span data-stu-id="9e5ae-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="9e5ae-114">Trenger lagermedarbeidere annen årsakskodevirkemåte på mobile skannere?</span><span class="sxs-lookup"><span data-stu-id="9e5ae-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="9e5ae-115">Hvis svaret er Ja, kan du opprette flere menyelementer og tilordne dem til forskjellige personer.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="9e5ae-116">Der bruke årsakskoder brukes</span><span class="sxs-lookup"><span data-stu-id="9e5ae-116">Where reason codes apply</span></span>

<span data-ttu-id="9e5ae-117">Du kan opprette flere årsakskodepolicyer, og hver årsakskodepolicy kan ha to årsakskodepolicyer for telling.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="9e5ae-118">Policyene for årsakskoder for telling kan brukes på lagernivå eller varenivå.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="9e5ae-119">Definere policyer for årsakskoder</span><span class="sxs-lookup"><span data-stu-id="9e5ae-119">Set up reason code policies</span></span>

1. <span data-ttu-id="9e5ae-120">Velg **Lagerstyring** \> **Oppsett** \> **Lager** \> **Årsakskodepolicyer for telling**, og opprett en ny policy for årsakskoder.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="9e5ae-121">I feltet **Årsakskodetype for telling** velger du **Obligatorisk** eller **Valgfritt** for å angi om valg av en årsakskode skal være en valgfri eller obligatorisk handling i én av følgende opptellingsjournaler:</span><span class="sxs-lookup"><span data-stu-id="9e5ae-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="9e5ae-122">Syklustelling (mobilenhet)</span><span class="sxs-lookup"><span data-stu-id="9e5ae-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="9e5ae-123">Spottelling (mobilenhet)</span><span class="sxs-lookup"><span data-stu-id="9e5ae-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="9e5ae-124">Terskeltelling (mobilenhet)</span><span class="sxs-lookup"><span data-stu-id="9e5ae-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="9e5ae-125">Justering inn (mobil enhet)</span><span class="sxs-lookup"><span data-stu-id="9e5ae-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="9e5ae-126">Justering ut (mobil enhet)</span><span class="sxs-lookup"><span data-stu-id="9e5ae-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="9e5ae-127">Opptellingsjournal (rik klient)</span><span class="sxs-lookup"><span data-stu-id="9e5ae-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="9e5ae-128">Du kan også definere årsakskoder for individuelle lagre og for produkter.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="9e5ae-129">Årsakskodeoppsettet for produkter kan se bort fra oppsettet for lagrene.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="9e5ae-130">Obligatoriske årsakskoder</span><span class="sxs-lookup"><span data-stu-id="9e5ae-130">Mandatory reason codes</span></span>

<span data-ttu-id="9e5ae-131">Hvis **Obligatorisk**-parameteren er angitt i konfigurasjonen av årsakskoder for lagre eller varer, kan ikke opptellingsjournalen fullføres og lukkes før en årsakskode er angitt.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="9e5ae-132">Definere årsakskoder for lagre</span><span class="sxs-lookup"><span data-stu-id="9e5ae-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="9e5ae-133">Velg **Lagerstyring** \> **Oppsett** \> **Lageroppdeling** \> **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="9e5ae-134">I **Lager**-kategorien i feltet **Årsakskodepolicy for telling**, velger du ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="9e5ae-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="9e5ae-135">**Tom** -parameteren som er definert for varen, brukes til å bestemme om opptellingsjournalene er obligatoriske for produktet.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="9e5ae-136">**Obligatorisk** – en årsakskode kreves alltid på opptellingsjournaler for lageret.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="9e5ae-137">**Valgfri** – en årsakskode kreves ikke på opptellingsjournaler for lageret.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="9e5ae-138">Definere årsakskoder for produkter</span><span class="sxs-lookup"><span data-stu-id="9e5ae-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="9e5ae-139">Velg **Behandling av produktinformasjon** \> **Produkter** \> **Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="9e5ae-140">I **Produkt**-kategorien velger du **Årsakskodepolicy for telling**, og deretter velger du ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="9e5ae-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="9e5ae-141">**Tom** -parameteren som er definert for lageret, brukes til å bestemme om opptellingsjournalene er obligatoriske for produktet.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="9e5ae-142">**Obligatorisk** – en årsakskode kreves alltid på opptellingsjournaler for produktet.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="9e5ae-143">Denne innstillingen overstyrer en årsakskodeinnstilling på lagernivå.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="9e5ae-144">**Valgfri** – en årsakskode kreves ikke på opptellingsjournaler for produktet.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="9e5ae-145">Denne innstillingen overstyrer en årsakskodeinnstilling på lagernivå.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="9e5ae-146">Bruke årsakskoder i opptellingsjournaler</span><span class="sxs-lookup"><span data-stu-id="9e5ae-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="9e5ae-147">I en opptellingsjournal kan du legge til årsakskoder for tellinger av følgende typer:</span><span class="sxs-lookup"><span data-stu-id="9e5ae-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="9e5ae-148">Syklustelling</span><span class="sxs-lookup"><span data-stu-id="9e5ae-148">Cycle Count</span></span>
- <span data-ttu-id="9e5ae-149">Spottelling</span><span class="sxs-lookup"><span data-stu-id="9e5ae-149">Spot Count</span></span>
- <span data-ttu-id="9e5ae-150">Terskeltelling</span><span class="sxs-lookup"><span data-stu-id="9e5ae-150">Threshold Count</span></span>
- <span data-ttu-id="9e5ae-151">Justering inn</span><span class="sxs-lookup"><span data-stu-id="9e5ae-151">Adjustment In</span></span>
- <span data-ttu-id="9e5ae-152">Justering ut</span><span class="sxs-lookup"><span data-stu-id="9e5ae-152">Adjustment Out</span></span>

<span data-ttu-id="9e5ae-153">Årsakskoder legges til i journallinjene i opptellingsjournaler av typen **Opptellingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="9e5ae-154">Velg **Lagerstyring** \> **Loggoppføringer** \> **Vareopptelling** \> **Opptelling**.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="9e5ae-155">I linjedetaljene i opptellingsjournalen i feltet **Årsakskode for telling**, velger du et alternativ.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="9e5ae-156">Vise historikken opptelling slik det er registrert etter årsakskoder</span><span class="sxs-lookup"><span data-stu-id="9e5ae-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="9e5ae-157">Velg **Lagerstyring** \> **Forespørsler og rapporter** \> **Opptellingslogg**, og deretter i **Årsakskode for telling**-feltet kan du vise opptellingsloggen som er registrert via en årsakskode.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="9e5ae-158">Bruke en årsakskode for en antallsjustering</span><span class="sxs-lookup"><span data-stu-id="9e5ae-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="9e5ae-159">På **Lagerbeholdning**-siden velger du **Juster antall**.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="9e5ae-160">Du kan åpne **Lagerbeholdning**-siden på flere måter.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="9e5ae-161">Velg for eksempel **Lagerstyring** \> **Forespørsler og rapporter** \> **Lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="9e5ae-162">Velg **Juster antall**, og deretter i **Årsakskode for telling**, velger en årsakskode.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="9e5ae-163">Konfigurere årsakskoder for menyelementer i mobilenheter</span><span class="sxs-lookup"><span data-stu-id="9e5ae-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="9e5ae-164">Du kan konfigurere årsakskoder for alle antall på et menyelement i en mobilenhet.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="9e5ae-165">Konfigurasjonen av menyelementet på mobilenheten omfatter følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="9e5ae-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="9e5ae-166">Om årsakskoden vises for mobilenhetsmedarbeideren under opptelling.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="9e5ae-167">Standard årsakskode som vises på et menyelement for mobilenhet.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="9e5ae-168">Om brukeren kan redigere årsakskoden.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="9e5ae-169">Definere årsakskoder på en mobilenhet</span><span class="sxs-lookup"><span data-stu-id="9e5ae-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="9e5ae-170">Velg **Lagerstyring** \> **Oppsett** \> **Mobilenhet** \> **Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="9e5ae-171">I kategorien **Syklustelling** velger **Syklustelling**.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="9e5ae-172">I feltet **Standard årsakskode for telling** angir du standard årsakskode som skal registreres når tellingen er utført, ved hjelp av menyelementet på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="9e5ae-173">I feltet **Vis årsakskode for telling** velger du **Linje** for å vise årsakskoden når hvert avvik er registrert.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="9e5ae-174">Velg eventuelt **Skjul** hvis ikke årsakskoden skal vises.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="9e5ae-175">Sett **Rediger årsakskode for telling** til **Ja** eller \*\*Ne\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="9e5ae-176">Hvis du setter dette alternativet til **Ja**, kan medarbeideren redigere årsakskoden når den vises på mobilenheten under opptelling.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="9e5ae-177">**Syklustelling**-knappen kan aktiveres på et menyelement for mobilenhet der telling kan utføres.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="9e5ae-178">Eksempel omfatter menyelementene for spottelling, brukerstyrt arbeid og systemstyrt arbeid.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="9e5ae-179">Godkjenninger av syklustelling</span><span class="sxs-lookup"><span data-stu-id="9e5ae-179">Cycle count approvals</span></span>

<span data-ttu-id="9e5ae-180">Før en telling er godkjent, kan brukeren endre årsakskoden som er knyttet til opptellingen.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="9e5ae-181">Når tellingen er godkjent, oppføres årsakskoden på opptellingsjournallinjene.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="9e5ae-182">Endre godkjenninger av syklustelling</span><span class="sxs-lookup"><span data-stu-id="9e5ae-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="9e5ae-183">Velg **Lagerstyring** \> **Syklustelling** \> **Syklustellingsarbeid venter på gjennomgang**.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="9e5ae-184">Velg **Syklustelling**, og deretter i **Årsakskode**-feltet, velger du en ny årsakskode.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="9e5ae-185">Endre menyelementet for mobilenhet for justering inn og justering ut</span><span class="sxs-lookup"><span data-stu-id="9e5ae-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="9e5ae-186">Velg **Lagerstyring** \> **Oppsett** \> **Mobilenhet** \> **Menyelementer på mobilenheten**, og velg deretter **Justering inn og ut**.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="9e5ae-187">Sett alternativet **Bruk eksisterende arbeid** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="9e5ae-188">I feltet **Arbeidsopprettelsesprosess** velger du **Justering inn**.</span><span class="sxs-lookup"><span data-stu-id="9e5ae-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="9e5ae-189">Følgende felt vil bli lagt til menyelementet for mobilenhet når **Justering inn** eller **Justering ut** er valgt under arbeidsopprettingen:</span><span class="sxs-lookup"><span data-stu-id="9e5ae-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="9e5ae-190">Standard årsakskode for telling</span><span class="sxs-lookup"><span data-stu-id="9e5ae-190">Default counting reason code</span></span>
- <span data-ttu-id="9e5ae-191">Vis årsakskode for telling</span><span class="sxs-lookup"><span data-stu-id="9e5ae-191">Display counting reason code</span></span>
- <span data-ttu-id="9e5ae-192">Rediger årsakskode for telling</span><span class="sxs-lookup"><span data-stu-id="9e5ae-192">Edit counting reason code</span></span>
