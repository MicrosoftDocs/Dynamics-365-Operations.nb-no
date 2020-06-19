---
title: Ferdigmelde fra jobbkortenheten
description: Dette emnet beskriver hvordan du konfigurerer systemet slik at brukere av en jobbkortenhet kan rapportere ferdige produkter fra en produksjonsordre til beholdning.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403268"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="8b7ff-103">Ferdigmelde fra jobbkortenheten</span><span class="sxs-lookup"><span data-stu-id="8b7ff-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b7ff-104">Arbeidere bruker **Rapporter fremdrift**-siden på jobbkortenheten til å rapportere antallet som er fullført for en produksjonsjobb.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="8b7ff-105">Kontrollere om antallene som ferdigmeldes, blir lagt til i beholdningen</span><span class="sxs-lookup"><span data-stu-id="8b7ff-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="8b7ff-106">Følg denne fremgangsmåten for å kontrollere hvorvidt og hvordan antallene som er rapportert som fullført for den siste operasjonen, skal legges til i beholdningen.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="8b7ff-107">Gå til **Produktkontroll \> Oppsett \> Produksjonsutførelse \> Standarder for produksjonsordre**.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="8b7ff-108">I **Ferdigmeld**-kategorien angir du en av følgende verdier for **Oppdater ferdig rapport online**-feltet:</span><span class="sxs-lookup"><span data-stu-id="8b7ff-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="8b7ff-109">**Nei** – ingen antall blir lagt til i beholdningen når antallene rapporteres ved siste operasjon.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="8b7ff-110">Statusen for produksjonsordren endres aldri.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="8b7ff-111">**Status + Antall** – Statusen for produksjonsordren endres til *Ferdigmeldt*, og antallet ferdigmeldes til beholdningen.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="8b7ff-112">**Antall** – Antallet rapporteres som fullført til beholdningen, men status for produksjonsordren endres aldri.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="8b7ff-113">**Status** – Bare statusen for produksjonsordren endres.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="8b7ff-114">Ingen antall blir lagt til i beholdningen når antallene rapporteres ved siste operasjon.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="8b7ff-115">Antall spores ikke i beholdningen hvis operasjonene de ferdigmeldes for, ikke er definert som siste operasjon.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="8b7ff-116">Disse antallene kan imidlertid brukes til å vise fremdriften.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="8b7ff-117">De kan også inkluderes i regler som kontrollerer om arbeidere kan starte neste operasjon før en definert terskel for rapporterte antall i den forrige operasjonen nås.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="8b7ff-118">Du kan definere disse reglene i **Antallsvalidering**-kategorien på **Standarder for produksjonsordre**-siden.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="8b7ff-119">Hvis du vil ha mer informasjon om hvordan du arbeider med **Standarder for produksjonsordre**-siden, kan du se [Produksjonsparametere i Produksjonsutførelse](production-parameters-manufacturing-execution.md).</span><span class="sxs-lookup"><span data-stu-id="8b7ff-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="8b7ff-120">Rapporter ferdigstillelse av partistyrte varer</span><span class="sxs-lookup"><span data-stu-id="8b7ff-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="8b7ff-121">Jobbkortenheten støtter tre scenarier for rapportering av partivise varer.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="8b7ff-122">Disse scenariene gjelder både for varer som er aktivert for avanserte lagerprosesser, og for varer som ikke er aktivert for avanserte lagerprosesser.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="8b7ff-123">**Manuelt tilordnede partinumre:** Arbeidere angir et egendefinert partinummer.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="8b7ff-124">Dette partinummeret kan komme fra en ekstern kilde som ikke er kjent for systemet.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="8b7ff-125">**Forhåndsdefinerte partinumre:** Arbeidere velger et partinummer fra en liste over partinumre som systemet automatisk genererer før produksjonsordren frigis til jobbkortenheten.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="8b7ff-126">**Faste partinumre:** Arbeidere verken angir eller velger et partinummer.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="8b7ff-127">I stedet tilordner systemet automatisk et partinummer til produksjonsordren før den frigis.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="8b7ff-128">Følg denne fremgangsmåten for å aktivere hvert enkelt scenario.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="8b7ff-129">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8b7ff-130">Velg produktet du vil konfigurere.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-130">Select the product to configure.</span></span>
1. <span data-ttu-id="8b7ff-131">I **Administrer lager**-hurtigkategorien, i **Partinummergruppe**-feltet velger du sporingsnummergruppen som er definert til å støtte scenariet.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="8b7ff-132">Hvis ingen partinummergruppe er tilordnet et partistyrt produkt, inneholder jobbkortenheten en standardløsning for manuell registrering av partinummer under ferdigmelding.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="8b7ff-133">Underdelene nedenfor beskriver hvordan du definerer sporingsnummergrupper for å støtte alle de tre scenariene for rapportering av partivise varer.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="8b7ff-134">Aktivere rapportering av partinummer på jobbkortenheten</span><span class="sxs-lookup"><span data-stu-id="8b7ff-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="8b7ff-135">Hvis du vil at jobbkortenhetene skal godta et partinummer under ferdigmelding, må du bruke [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere følgende funksjoner (i denne rekkefølgen):</span><span class="sxs-lookup"><span data-stu-id="8b7ff-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="8b7ff-136">Forbedret brukeropplevelse for dialogboksen Rapportfremdrift i jobbkortenheten.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="8b7ff-137">Aktiver angivelse av parti- og serienumre under ferdigrapportering fra jobbkortenheten (forhåndsvisning)</span><span class="sxs-lookup"><span data-stu-id="8b7ff-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="8b7ff-138">Konfigurere en sporingsnummergruppe som gjør at arbeiderne kan tilordne et partinummer manuelt</span><span class="sxs-lookup"><span data-stu-id="8b7ff-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="8b7ff-139">For å tillate manuelt tilordne partinumre følger du denne fremgangsmåten for å konfigurere en sporingsnummergruppe.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="8b7ff-140">Gå til **Lagerstyring \> Oppsett \> Dimensjoner \> Sporingsnummergrupper**.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="8b7ff-141">Opprette eller velge sporingsnummergruppen som skal konfigureres.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="8b7ff-142">På **Generelt**-hurtigfanen angir du **Manuelt**-alternativet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="8b7ff-143">![Siden med sporingsnummergrupper](media/tracking-number-group-manual.png "Siden med sporingsnummergrupper")</span><span class="sxs-lookup"><span data-stu-id="8b7ff-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="8b7ff-144">Angi andre verdier etter behov, og velg deretter denne sporingsnummergruppen som partinummergruppen for frigitte produkter som du vil bruke dette scenariet for.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="8b7ff-145">Når du bruker dette scenariet, er **Partinummer**-feltet som **Rapporter fremdrift**-siden på jobbkortenheten leverer, en tekstboks der arbeidere kan angi en hvilken som helst verdi.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="8b7ff-146">![Side med fremdriftsrapport med et felt for manuelle partinumre](media/job-card-device-batch-manual.png "Side med fremdriftsrapport med et felt for manuelle partinumre")</span><span class="sxs-lookup"><span data-stu-id="8b7ff-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="8b7ff-147">Konfigurere en sporingsnummergruppe som gir en liste over forhåndsdefinerte partinumre</span><span class="sxs-lookup"><span data-stu-id="8b7ff-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="8b7ff-148">For å generere en liste over forhåndsdefinerte partinumre følger du denne fremgangsmåten for å konfigurere en sporingsnummergruppe.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="8b7ff-149">Gå til **Lagerstyring \> Oppsett > Dimensjoner \> Sporingsnummergrupper**.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="8b7ff-150">Opprette eller velge sporingsnummergruppen som skal konfigureres.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="8b7ff-151">På **Generelt**-hurtigfanen angir du **Bare for lagertransaksjoner**-alternativet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="8b7ff-152">Bruk **Per antall**-feltet til å dele opp partinumre etter antall, basert på verdien du angir.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="8b7ff-153">Tenk deg at du har en produksjonsordre på ti stykker, og at **Per antall**-feltet er satt til *2*.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="8b7ff-154">I dette tilfellet blir fem partinumre tilordnet produksjonsordren når den opprettes.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="8b7ff-155">![Siden med sporingsnummergrupper](media/tracking-number-group-predefined.png "Siden med sporingsnummergrupper")</span><span class="sxs-lookup"><span data-stu-id="8b7ff-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="8b7ff-156">Angi andre verdier etter behov, og velg deretter denne sporingsnummergruppen som partinummergruppen for frigitte produkter som du vil bruke dette scenariet for.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="8b7ff-157">Når du bruker dette scenariet, er **Partinummer**-feltet som **Rapporter fremdrift**-siden på jobbkortenheten leverer, en rullegardinliste der arbeidere må velge en forhåndsdefinert verdi.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="8b7ff-158">![Side med fremdriftsrapport med en liste over forhåndsdefinerte partinumre](media/job-card-device-batch-predefined.png "Side med fremdriftsrapport med en liste over forhåndsdefinerte partinumre")</span><span class="sxs-lookup"><span data-stu-id="8b7ff-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="8b7ff-159">Konfigurere en sporingsnummergruppe som automatisk tilordner partinumre</span><span class="sxs-lookup"><span data-stu-id="8b7ff-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="8b7ff-160">Hvis partinumre skal tilordnes automatisk uten inndata fra ansatte, følger du denne fremgangsmåten for å konfigurere en sporingsnummergruppe.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="8b7ff-161">Gå til **Lagerstyring \> Oppsett \> Dimensjoner \> Sporingsnummergrupper**.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="8b7ff-162">Opprette eller velge sporingsnummergruppen som skal konfigureres.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="8b7ff-163">På **Generelt**-hurtigfanen angir du **Bare for lagertransaksjoner**-alternativet til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="8b7ff-164">Angi **Manuelt**-alternativet til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="8b7ff-165">![Siden med sporingsnummergrupper](media/tracking-number-group-fixed.png "Siden med sporingsnummergrupper")</span><span class="sxs-lookup"><span data-stu-id="8b7ff-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="8b7ff-166">Angi andre verdier etter behov, og velg deretter denne sporingsnummergruppen som partinummergruppen for frigitte produkter som du vil bruke dette scenariet for.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="8b7ff-167">Når du bruker dette scenariet, viser **Partinummer**-feltet som **Rapporter fremdrift**-siden på jobbkortenheten leverer, en verdi, men arbeiderne kan ikke redigere den.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="8b7ff-168">![Side med fremdriftsrapport med et fastsatt partinummer](media/job-card-device-batch-fixed.png "Side med fremdriftsrapport med et fastsatt partinummer")</span><span class="sxs-lookup"><span data-stu-id="8b7ff-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="8b7ff-169">Ferdigmeld til et nummerskilt</span><span class="sxs-lookup"><span data-stu-id="8b7ff-169">Report as finished to a license plate</span></span>

<span data-ttu-id="8b7ff-170">Avanserte lagerprosesser kan bruke nummerskiltdimensjonen til å spore beholdning på lagerlokasjoner som er definert for dette formålet.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="8b7ff-171">I dette tilfellet kreves skiltnummeret når en arbeider rapporterer antall som ferdigmeldt.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="8b7ff-172">Aktivere nummerskiltrapportering og etikettutskrifter</span><span class="sxs-lookup"><span data-stu-id="8b7ff-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="8b7ff-173">Hvis du vil bruke funksjonene som beskrives i denne delen, må du bruke [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) for å aktivere følgende funksjoner (i denne rekkefølgen):</span><span class="sxs-lookup"><span data-stu-id="8b7ff-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="8b7ff-174">Nummerskilt for ferdigmelding lagt til i jobbkortenheten</span><span class="sxs-lookup"><span data-stu-id="8b7ff-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="8b7ff-175">Aktiver automatisk generering av nummerskiltnummer ved ferdigrapportering i jobbkortenheten</span><span class="sxs-lookup"><span data-stu-id="8b7ff-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="8b7ff-176">Skriv ut etikett fra jobbkortenhet</span><span class="sxs-lookup"><span data-stu-id="8b7ff-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="8b7ff-177">Konfigurere ferdigmelding til et nummerskilt</span><span class="sxs-lookup"><span data-stu-id="8b7ff-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="8b7ff-178">Følg denne fremgangsmåten for å kontrollere om arbeidere bør gjenbruke et eksisterende nummerskilt eller generere et nytt nummerskilt når de ferdigmelder antall.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="8b7ff-179">Gå til **Produksjonskontroll \> Oppsett \> Produksjonsutførelse \> Konfigurer jobbkort for enheter**.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="8b7ff-180">Angi følgende alternativer for hver enhet:</span><span class="sxs-lookup"><span data-stu-id="8b7ff-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="8b7ff-181">**Generer nummerskilt** – sett dette alternativet til **Ja** for å generere et nytt nummerskilt for hver rapport som fullføres.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="8b7ff-182">Angi **Nei** hvis det skal brukes et eksisterende nummerskilt for hver ferdigmelding.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="8b7ff-183">**Skriv ut etikett** – sett dette alternativet til **Ja** hvis arbeideren må skrive ut en nummerskiltetikett for hver ferdigmelding.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="8b7ff-184">Angi **Nei** hvis det ikke kreves etiketter.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="8b7ff-185">![Side for konfigurasjon av jobbkort for enheter](media/config-job-card-raf.png "Side for konfigurasjon av jobbkort for enheter")</span><span class="sxs-lookup"><span data-stu-id="8b7ff-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="8b7ff-186">For å konfigurere etiketten går du til **Lagerstyring \> Oppsett \> Dokumentruting \> Dokumentruting**.</span><span class="sxs-lookup"><span data-stu-id="8b7ff-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="8b7ff-187">Hvis du vil ha mer informasjon, kan du se [Aktivere utskrift av nummerskiltetiketter](../warehousing/tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="8b7ff-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>
