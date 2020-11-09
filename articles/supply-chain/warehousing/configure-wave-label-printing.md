---
title: Definere og bruke bølgeetikettutskrift
description: Dette emnet beskriver bølgeetikettutskrift og forklarer hvordan du konfigurerer den.
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: configure-wave-label-printing
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 1f51ed9f05caede3d4f320ddb6b705e67df9aa1f
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016961"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="5b3d0-103">Definere og bruke bølgeetikettutskrift</span><span class="sxs-lookup"><span data-stu-id="5b3d0-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b3d0-104">Bølgeetikettutskrift gir en alternativ tilnærming til etikettutskrift ved å introdusere en ny bølgetrinnmetode som lar deg opprette og skrive ut etiketter direkte fra bølgemalen under bølgekjøring.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="5b3d0-105">Etikettene vil derfor allerede være tilgjengelige før de ansatte kjører arbeidsordren på en mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="5b3d0-106">Arbeidere kan deretter knytte de nødvendige etikettene til under plukking i stedet for etter plukking.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="5b3d0-107">Bølgeetikettutskrift bruker Zebra Programming Language (ZPL) til å opprette etikettoppsett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="5b3d0-108">Et etikettoppsett er delt inn i tre inndelinger (topptekst, brødtekst og bunntekst) for å tillate etiketter som har gjentatt struktur.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="5b3d0-109">Maler for bølgeetiketter forteller systemet hvilket etikettoppsett som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="5b3d0-110">Brukere kan angi hvilken skriver som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-110">Users can specify which printer is used.</span></span> <span data-ttu-id="5b3d0-111">De kan også skrive ut etiketter på flere skrivere samtidig, i henhold til hva de trenger.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="5b3d0-112">Siden for **Bølgeetikettlogg** viser en oversikt over alle etiketter som er opprettet ved hjelp av dette oppsettet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="5b3d0-113">Du kan skrive ut og sortere etiketter basert på arbeidshoder, du kan skrive ut pauseetiketter per arbeidshode, og du kan skrive ut containerinnholdsetiketter, saksetiketter og andre lignende etiketter.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="5b3d0-114">Denne funksjonaliteten erstatter ikke eksisterende etikettutskriftsfunksjoner som er basert på dokumentruting.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="5b3d0-115">Bølgeetikettutskriftt gir følgende forbedringer:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="5b3d0-116">Skriv ut etiketter i henhold til antallet kartonger på én enkelt arbeidslinje, uten containerbruk.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="5b3d0-117">(En "kartong" er en enhet som er angitt på linjer for sekvensgrupper for enhet.)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="5b3d0-118">Skriv ut flere forskjellige etikettsekvenser (for eksempel kartong- og palletiketter).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="5b3d0-119">Inkluder etikettopplisting (for eksempel 1/124, 2/124, ... 124/124), og definer området for opplistingen (for eksempel arbeidslinje, lastlinje eller forsendelse).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="5b3d0-120">Opprett og skriv ut en fraktbrev-ID på etiketter før fraktbrevet genereres.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="5b3d0-121">Opprett en unik SSCC (serial shipping container code) for hver kartong, og ta den med på hver etikett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="5b3d0-122">Opprett GS1-kompatible nummerserier for fraktbrev-IDer og SSCCer.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="5b3d0-123">Skriv ut etiketter både fra mobile enheter og den rike klienten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="5b3d0-124">Annuller etiketter (for eksempel i scenarioer med plukk med mangler), og skrive dem ut på nytt.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="5b3d0-125">Rydde opp i bølgeetikettloggen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="5b3d0-126">Forbedringer i dokumentrutingsoppsett deles mellom dokumentrutingsoppsett og bølgeetikettoppsett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="5b3d0-127">(Hvis du vil ha mer informasjon, se [Dokumentrutingsoppsett for nummerskiltetiketter](../warehousing/document-routing-layout-for-license-plates.md).)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="5b3d0-128">Disse forbedringene gjør det mer effektivt å merke kartonger før lagring på paller.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="5b3d0-129">De er spesielt nyttige for firmaer som leverer til store forhandlere som bekrefter ordremottak automatisk ved å skanne hver kartong separat.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="5b3d0-130">Du kan implementere konfigurasjonsscenarioene som er beskrevet i dette emnet, enten separat eller i kombinasjon, avhengig av dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="5b3d0-131">Du kan utforme flere bølgeetikettmaler som fungerer i rekkefølge (som illustrert i scenario 3).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="5b3d0-132">Du kan for eksempel bruke scenario 1 til å skrive ut kartongetiketter og scenario 2 for å skrive ut palletiketter (hvis paller på lager varierer i størrelse og sammensetning).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="5b3d0-133">Aktivere funksjonen Bølgeetikettutskrift</span><span class="sxs-lookup"><span data-stu-id="5b3d0-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="5b3d0-134">Før du kan bruke *Bølgeetikettutskrift* -funksjonen, må den aktiveres i systemet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="5b3d0-135">Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="5b3d0-136">Funksjonen vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="5b3d0-137">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="5b3d0-138">**Funksjonsnavn:** *Bølgeetikettutskrift*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="5b3d0-139">Scenario 1: Bølgeetikettutskrift der det genereres en enkelt bølgeetikett</span><span class="sxs-lookup"><span data-stu-id="5b3d0-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="5b3d0-140">Dette scenariet viser hvordan et firma kan skrive ut forsendelsesetiketter for en stor forhandler som automatisk bekrefter ordremottak ved å skanne hver kartong separat.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="5b3d0-141">Dette scenariet viser ende-til-ende-flyten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="5b3d0-142">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="5b3d0-142">Make demo data available</span></span>

<span data-ttu-id="5b3d0-143">For å følge dette scenarioet må du ha demonstrasjonsdata installert, og du må velge den juridiske enheten **USMF**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="5b3d0-144">Kontrollere at bølgeetikettmetoden er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="5b3d0-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="5b3d0-145">Det kan hende du må generere metodene for bølgebehandling på nytt for å gjøre metoden for bølgeetikettutskrift tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="5b3d0-146">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgebehandlingsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="5b3d0-147">Bekreft at **waveLabelPrinting** er i listen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="5b3d0-148">Hvis den ikke er det, velger du **Generer metoder på nytt** i handlingsruten for å legge den til.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="5b3d0-149">Konfigurere en bølgemal</span><span class="sxs-lookup"><span data-stu-id="5b3d0-149">Configure a wave template</span></span>

<span data-ttu-id="5b3d0-150">Med bølgemaler kan du koble bestemte forekomster av bølgemetoder til en tilsvarende bølgeetikettmal.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="5b3d0-151">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="5b3d0-152">Velg en mal, for eksempel **62 Standardforsendelse**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="5b3d0-153">I hurtigfanen **Metoder** flytter du metoden **Bølgeetikettutskrift** til kolonnen **Valgte metoder**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="5b3d0-154">I kolonnen **Valgte metoder** velger du metoden **Bølgeetikettutskrift** og setter feltet **Bølgetrinnkode** til *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="5b3d0-155">For mer informasjon om bølgetrinnkoder, se [Bølgetrinnkoder](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="5b3d0-156">Opprette et oppsett for bølgeetikett</span><span class="sxs-lookup"><span data-stu-id="5b3d0-156">Create a wave label layout</span></span>

<span data-ttu-id="5b3d0-157">Etikettoppsettet kontrollerer hvilken informasjon som skrives ut på etiketten, og hvordan den er satt opp. Her angir du ZPL-koden som sendes til skriveren.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="5b3d0-158">Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Bølgeetikettoppsett**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="5b3d0-159">Opprett en post som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-160">**Etikettoppsett-ID:** *Kartong*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="5b3d0-161">**Beskrivelse:** *Kartong (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="5b3d0-162">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5b3d0-163">I handlingsruten velger du alternativet for **Radinnstillinger for bølgeetikett**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="5b3d0-164">Siden for **Radinnstillinger for bølgeetikett** vises.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="5b3d0-165">Her kan du konfigurere den dynamiske delen av etiketten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="5b3d0-166">Legg til en rad som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-167">**Rad-ID:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="5b3d0-168">**Navn på radtabell:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="5b3d0-169">**Startposisjon for rad:** *0*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="5b3d0-170">Dette feltet angir den loddrette plasseringen der raden vil begynne på etiketten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="5b3d0-171">**Radhøyde:** *0*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-171">**Row height:** *0*</span></span>

        <span data-ttu-id="5b3d0-172">Dette feltet definerer høyden på hver rad (i punkter) i henhold til ZPL-standarden.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="5b3d0-173">Radhøyden er positiv for vannrette etiketter og negativ for loddrette etiketter.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="5b3d0-174">Fordi det bare er én rad i dette eksemplet, kan du sette verdien til *0* (null).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="5b3d0-175">**Rader per side:** *1*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="5b3d0-176">Dette feltet definerer antallet rader som kan skrives ut på hver etikett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="5b3d0-177">Dette oppsettet vil føre til at det skrives ut en egen ZPL-etikett for hver post i bølgeetikettabellen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="5b3d0-178">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-178">Close the page.</span></span>
1. <span data-ttu-id="5b3d0-179">I handlingsruten velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="5b3d0-180">I dialogboksen for redigeringsprogrammet, i tabellen **Område** , legger du til en rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-181">**Tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-182">**Avledet tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-183">**Felt:** *Arbeidstype*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="5b3d0-184">**Kriterier:** *Plukk*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="5b3d0-185">Denne spørringen sikrer at bare arbeidslinjer av plukktypen blir skrevet ut på etiketten, ikke plasser-arbeidslinjer.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="5b3d0-186">Hvis du vil ha muligheten til å skrive ut fraktbrev-IDen, velger du kategorien **Sammenkoblinger** , velger tabellen **Arbeidslinjer** og kobler **Forsendelser** -tabellen til den.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="5b3d0-187">Lukk dialogboksen for redigeringsprogram for spørring.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="5b3d0-188">Hurtigfanen for **Skrivertekstoppsett** har tre inndelinger der du kan skrive skriverkode: **topptekstdelen** , **brødtekstdelen** og **bunntekstdelen**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="5b3d0-189">I **topptekstdelen** i feltet for **etikettopptekst** angir du koden for den nødvendige toppteksten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="5b3d0-190">Hvis du for eksempel bruker Zebra-skrivere, kan du bruke følgende kode.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="5b3d0-191">I **brødtekstdelen** i feltet for **etikettbrødtekst** angir du ZPL-kode for den nødvendige brødteksten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="5b3d0-192">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="5b3d0-193">I **brødtekstdelen** i feltet for **etikettbunntekst** angir du ZPL-kode for den nødvendige bunnteksten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="5b3d0-194">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="5b3d0-195">Dette oppsettet skriver bare ut én kopi av hver etikett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="5b3d0-196">Hvis du trenger flere kopier (for eksempel én kopi for hver side av pallen), setter du **n** -verdien for **\^PQn** -delen i bunnteskten til det nødvendige antallet eksemplarer.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="5b3d0-197">Hvis du for eksempel vil skrive ut fire eksemplarer av hver etikett, angir du **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="5b3d0-198">Etiketten er nå klar til bruk.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="5b3d0-199">Opprette en type bølgeetikett</span><span class="sxs-lookup"><span data-stu-id="5b3d0-199">Create a wave label type</span></span>

<span data-ttu-id="5b3d0-200">Bølgeetiketttyper brukes til å koble bølgeetikettmaler til en enhet på enhetssekvensgruppelinjer.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="5b3d0-201">Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Bølgeetiketttyper**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="5b3d0-202">Legg til bølgeetikettype som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-203">**Etikettype:** *Kartong*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="5b3d0-204">**Beskrivelse:** *Kartong*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="5b3d0-205">Konfigurer sekvensgrupper for enheter</span><span class="sxs-lookup"><span data-stu-id="5b3d0-205">Set up unit sequence groups</span></span>

<span data-ttu-id="5b3d0-206">Deretter definerer du enhetsseriegruppen for bølgeetikettypen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="5b3d0-207">Gå til **Lagerstyring \> Oppsett \> Lager \> Sekvensgrupper for enhet**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="5b3d0-208">Velg gruppen **Ea Box PL**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="5b3d0-209">For **Boks** angir du feltet **Bølgenivåtype** til *Kartong*.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="5b3d0-210">Opprette en mal for bølgeetikett</span><span class="sxs-lookup"><span data-stu-id="5b3d0-210">Create a wave label template</span></span>

<span data-ttu-id="5b3d0-211">Deretter oppretter du bølgeetikettmalen for bølgeetikettypen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="5b3d0-212">Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Maler for bølgeetiketter**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="5b3d0-213">Legg til en bølgenivåmal, og angi følgende verdier i toppteksten:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="5b3d0-214">**Etikettmalnavn:** *Kartongetiketter*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="5b3d0-215">**Beskrivelse:** *Kartongetiketter*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="5b3d0-216">**Bølgetrinnkode:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="5b3d0-217">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="5b3d0-218">I hurtigfanen **Generelt** angir du feltet **Bølgeetiketttype** -feltet til *Kartong*.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="5b3d0-219">I hurtigfanen for **Maldetaljer for bølgeetikett** legger du til en ny rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-220">**Etikettoppsett-ID:** *Kartong*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="5b3d0-221">**Skrivernavn:** Velg en passende ZPL-skriver.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="5b3d0-222">**Kjør spørring:** *Ja* (Denne innstillingen er valgfri, men anbefales for optimal ytelse.)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="5b3d0-223">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5b3d0-224">Valgfritt: Hvis du definerer en kundespesifikk etikettutforming, må du opprette en spørring for å finne kundens konto.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="5b3d0-225">På hurtigfanen **Maldetaljer for bølgeetikett** velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="5b3d0-226">Deretter, i dialoglogboksen for redigeringsprogrammet, i tabellen **Område** , legger du til en rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-227">**Tabell:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="5b3d0-228">**Avledet tabell:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="5b3d0-229">**Felt:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="5b3d0-230">**Kriterier:** Angi det aktuelle kundekontonummeret.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="5b3d0-231">Når du er ferdig, velger du **OK** for å lukke dialogboksen redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="5b3d0-232">I handlingsruten velger du **Rediger spørring** for å åpne dialogboksen for redigeringsprogrammet for spørringen for hele etikettmalen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="5b3d0-233">I dialogboksen for redigeringsprogrammet, i tabellen **Sortering** , legger du til en rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-234">**Tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-235">**Avledet tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-236">**Felt:** *Linje-ID for referanselast (post-ID)*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="5b3d0-237">**Søkeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="5b3d0-238">Velg **OK** for å lukke dialogboksen for redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="5b3d0-239">En meldingsboks ber deg bekrefte gjenopprettingsoperasjonen for gruppering.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="5b3d0-240">Klikk **Ja** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="5b3d0-241">Velg **Malgruppe for bølgeetikett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="5b3d0-242">I dialogboksen **Malgruppe for bølgeetikett** velger du raden der feltet **Referansefeltnavn** er satt til *Linje-ID for referanselast* , og deretter merker du av for **Etikettversjons-ID** for denne raden.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id* , and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5b3d0-243">Dette oppsettet vil opprette én etikettsekvens ("Kartong 1 av X") per lastlinje gjennom bølgen, uansett oppsett for arbeidsgruppering.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="5b3d0-244">Denne etikettsekvensen kan skrives ut på etikettoppsettet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="5b3d0-245">Konfigurere nummerserieutvidelser</span><span class="sxs-lookup"><span data-stu-id="5b3d0-245">Configure number sequence extensions</span></span>

<span data-ttu-id="5b3d0-246">Nummerserieutvidelser kontrollerer GS1-samsvar for bestemte nummerserier.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="5b3d0-247">Denne konfigurasjonen er valgfri for det gjeldende scenariet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="5b3d0-248">Du finner mer informasjon og konfigurasjonsinstruksjoner under [Konfigurere nummerserieutvidelser](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="5b3d0-249">Opprette en salgsordre og frigi den til lageret</span><span class="sxs-lookup"><span data-stu-id="5b3d0-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="5b3d0-250">Gå til **Salg og markedsføring \> Salgsordre \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="5b3d0-251">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-252">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5b3d0-253">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="5b3d0-254">Legg til to salgsordrelinjer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="5b3d0-255">Salgsordrelinje 1:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-255">Sales order line 1:</span></span>

        - <span data-ttu-id="5b3d0-256">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="5b3d0-257">**Antall:** *9024*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="5b3d0-258">**Enhet:** *ea* (9024 ea = 376 Box = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="5b3d0-259">Salgsordrelinje 2:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-259">Sales order line 2:</span></span>

        - <span data-ttu-id="5b3d0-260">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="5b3d0-261">**Antall:** *9016*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="5b3d0-262">**Enhet:** *ea* (9016 ea = 322 Box = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="5b3d0-263">Varene og antallene som beskrives her, er bare eksempler.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="5b3d0-264">De må bruke enhetsseriegruppen du definerte tidligere, riktige enhetskonverteringer fra *ea* til *Box* til *PL* må være definert for dem, og de må ha lager i lageret *62*.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="5b3d0-265">Hvis du vil ha mer informasjon, kan du se [Måleenhet og lagringspolicyer](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="5b3d0-266">Velg salgsordrelinjen 1.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-266">Select sales order line 1.</span></span> <span data-ttu-id="5b3d0-267">Deretter, i delen **Salgsordrelinje** på menyen **Lager** , velger du **Reservasjoner**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="5b3d0-268">På **Reservasjon** -siden i handlingsruten velger du **Reserver parti** , og deretter lukker du siden.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-268">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="5b3d0-269">Gjenta trinn 4 og 5 for salgsordrelinje 2.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="5b3d0-270">Velg **Frigi til lager** i kategorien **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="5b3d0-271">Følgende hendelser skjer:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-271">The following events occur:</span></span>

    - <span data-ttu-id="5b3d0-272">Systemet behandler den opprettede forsendelsen ved hjelp av malen som inneholder etikettutskriftstrinnet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="5b3d0-273">Etikettoppsettet blir brukt til å definere etikettens format, og resultatet blir en etikett som skrives ut på skriveren som er valgt i etikettmalen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="5b3d0-274">Bølgeetiketter genereres og skrives ut.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="5b3d0-275">Antallet etiketter vil tilsvare antallet kartonger (i dette eksemplet er 376 Box-etiketter for linje 1 og 322 Box-etiketter for linje 2).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="5b3d0-276">En ny fraktbrev-ID genereres for forsendelsene.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="5b3d0-277">Hvis du konfigurerte nummerserieutvidelsene, vil bølgeetikett-IDene følge **SSCC-18** -nummerformatet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="5b3d0-278">Du kan vise og skrive ut bølgeetiketter på nytt fra følgende sider.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="5b3d0-279">På handlingsruten for hver side, i kategorien **Forsendelser** i gruppen **Beslektet informasjon** , velger du **Bølgeetiketter**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="5b3d0-280">Alle forsendelser \> Forsendelsesdetaljer</span><span class="sxs-lookup"><span data-stu-id="5b3d0-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="5b3d0-281">Alle laster \> Lastdetaljer</span><span class="sxs-lookup"><span data-stu-id="5b3d0-281">All loads \> Load details</span></span>
- <span data-ttu-id="5b3d0-282">Alle bølger</span><span class="sxs-lookup"><span data-stu-id="5b3d0-282">All waves</span></span>
- <span data-ttu-id="5b3d0-283">Bølgeetiketter</span><span class="sxs-lookup"><span data-stu-id="5b3d0-283">Wave labels</span></span>
- <span data-ttu-id="5b3d0-284">Historikk for bølgeetikett</span><span class="sxs-lookup"><span data-stu-id="5b3d0-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="5b3d0-285">Scenario 2: Bølgeetikettutskrift for containerbruk (uten bølgeetikettposter)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="5b3d0-286">I dette scenariet kan du skrive ut bølgeetiketter ved containerbruk for automatisk å dele varer inn i kartonger, som dermed ikke krever en bølgeetikettpost.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="5b3d0-287">I dette tilfellet fungerer container-IDen som en plassholder for SSCC.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="5b3d0-288">Her er hovedforskjellen mellom dette scenariet og scenario 1:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="5b3d0-289">**Maler for bølgeetiketter:** Du velger ikke en bølgeetikettype på bølgeetikettmalen, og du trenger ikke en etikettversjonsgruppering.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="5b3d0-290">Ellers vil du konfigurere bølgeetikettmalen og koble til bølgemalen på samme måte som beskrevet i scenario 1.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="5b3d0-291">Du må la bølgeetikettypen være tom for å hindre at bølgeetiketter blir generert.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="5b3d0-292">**Oppsett av bølgeetiketter:** Du konfigurerer radinnstillingene for bølgeetikettoppsett for arbeidslinjer i stedet for bølgeetikettposter.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="5b3d0-293">Du må konfigurere radinnstillingen for etikettoppsettet ved hjelp av **WHSWorkLine** -tabellen i stedet for **WHSWaveLabel** -tabellen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="5b3d0-294">**Rader per side** -innstillingen kontrollerer antallet rader som brødtekstdelen vil ha.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="5b3d0-295">Denne konfigurasjonen egner seg også for forretningsscenarioer der flere ulike varer pakkes inn i én boks med etikett eller på en pall, og denne pakkeprosessen kan defineres av arbeidsopprettelsen (for eksempel arbeid som er gruppert etter forsendelse).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="5b3d0-296">Dette scenariet viser ende-til-ende-flyten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="5b3d0-297">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="5b3d0-297">Make demo data available</span></span>

<span data-ttu-id="5b3d0-298">For å følge dette scenarioet må du ha demonstrasjonsdata installert, og du må velge den juridiske enheten **USMF**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="5b3d0-299">Kontrollere at bølgeetikettmetoden er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="5b3d0-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="5b3d0-300">Det kan hende du må generere metodene for bølgebehandling på nytt for å gjøre metoden for bølgeetikettutskrift tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="5b3d0-301">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgebehandlingsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="5b3d0-302">Bekreft at **waveLabelPrinting** er i listen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="5b3d0-303">Hvis den ikke er det, velger du **Generer metoder på nytt** i handlingsruten for å legge den til.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="5b3d0-304">Definere en bølgemal</span><span class="sxs-lookup"><span data-stu-id="5b3d0-304">Set up a wave template</span></span>

<span data-ttu-id="5b3d0-305">Med bølgemaler kan du koble bestemte forekomster av bølgemetoder til en tilsvarende bølgeetikettmal.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="5b3d0-306">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="5b3d0-307">Velg en mal, for eksempel **63 Containerbruk**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="5b3d0-308">I hurtigfanen **Metoder** flytter du metoden **Bølgeetikettutskrift** til kolonnen **Valgte metoder**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="5b3d0-309">I kolonnen **Valgte metoder** velger du metoden **Bølgeetikettutskrift** og setter feltet **Bølgetrinnkode** til *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="5b3d0-310">For mer informasjon om bølgetrinnkoder, se [Bølgetrinnkoder](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="5b3d0-311">Opprette et oppsett for bølgeetikett</span><span class="sxs-lookup"><span data-stu-id="5b3d0-311">Create a wave label layout</span></span>

1. <span data-ttu-id="5b3d0-312">Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Bølgeetikettoppsett**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="5b3d0-313">Opprett en post som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-314">**Etikettoppsett-ID:** *Kartong*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="5b3d0-315">**Beskrivelse:** *Kartong (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="5b3d0-316">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5b3d0-317">I handlingsruten velger du alternativet for **Radinnstillinger for bølgeetikett**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="5b3d0-318">Siden for **Radinnstillinger for bølgeetikett** vises.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="5b3d0-319">Her kan du konfigurere den dynamiske delen av etiketten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="5b3d0-320">Legg til en rad som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-321">**Rad-ID:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="5b3d0-322">**Navn på radtabell:** *WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="5b3d0-323">**Startposisjon for rad:** *500*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="5b3d0-324">Dette feltet angir den loddrette plasseringen der raden vil begynne på etiketten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="5b3d0-325">**Radhøyde:** *-50*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="5b3d0-326">Dette feltet definerer høyden på hver rad.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-326">This field defines the height of each row.</span></span> <span data-ttu-id="5b3d0-327">Radhøyden er positiv for vannrette etiketter og negativ for loddrette etiketter.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="5b3d0-328">**Rader per side:** *5*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="5b3d0-329">Dette feltet definerer antallet rader som kan skrives ut på hver etikett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="5b3d0-330">Dette oppsettet vil skrive ut flere ZPL-etiketter per arbeid, der hver side kan inneholde opptil fem arbeidslinjer.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="5b3d0-331">Hvis for eksempel en etikett skrives ut for en container med 12 linjer, skrives tre etiketter ut.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="5b3d0-332">Hvis du vil skrive ut en egen etikett for hver plukklinje, setter du denne verdien til *1*.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="5b3d0-333">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-333">Close the page.</span></span>
1. <span data-ttu-id="5b3d0-334">I handlingsruten velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="5b3d0-335">I dialogboksen for redigeringsprogrammet, i tabellen **Område** , legger du til en rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-336">**Tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-337">**Avledet tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-338">**Felt:** *Arbeidstype*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="5b3d0-339">**Kriterier:** *Plukk*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="5b3d0-340">Hvis du vil ha muligheten til å skrive ut fraktbrev-IDen, velger du kategorien **Sammenkoblinger** , velger tabellen **Arbeidslinjer** og kobler **Forsendelser** -tabellen til den.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="5b3d0-341">Lukk dialogboksen for redigeringsprogram for spørring.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="5b3d0-342">Hurtigfanen for **Skrivertekstoppsett** har tre inndelinger der du kan skrive skriverkode: **topptekstdelen** , **brødtekstdelen** og **bunntekstdelen**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="5b3d0-343">I **topptekstdelen** i feltet for **etikettopptekst** angir du koden for den nødvendige toppteksten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="5b3d0-344">Hvis du for eksempel bruker Zebra-skrivere, kan du bruke følgende kode.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="5b3d0-345">I **brødtekstdelen** i feltet for **etikettbrødtekst** angir du ZPL-kode for den nødvendige brødteksten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="5b3d0-346">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="5b3d0-347">I **brødtekstdelen** i feltet for **etikettbunntekst** angir du ZPL-kode for den nødvendige bunnteksten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="5b3d0-348">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="5b3d0-349">Dette oppsettet skriver bare ut én kopi av hver etikett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="5b3d0-350">Hvis du trenger flere kopier (for eksempel én kopi for hver side av pallen), setter du **n** -verdien for **\^PQn** -delen i bunnteskten til det nødvendige antallet eksemplarer.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="5b3d0-351">Hvis du for eksempel vil skrive ut fire eksemplarer av hver etikett, angir du **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="5b3d0-352">Etiketten er nå klar til bruk.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="5b3d0-353">Opprette en mal for bølgeetikett</span><span class="sxs-lookup"><span data-stu-id="5b3d0-353">Create a wave label template</span></span>

1. <span data-ttu-id="5b3d0-354">Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Maler for bølgeetiketter**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="5b3d0-355">Legg til en bølgenivåmal, og angi følgende verdier i toppteksten:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="5b3d0-356">**Etikettmalnavn:** *Containeretiketter*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="5b3d0-357">**Beskrivelse:** *Containeretiketter*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="5b3d0-358">**Bølgetrinnkode:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="5b3d0-359">**Lager:** *63*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="5b3d0-360">I hurtigfanen for **Maldetaljer for bølgeetikett** legger du til en rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-361">**Etikettoppsett-ID:** *Container*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="5b3d0-362">**Skrivernavn:** Velg en passende ZPL-skriver.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="5b3d0-363">**Kjør spørring:** *Ja* (Denne innstillingen er valgfri, men anbefales for optimal ytelse.)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="5b3d0-364">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5b3d0-365">Valgfritt: Hvis du definerer en kundespesifikk etikettutforming, må du opprette en spørring for å finne kundens konto.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="5b3d0-366">På hurtigfanen **Maldetaljer for bølgeetikett** velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="5b3d0-367">Deretter, i dialoglogboksen for redigeringsprogrammet, i tabellen **Område** , legger du til en rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-368">**Tabell:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="5b3d0-369">**Avledet tabell:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="5b3d0-370">**Felt:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="5b3d0-371">**Kriterier:** Angi det aktuelle kundekontonummeret.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="5b3d0-372">Når du er ferdig, velger du **OK** for å lukke dialogboksen redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="5b3d0-373">Konfigurere nummerserieutvidelser</span><span class="sxs-lookup"><span data-stu-id="5b3d0-373">Configure number sequence extensions</span></span>

<span data-ttu-id="5b3d0-374">Nummerserieutvidelser kontrollerer GS1-samsvar for bestemte nummerserier.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="5b3d0-375">Denne konfigurasjonen er valgfri for det gjeldende scenariet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="5b3d0-376">Du finner mer informasjon og konfigurasjonsinstruksjoner under [Konfigurere nummerserieutvidelser](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="5b3d0-377">Opprette en salgsordre og frigi den til lageret</span><span class="sxs-lookup"><span data-stu-id="5b3d0-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="5b3d0-378">Gå til **Salg og markedsføring \> Salgsordre \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="5b3d0-379">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-380">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5b3d0-381">**Lager:** *63*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="5b3d0-382">Legg til fem salgsordrelinjer:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="5b3d0-383">Salgsordrelinje 1:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-383">Sales order line 1:</span></span>

        - <span data-ttu-id="5b3d0-384">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="5b3d0-385">**Antall:** *10*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="5b3d0-386">Salgsordrelinje 2:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-386">Sales order line 2:</span></span>

        - <span data-ttu-id="5b3d0-387">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="5b3d0-388">**Antall:** *20*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="5b3d0-389">Salgsordrelinje 3:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-389">Sales order line 3:</span></span>

        - <span data-ttu-id="5b3d0-390">**Varenummer:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="5b3d0-391">**Antall:** *20*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="5b3d0-392">Salgsordrelinje 4:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-392">Sales order line 4:</span></span>

        - <span data-ttu-id="5b3d0-393">**Varenummer:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="5b3d0-394">**Antall:** *40*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="5b3d0-395">Salgsordrelinje 5:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-395">Sales order line 5:</span></span>

        - <span data-ttu-id="5b3d0-396">**Varenummer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="5b3d0-397">**Antall:** *50*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="5b3d0-398">Varene og antallene som beskrives her, er bare eksempler.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="5b3d0-399">De må ha lager i det angitte lageret.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="5b3d0-400">Velg salgsordrelinjen 1.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-400">Select sales order line 1.</span></span> <span data-ttu-id="5b3d0-401">Deretter, i delen **Salgsordrelinje** på menyen **Lager** , velger du **Reservasjoner**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="5b3d0-402">På **Reservasjon** -siden i handlingsruten velger du **Reserver parti** , og deretter lukker du siden.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-402">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="5b3d0-403">Gjenta trinn 4 og 5 for hver ekstra salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="5b3d0-404">Velg **Frigi til lager** i kategorien **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="5b3d0-405">Følgende hendelser skjer:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-405">The following events occur:</span></span>

    - <span data-ttu-id="5b3d0-406">Systemet behandler den opprettede forsendelsen ved hjelp av malen som inneholder etikettutskriftstrinnet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="5b3d0-407">Etikettoppsettet blir brukt til å definere etikettens format, og sluttresultatet blir en etikett som har fem linjer og som skrives på skriveren som er valgt i etikettmalen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="5b3d0-408">En ny fraktbrev-ID genereres for forsendelsene.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="5b3d0-409">Hvis du konfigurerte nummerserieutvidelsene, vil bølgeetikett-IDene følge **SSCC-18** -nummerformatet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="5b3d0-410">Du kan skrive ut disse bølgeetikettene på nytt ved å gå til **Lagerstyring \> Forespørsler og rapporter \> Bølgeetikettlogg**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="5b3d0-411">Scenario 3: Utskrift av bølgeetiketter for etiketter med flere nivåer</span><span class="sxs-lookup"><span data-stu-id="5b3d0-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="5b3d0-412">Dette scenariet viser hvordan du bruker utskriftsfunksjonaliteten for bølgeetiketter når lagerprosessene krever flere nivåer av leveringsetiketter.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="5b3d0-413">Det kan for eksempel hende at separate etiketter må skrives ut for kartonger og paller, og en pauseetikett må kanskje skrives ut for en hel forsendelse.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="5b3d0-414">Pauseetiketter er en separat type etikett som kan brukes som en skiller mellom rulleringer og containere, for eksempel etiketter for forsendelses-IDen og en strekkode, slik at etikettene enkelt kan sorteres etter at de er skrevet ut.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="5b3d0-415">Hovedforskjellen mellom konfigurasjonen av dette scenariet og konfigurasjonen av scenario 1, i tillegg til at pauseetiketter aktiveres, er at flere bølgeetikettyper må knyttes til bølgeetikettmaler og linjer for sekvensgrupper for enhet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="5b3d0-416">Du kan oppnå denne konfigurasjonen ved å definere følgende elementer i dette scenariet:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="5b3d0-417">**Bølgebehandlingsmetoder:** Du merker bølgeetikettmetoden som "kan gjentas", legger den til to (eller flere) ganger til bølgemalen og angir ulike bølgetrinnkoder.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="5b3d0-418">**Maler for bølgeetiketter:** Du konfigurerer bølgeetikettmalene og kobler dem til bølgemalen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="5b3d0-419">Hver bølgeetikettmal har sin egen bølgeetikettype.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="5b3d0-420">**Bølgeetikettoppsett:** Du oppretter flere bølgeetikettoppsett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="5b3d0-421">Det vil være et separat etikettoppsett for hvert "lag" med etiketter, og det vil også være et pauseetikettoppsett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="5b3d0-422">Dette scenariet viser ende-til-ende-flyten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="5b3d0-423">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="5b3d0-423">Make demo data available</span></span>

<span data-ttu-id="5b3d0-424">For å følge dette scenarioet må du ha demonstrasjonsdata installert, og du må velge den juridiske enheten **USMF**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="5b3d0-425">Definere en metode for bølgeprosess</span><span class="sxs-lookup"><span data-stu-id="5b3d0-425">Set up a wave process method</span></span>

1. <span data-ttu-id="5b3d0-426">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgebehandlingsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="5b3d0-427">Bekreft at **waveLabelPrinting** er i listen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="5b3d0-428">Hvis den ikke er det, velger du **Generer metoder på nytt** i handlingsruten for å legge den til.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="5b3d0-429">For **waveLabelPrinting** -metoden merker du av for at **metoden kan gjentas**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="5b3d0-430">Definere en bølgemal</span><span class="sxs-lookup"><span data-stu-id="5b3d0-430">Set up a wave template</span></span>

1. <span data-ttu-id="5b3d0-431">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="5b3d0-432">Velg en mal, for eksempel **62 Standardforsendelse**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="5b3d0-433">I hurtigfanen **Metoder** flytter du metoden **Bølgeetikettutskrift** til kolonnen **Valgte metoder**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="5b3d0-434">I kolonnen **Valgte metoder** tilordner du verdien **Bølgetrinnkode** , for eksempel *Kartong* , til metoden **Bølgeetikettutskrift**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton* , to the **Wave label printing** method.</span></span> <span data-ttu-id="5b3d0-435">For mer informasjon om bølgetrinnkoder, se [Bølgetrinnkoder](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="5b3d0-436">Flytt metoden **Bølgeetikettutskrift** til kolonnen **Valgte metoder** enda en gang.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="5b3d0-437">I kolonnen **Valgte metoder** tilordner du en annen **Bølgetrinnkode** -verdi, for eksempel *Palle* , til den andre **Bølgeetikettutskrift** -metoden.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet* , to the second **Wave label printing** method.</span></span> <span data-ttu-id="5b3d0-438">For mer informasjon om bølgetrinnkoder, se [Bølgetrinnkoder](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="5b3d0-439">Opprette tre oppsett for bølgeetikett</span><span class="sxs-lookup"><span data-stu-id="5b3d0-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="5b3d0-440">Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Bølgeetikettoppsett**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="5b3d0-441">Opprett en post som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-442">**Etikettoppsett-ID:** *Kartong*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="5b3d0-443">**Beskrivelse:** *Kartong (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="5b3d0-444">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5b3d0-445">I handlingsruten velger du alternativet for **Radinnstillinger for bølgeetikett**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="5b3d0-446">Siden for **Radinnstillinger for bølgeetikett** vises.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="5b3d0-447">Her kan du konfigurere den dynamiske delen av etiketten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="5b3d0-448">Legg til en rad som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-449">**Rad-ID:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="5b3d0-450">**Navn på radtabell:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="5b3d0-451">**Startposisjon for rad:** *0*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="5b3d0-452">Dette feltet angir den loddrette plasseringen der raden vil begynne på etiketten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="5b3d0-453">**Radhøyde:** *0*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-453">**Row height:** *0*</span></span>

        <span data-ttu-id="5b3d0-454">Dette feltet definerer høyden på hver rad (i punkter) i henhold til ZPL-standarden.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="5b3d0-455">Radhøyden er positiv for vannrette etiketter og negativ for loddrette etiketter.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="5b3d0-456">Fordi det bare er én rad i dette eksemplet, kan du sette verdien til *0* (null).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="5b3d0-457">**Rader per side:** *1*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="5b3d0-458">Dette feltet definerer antallet rader som kan skrives ut på hver etikett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="5b3d0-459">Dette oppsettet vil føre til at det skrives ut en egen ZPL-etikett for hver post i bølgeetikettabellen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="5b3d0-460">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-460">Close the page.</span></span>
1. <span data-ttu-id="5b3d0-461">I handlingsruten velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="5b3d0-462">I dialogboksen for redigeringsprogrammet, i tabellen **Område** , legger du til en rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-463">**Tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-464">**Avledet tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-465">**Felt:** *Arbeidstype*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="5b3d0-466">**Kriterier:** *Plukk*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="5b3d0-467">Denne spørringen sikrer at bare arbeidslinjer av plukktypen blir skrevet ut på etiketten, ikke plasser-arbeidslinjer.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="5b3d0-468">Hvis du vil ha muligheten til å skrive ut fraktbrev-IDen, velger du kategorien **Sammenkoblinger** , velger tabellen **Arbeidslinjer** og kobler **Forsendelser** -tabellen til den.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="5b3d0-469">Lukk dialogboksen for redigeringsprogram for spørring.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="5b3d0-470">Hurtigfanen for **Skrivertekstoppsett** har tre inndelinger der du kan skrive skriverkode: **topptekstdelen** , **brødtekstdelen** og **bunntekstdelen**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="5b3d0-471">I **topptekstdelen** i feltet for **etikettopptekst** angir du koden for den nødvendige toppteksten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="5b3d0-472">Hvis du for eksempel bruker Zebra-skrivere, kan du bruke følgende kode.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="5b3d0-473">I **brødtekstdelen** i feltet for **etikettbrødtekst** angir du ZPL-kode for den nødvendige brødteksten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="5b3d0-474">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="5b3d0-475">I **brødtekstdelen** i feltet for **etikettbunntekst** angir du ZPL-kode for den nødvendige bunnteksten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="5b3d0-476">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="5b3d0-477">Dette oppsettet skriver bare ut én kopi av hver etikett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="5b3d0-478">Hvis du trenger flere kopier (for eksempel én kopi for hver side av pallen), setter du **n** -verdien for **\^PQn** -delen i bunnteskten til det nødvendige antallet eksemplarer.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="5b3d0-479">Hvis du for eksempel vil skrive ut fire eksemplarer av hver etikett, angir du **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="5b3d0-480">Den første etiketten er nå klar til bruk.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="5b3d0-481">Opprett en oppsettpost nummer to som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-482">**Etikettoppsett-ID:** *Pall*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="5b3d0-483">**Beskrivelse:** *Pall*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="5b3d0-484">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5b3d0-485">I handlingsruten velger du alternativet for **Radinnstillinger for bølgeetikett**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="5b3d0-486">Siden for **Radinnstillinger for bølgeetikett** vises.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="5b3d0-487">Her kan du konfigurere den dynamiske delen av etiketten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="5b3d0-488">Legg til en rad som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-489">**Rad-ID:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="5b3d0-490">**Navn på radtabell:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="5b3d0-491">**Startposisjon for rad:** *0*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="5b3d0-492">Dette feltet angir den loddrette plasseringen der raden vil begynne på etiketten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="5b3d0-493">**Radhøyde:** *0*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-493">**Row height:** *0*</span></span>

        <span data-ttu-id="5b3d0-494">Dette feltet definerer høyden på hver rad (i punkter) i henhold til ZPL-standarden.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="5b3d0-495">Radhøyden er positiv for vannrette etiketter og negativ for loddrette etiketter.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="5b3d0-496">Fordi det bare er én rad i dette eksemplet, kan du sette verdien til *0* (null).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="5b3d0-497">**Rader per side:** *1*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="5b3d0-498">Dette feltet definerer antallet rader som kan skrives ut på hver etikett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="5b3d0-499">Dette oppsettet fører til at det skrives ut en egen ZPL-etikett for hver post i bølgeetikettabellen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="5b3d0-500">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-500">Close the page.</span></span>
1. <span data-ttu-id="5b3d0-501">I handlingsruten velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="5b3d0-502">I dialogboksen for redigeringsprogrammet, i tabellen **Område** , legger du til en rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-503">**Tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-504">**Avledet tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-505">**Felt:** *Arbeidstype*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="5b3d0-506">**Kriterier:** *Plukk*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="5b3d0-507">Denne spørringen sikrer at bare arbeidslinjer av plukktypen blir skrevet ut på etiketten, ikke plasser-arbeidslinjer.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="5b3d0-508">Hvis du vil ha muligheten til å skrive ut fraktbrev-IDen, velger du kategorien **Sammenkoblinger** , velger tabellen **Arbeidslinjer** og kobler **Forsendelser** -tabellen til den.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="5b3d0-509">Lukk dialogboksen for redigeringsprogram for spørring.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="5b3d0-510">Hurtigfanen for **Skrivertekstoppsett** har tre inndelinger der du kan skrive skriverkode: **topptekstdelen** , **brødtekstdelen** og **bunntekstdelen**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="5b3d0-511">I **topptekstdelen** i feltet for **etikettopptekst** angir du koden for den nødvendige toppteksten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="5b3d0-512">Hvis du for eksempel bruker Zebra-skrivere, kan du bruke følgende kode.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="5b3d0-513">I **brødtekstdelen** i feltet for **etikettbrødtekst** angir du ZPL-kode for den nødvendige brødteksten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="5b3d0-514">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="5b3d0-515">I **brødtekstdelen** i feltet for **etikettbunntekst** angir du ZPL-kode for den nødvendige bunnteksten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="5b3d0-516">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="5b3d0-517">Dette oppsettet skriver bare ut én kopi av hver etikett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="5b3d0-518">Hvis du trenger flere kopier (for eksempel én kopi for hver side av pallen), setter du **n** -verdien for **\^PQn** -delen i bunnteskten til det nødvendige antallet eksemplarer.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="5b3d0-519">Hvis du for eksempel vil skrive ut fire eksemplarer av hver etikett, angir du **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="5b3d0-520">Den andre etiketten er nå klar til bruk.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="5b3d0-521">Opprett en tredje oppsettpost som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-522">**Etikettoppsett-ID:** *Pause*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="5b3d0-523">**Beskrivelse:** *Pauseetikett*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="5b3d0-524">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5b3d0-525">Hurtigfanen for **Skrivertekstoppsett** har tre inndelinger der du kan skrive skriverkode: **topptekstdelen** , **brødtekstdelen** og **bunntekstdelen**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="5b3d0-526">I **topptekstdelen** i feltet for **etikettopptekst** angir du ZPL-koden for den nødvendige toppteksten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="5b3d0-527">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="5b3d0-528">Denne gangen er ikke brødtekst nødvendig.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-528">This time, no body is required.</span></span> <span data-ttu-id="5b3d0-529">Skriv derfor bare inn den påkrevde teksten i **bunntekstdelen**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="5b3d0-530">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="5b3d0-531">Den tredje etiketten er nå klar til bruk.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5b3d0-532">Denne tredje etiketten er en pauseetikett som vil bli brukt som skille mellom etiketter.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="5b3d0-533">Opprette to bølgeetikettyper</span><span class="sxs-lookup"><span data-stu-id="5b3d0-533">Create two wave label types</span></span>

1. <span data-ttu-id="5b3d0-534">Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Bølgeetiketttyper**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="5b3d0-535">Opprett en post som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-536">**Etikettype:** *Kartong*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="5b3d0-537">**Beskrivelse:** *Kartong*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="5b3d0-538">Opprett en post nummer to som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-539">**Etikettype:** *Pall*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="5b3d0-540">**Beskrivelse:** *Pall*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="5b3d0-541">Konfigurer sekvensgrupper for enheter</span><span class="sxs-lookup"><span data-stu-id="5b3d0-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="5b3d0-542">Gå til **Lagerstyring \> Oppsett \> Lager \> Sekvensgrupper for enhet**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="5b3d0-543">Velg eller opprett en **EA Box pl** -gruppe.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="5b3d0-544">For **Boks** angir du feltet **Bølgenivåtype** til *Kartong*.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="5b3d0-545">For **PL** -linjen angir du feltet **Bølgenivåtype** til *Pall*.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="5b3d0-546">Opprette maler for bølgeetikett</span><span class="sxs-lookup"><span data-stu-id="5b3d0-546">Create wave label templates</span></span>

1. <span data-ttu-id="5b3d0-547">Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Maler for bølgeetiketter**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="5b3d0-548">Opprett en etikettmal som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-549">**Etikettmalnavn:** *Kartongetiketter*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="5b3d0-550">**Beskrivelse:** *Kartongetiketter*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="5b3d0-551">**Bølgetrinnkode:** *Kartong*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="5b3d0-552">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="5b3d0-553">På hurtigfanen **Generelt** , i feltet **Bølgeetiketttype** , velger du en verdi, for eksempel *Kartong*.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="5b3d0-554">I hurtigfanen for **Maldetaljer for bølgeetikett** legger du til en rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-555">**Etikettoppsett-ID:** *Kartong*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="5b3d0-556">**Skrivernavn:** Velg en passende ZPL-skriver.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="5b3d0-557">**Kjør spørring:** *Ja* (Denne innstillingen er valgfri, men anbefales for optimal ytelse.)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="5b3d0-558">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5b3d0-559">Valgfritt: Hvis du definerer en kundespesifikk etikettutforming, må du opprette en spørring for å finne kundens konto.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="5b3d0-560">På hurtigfanen **Maldetaljer for bølgeetikett** velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="5b3d0-561">Deretter, i dialoglogboksen for redigeringsprogrammet, i tabellen **Område** , legger du til en rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-562">**Tabell:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="5b3d0-563">**Avledet tabell:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="5b3d0-564">**Felt:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="5b3d0-565">**Kriterier:** Angi det aktuelle kundekontonummeret.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="5b3d0-566">Når du er ferdig, velger du **OK** for å lukke dialogboksen redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="5b3d0-567">I handlingsruten velger du **Rediger spørring** for å åpne dialogboksen for redigeringsprogrammet for spørringen for hele etikettmalen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="5b3d0-568">I dialogboksen for redigeringsprogrammet, i tabellen **Sortering** , legger du til en rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-569">**Tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-570">**Avledet tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-571">**Felt:** *Linje-ID for referanselast (post-ID)*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="5b3d0-572">**Søkeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="5b3d0-573">Legg til en rad nummer to som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-574">**Tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-575">**Avledet tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-576">**Felt:** *Leverings-ID*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="5b3d0-577">**Søkeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="5b3d0-578">Velg **OK** for å lukke dialogboksen for redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="5b3d0-579">En meldingsboks ber deg bekrefte gjenopprettingsoperasjonen for gruppering.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="5b3d0-580">Klikk **Ja** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="5b3d0-581">Velg **Malgruppe for bølgeetikett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="5b3d0-582">I dialogboksen for **Malgruppe for bølgeetikett** , for raden der feltet **Referansefeltnavn** er satt til *Forsendelses-ID* , angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID* , set the following values:</span></span>

    - <span data-ttu-id="5b3d0-583">**Skriv ut pauseetikett:** Merk av i denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="5b3d0-584">**Etikettoppsett-ID:** Velg en pauseetikett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="5b3d0-585">(Merk for eksempel av for *Pause* -etikettoppsettet som du opprettet tidligere i dette scenariet.)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="5b3d0-586">**Skrivernavn:** Velg skriveren for pauseetiketten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="5b3d0-587">(Vanligvis må du velge den samme skriveren som er valgt i hurtigfanen **Maldetaljer for bølgeetikett** , for å skille mellom etiketter.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="5b3d0-588">Det er imidlertid mulig å bruke andre scenarier.)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="5b3d0-589">For raden der feltet **Referansefeltnavn** er satt til *Linje-ID for referanselast* , merker du av for **Etikettversjons-ID**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-589">For the row where the **Reference field name** field is set to *Reference load line id* , select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5b3d0-590">Dette oppsettet vil opprette én etikettsekvens ("Kartong 1 av X") per lastlinje gjennom bølgen, uansett oppsett for arbeidsgruppering.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="5b3d0-591">Denne etikettsekvensen kan skrives ut på et etikettoppsettet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="5b3d0-592">I tillegg vil etiketter for forskjellige forsendelser skilles med den valgte pauseetiketten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="5b3d0-593">Velg **OK** for å lukke dialogboksen **Malgruppe for bølgeetikett**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="5b3d0-594">Opprett en etikettmal nummer to som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-595">**Etikettmalnavn:** *Palletiketter*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="5b3d0-596">**Beskrivelse:** *Palletiketter*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="5b3d0-597">**Bølgetrinnkode:** *Pall*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="5b3d0-598">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="5b3d0-599">På hurtigfanen **Generelt** , i feltet **Bølgeetiketttype** , velger du en verdi, for eksempel *Pall*.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="5b3d0-600">I hurtigfanen for **Maldetaljer for bølgeetikett** legger du til en rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-601">**Etikettoppsett-ID:** *Pall*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="5b3d0-602">**Skrivernavn:** Velg en passende ZPL-skriver.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="5b3d0-603">**Kjør spørring:** *Ja* (Denne innstillingen er valgfri, men anbefales for optimal ytelse.)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="5b3d0-604">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5b3d0-605">Valgfritt: Hvis du definerer en kundespesifikk etikettutforming, må du opprette en spørring for å finne kundens konto.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="5b3d0-606">På hurtigfanen **Maldetaljer for bølgeetikett** velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="5b3d0-607">Deretter, i dialoglogboksen for redigeringsprogrammet, i tabellen **Område** , legger du til en rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-608">**Tabell:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="5b3d0-609">**Avledet tabell:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="5b3d0-610">**Felt:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="5b3d0-611">**Kriterier:** Angi det aktuelle kundekontonummeret.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="5b3d0-612">Når du er ferdig, velger du **OK** for å lukke dialogboksen redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="5b3d0-613">I handlingsruten velger du **Rediger spørring** for å åpne dialogboksen for redigeringsprogrammet for spørringen for hele etikettmalen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="5b3d0-614">I dialogboksen for redigeringsprogrammet, i tabellen **Sortering** , legger du til en rad med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-615">**Tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-616">**Avledet tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-617">**Felt:** *Linje-ID for referanselast (post-ID)*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="5b3d0-618">**Søkeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="5b3d0-619">Legg til en rad nummer to som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-620">**Tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-621">**Avledet tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="5b3d0-622">**Felt:** *Leverings-ID*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="5b3d0-623">**Søkeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="5b3d0-624">Velg **OK** for å lukke dialogboksen for redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="5b3d0-625">En meldingsboks ber deg bekrefte gjenopprettingsoperasjonen for gruppering.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="5b3d0-626">Klikk **Ja** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="5b3d0-627">Velg **Malgruppe for bølgeetikett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="5b3d0-628">I dialogboksen for **Malgruppe for bølgeetikett** , for raden der feltet **Referansefeltnavn** er satt til *Forsendelses-ID* , angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID* , set the following values:</span></span>

    - <span data-ttu-id="5b3d0-629">**Skriv ut pauseetikett:** Merk av i denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="5b3d0-630">**Etikettoppsett-ID:** Velg en pauseetikett.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="5b3d0-631">(Merk for eksempel av for *Pause* -etikettoppsettet som du opprettet tidligere i dette scenariet.)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="5b3d0-632">**Skrivernavn:** Velg skriveren for pauseetiketten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="5b3d0-633">(Vanligvis må du velge den samme skriveren som er valgt i hurtigfanen **Maldetaljer for bølgeetikett** , for å skille mellom etiketter.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="5b3d0-634">Det er imidlertid mulig å bruke andre scenarier.)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="5b3d0-635">For raden der feltet **Referansefeltnavn** er satt til *Linje-ID for referanselast* , merker du av for **Etikettversjons-ID**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-635">For the row where the **Reference field name** field is set to *Reference load line id* , select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5b3d0-636">Dette oppsettet vil opprette én etikettsekvens ("Kartong 1 av X") per lastlinje gjennom bølgen, uansett oppsett for arbeidsgruppering.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="5b3d0-637">Denne etikettsekvensen kan skrives ut på et etikettoppsettet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="5b3d0-638">I tillegg vil etiketter for forskjellige forsendelser skilles med den valgte pauseetiketten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="5b3d0-639">Konfigurere nummerserieutvidelser</span><span class="sxs-lookup"><span data-stu-id="5b3d0-639">Configure number sequence extensions</span></span>

<span data-ttu-id="5b3d0-640">Nummerserieutvidelser kontrollerer GS1-samsvar for bestemte nummerserier.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="5b3d0-641">Denne konfigurasjonen er valgfri for det gjeldende scenariet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="5b3d0-642">Du finner mer informasjon og konfigurasjonsinstruksjoner under [Konfigurere nummerserieutvidelser](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="5b3d0-643">Opprette en salgsordre og frigi den til lageret</span><span class="sxs-lookup"><span data-stu-id="5b3d0-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="5b3d0-644">Gå til **Salg og markedsføring \> Salgsordre \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="5b3d0-645">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="5b3d0-646">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5b3d0-647">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="5b3d0-648">Legg til to salgsordrelinjer:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="5b3d0-649">Salgsordrelinje 1:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-649">Sales order line 1:</span></span>

        - <span data-ttu-id="5b3d0-650">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="5b3d0-651">**Antall:** *9024*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="5b3d0-652">**Enhet:** *ea* (9024 ea = 376 Box = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="5b3d0-653">Salgsordrelinje 2:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-653">Sales order line 2:</span></span>

        - <span data-ttu-id="5b3d0-654">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="5b3d0-655">**Antall:** *9016*</span><span class="sxs-lookup"><span data-stu-id="5b3d0-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="5b3d0-656">**Enhet:** *ea* (9016 ea = 322 Box = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="5b3d0-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="5b3d0-657">Varene og antallene som beskrives her, er bare eksempler.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="5b3d0-658">De må bruke enhetsseriegruppen du definerte tidligere, riktige enhetskonverteringer fra *ea* til *Box* til *PL* må være definert for dem, og de må ha lager i lageret *62*.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="5b3d0-659">Hvis du vil ha mer informasjon, kan du se [Måleenhet og lagringspolicyer](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="5b3d0-660">Velg salgsordrelinjen 1.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-660">Select sales order line 1.</span></span> <span data-ttu-id="5b3d0-661">Deretter, i delen **Salgsordrelinje** på menyen **Lager** , velger du **Reservasjoner**.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="5b3d0-662">På **Reservasjon** -siden i handlingsruten velger du **Reserver parti** , og deretter lukker du siden.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-662">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="5b3d0-663">Gjenta trinn 4 og 5 for salgsordrelinje 2.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="5b3d0-664">Velg **Frigi til lager** i kategorien **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="5b3d0-665">Følgende hendelser skjer:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-665">The following events occur:</span></span> 

    - <span data-ttu-id="5b3d0-666">Systemet behandler den opprettede forsendelsen ved hjelp av malen som inneholder etikettutskriftstrinnet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="5b3d0-667">Etikettoppsettet blir brukt til å definere etikettens format, og resultatet blir en etikett som skrives ut på skriveren som er valgt i etikettmalen.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="5b3d0-668">Bølgeetiketter genereres og skrives ut.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="5b3d0-669">Antallet etiketter vil tilsvare antallet kartonger (i dette eksemplet er 376 Box-etiketter for linje 1, 322 Box-etiketter for linje 2, 47 PL-etiketter for linje 1, 47 PL-etiketter for linje 2 og to pauseetiketter som har forsendelses-IDen).</span><span class="sxs-lookup"><span data-stu-id="5b3d0-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="5b3d0-670">En ny fraktbrev-ID genereres for forsendelsene.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="5b3d0-671">Hvis du konfigurerte nummerserieutvidelsene, vil bølgeetikett-IDene følge **SSCC-18** -nummerformatet.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="5b3d0-672">Du kan vise og skrive ut bølgeetiketter på nytt fra følgende sider:</span><span class="sxs-lookup"><span data-stu-id="5b3d0-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="5b3d0-673">Alle forsendelser \> Forsendelsesdetaljer</span><span class="sxs-lookup"><span data-stu-id="5b3d0-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="5b3d0-674">Alle laster \> Lastdetaljer</span><span class="sxs-lookup"><span data-stu-id="5b3d0-674">All loads \> Load details</span></span>
- <span data-ttu-id="5b3d0-675">Alle bølger</span><span class="sxs-lookup"><span data-stu-id="5b3d0-675">All waves</span></span>
- <span data-ttu-id="5b3d0-676">Bølgeetiketter</span><span class="sxs-lookup"><span data-stu-id="5b3d0-676">Wave labels</span></span>
- <span data-ttu-id="5b3d0-677">Historikk for bølgeetikett</span><span class="sxs-lookup"><span data-stu-id="5b3d0-677">Wave label history</span></span>

<span data-ttu-id="5b3d0-678">For de fleste av disse sidene kan du finne den relevante funksjonen ved å velge **Bølgeetiketter** i **Relatert informasjon** -gruppen i kategorien **Forsendelser** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b3d0-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>
