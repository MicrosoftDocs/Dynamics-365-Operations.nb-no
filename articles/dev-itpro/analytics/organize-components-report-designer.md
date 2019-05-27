---
title: Organisere rapportkomponenter i rapportutforming
description: Når du har utformet byggeblokker og genererte rapporter, er det nyttig å organisere disse objektene slik at de blir enklere for brukerne å finne. Denne artikkelen beskriver hvordan du organiserer eksisterende rapporter, byggeblokker og objekter i rapportutforming.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3f2b34cccfd84a9e4bb76e7a1da64e5cefa9982e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551749"
---
# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="694be-104">Organisere rapportkomponenter i rapportutforming</span><span class="sxs-lookup"><span data-stu-id="694be-104">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="694be-105">Når du har utformet byggeblokker og genererte rapporter, er det nyttig å organisere disse objektene slik at de blir enklere for brukerne å finne.</span><span class="sxs-lookup"><span data-stu-id="694be-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="694be-106">Denne artikkelen beskriver hvordan du organiserer eksisterende rapporter, byggeblokker og objekter i rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="694be-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="694be-107">Du kan gi nytt navn til mapper, rapporter, byggeblokker og andre objekter i rapportutforming, for å bidra til å organisere filene dine.</span><span class="sxs-lookup"><span data-stu-id="694be-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="694be-108">Avhengig av hvilken type objekt du gir nytt navn, må du kanskje oppdatere tilknytninger til dette objektet.</span><span class="sxs-lookup"><span data-stu-id="694be-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="694be-109">Gi nytt navn til en mappe eller byggeblokk i Rapportutforming</span><span class="sxs-lookup"><span data-stu-id="694be-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="694be-110">I Rapportutforming kan du gi nytt navn til mapper, rapportdefinisjoner, raddefinisjoner, kolonnedefinisjoner og rapporteringstredefinisjoner.</span><span class="sxs-lookup"><span data-stu-id="694be-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="694be-111">Gi nytt navn til en mappe eller byggeblokk i Rapportutforming</span><span class="sxs-lookup"><span data-stu-id="694be-111">Rename a folder or building block in Report Designer</span></span>

1. <span data-ttu-id="694be-112">Bruk navigasjonsruten i Rapportutforming til å finne mappen eller objektet som skal gis nytt navn.</span><span class="sxs-lookup"><span data-stu-id="694be-112">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2. <span data-ttu-id="694be-113">Høyreklikk mappen eller objektet, og klikk deretter **Gi nytt navn**.</span><span class="sxs-lookup"><span data-stu-id="694be-113">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="694be-114">**Navn**-feltet i navigasjonsruten blir tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="694be-114">The **Name** field in the navigation pane becomes available.</span></span>
3. <span data-ttu-id="694be-115">Skriv inn et nytt navn, og trykk deretter Enter.</span><span class="sxs-lookup"><span data-stu-id="694be-115">Type a new name, and then press Enter.</span></span>
4. <span data-ttu-id="694be-116">Hvis byggeblokken er en raddefinisjon, kolonnedefinisjon eller rapporteringstredefinisjon, må du oppdatere andre byggeblokker som er knyttet til det.</span><span class="sxs-lookup"><span data-stu-id="694be-116">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="694be-117">Høyreklikk byggeblokken du ga nytt navn i trinn 3, velg **Tilknytninger** og velg deretter et element i listen for å oppdatere det.</span><span class="sxs-lookup"><span data-stu-id="694be-117">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5. <span data-ttu-id="694be-118">Gjenta trinn 4 til alle tilknyttede elementer er oppdaterte.</span><span class="sxs-lookup"><span data-stu-id="694be-118">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="694be-119">Opprette og administrere rapportgrupper.</span><span class="sxs-lookup"><span data-stu-id="694be-119">Create and manage report groups</span></span>
<span data-ttu-id="694be-120">Du kan gruppere rapportdefinisjoner for å generere flere rapporter samtidig.</span><span class="sxs-lookup"><span data-stu-id="694be-120">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="694be-121">Hvis du vil opprette, endre, slette og generere rapportgrupper, må du ha rolle som utformer eller administrator.</span><span class="sxs-lookup"><span data-stu-id="694be-121">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="694be-122">Brukere som har generatorrollen kan generere rapportgrupper og kan også endre innstillingen for brukerrapportdefinisjonene for rapportgrupper.</span><span class="sxs-lookup"><span data-stu-id="694be-122">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="694be-123">Opprette en rapportgruppe</span><span class="sxs-lookup"><span data-stu-id="694be-123">Create a report group</span></span>

1. <span data-ttu-id="694be-124">Klikk **Rapportgrupper** i navigasjonsruten i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="694be-124">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="694be-125">På **Fil**-menhyen klikker du **Ny** &gt; **Rapportgruppedefinisjon** for å åpne en ny rapportgruppe i visningsvinduet.</span><span class="sxs-lookup"><span data-stu-id="694be-125">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="694be-126">Du kan også klikke **Rapportgruppe**-knappen ![Rapportgruppe](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Rapportgruppe") på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="694be-126">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3. <span data-ttu-id="694be-127">Klikk kategorien **Rapportgruppe**. For å overstyre informasjonen om de enkelte rapportdefinisjonene for genereringen av denne rapporten, merker du av for **Overstyr selskap, detalj og datoinnstillinger fra de enkelte rapportdefinisjonene**.</span><span class="sxs-lookup"><span data-stu-id="694be-127">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="694be-128">Innstillingene for firmanavnet, detaljnivået, provisorisk og datoinformasjon, fylles ut automatisk, men du kan foreta oppdateringer.</span><span class="sxs-lookup"><span data-stu-id="694be-128">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4. <span data-ttu-id="694be-129">Hvis du vil generere flere rapporter som viser rapporteringsvalutaene, merker du av for **Inkluder alle rapporteringsvalutaer**.</span><span class="sxs-lookup"><span data-stu-id="694be-129">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="694be-130">Du kan deretter gå til flere visninger ved å klikke **Valuta** i webvisningen når du viser rapporten.</span><span class="sxs-lookup"><span data-stu-id="694be-130">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5. <span data-ttu-id="694be-131">I feltet **Rapporter i gruppen** klikker du **Legg til** for å velge rapportene som skal tas med i rapportgruppen.</span><span class="sxs-lookup"><span data-stu-id="694be-131">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="694be-132">Hvis du vil velge flere rapporter i dialogboksen **Legg til**, holder du nede CTRL-tasten mens du merker rapporter.</span><span class="sxs-lookup"><span data-stu-id="694be-132">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="694be-133">Når du er ferdig med å velge rapporter, klikker du **OK**.</span><span class="sxs-lookup"><span data-stu-id="694be-133">When you've finished selecting reports, click **OK**.</span></span>
6. <span data-ttu-id="694be-134">Klikk **Fil** &gt; **Lagre** for å lagre den nye rapportgruppen.</span><span class="sxs-lookup"><span data-stu-id="694be-134">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="694be-135">Endre en rapportgruppe</span><span class="sxs-lookup"><span data-stu-id="694be-135">Modify a report group</span></span>

1. <span data-ttu-id="694be-136">Klikk **Rapportgrupper** i navigasjonsruten i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="694be-136">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="694be-137">Dobbeltklikk rapportgruppen du vil endre.</span><span class="sxs-lookup"><span data-stu-id="694be-137">Double-click the report group to modify.</span></span>
3. <span data-ttu-id="694be-138">I kategorien **Rapportgruppe** gjør du de ønskede endringene.</span><span class="sxs-lookup"><span data-stu-id="694be-138">On the **Report Group** tab, make the changes that you want.</span></span>
4. <span data-ttu-id="694be-139">På **Fil**-menyen klikker du **Lagre** for å lagre den endrede rapportgruppen. Du kan også klikke **Lagre**-knappen ![Lagre](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Lagre") på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="694be-139">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

> <span data-ttu-id="694be-140">[OBS!] Hvis du har planlagt rapporter slik at de genereres med jevne mellomrom, kan du overstyre disse innstillingene og generere en rapport umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="694be-140">[NOTE] If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="694be-141">Generere en rapport for en rapportgruppe</span><span class="sxs-lookup"><span data-stu-id="694be-141">Generate a report group report</span></span>

1. <span data-ttu-id="694be-142">Klikk **Rapportgrupper** i navigasjonsruten i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="694be-142">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="694be-143">Åpne rapportgruppen som skal genereres.</span><span class="sxs-lookup"><span data-stu-id="694be-143">Open the report group to generate.</span></span>
3. <span data-ttu-id="694be-144">Klikk **Generer rapport**-knappen ![Generer rapport](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generer rapport") for å generere rapporter.</span><span class="sxs-lookup"><span data-stu-id="694be-144">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="694be-145">Slette en rapportgruppe</span><span class="sxs-lookup"><span data-stu-id="694be-145">Delete a report group</span></span>

1. <span data-ttu-id="694be-146">Klikk **Rapportgrupper** i navigasjonsruten i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="694be-146">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="694be-147">Høyreklikk rapportgruppen som skal slettes, og velg deretter **Slett**.</span><span class="sxs-lookup"><span data-stu-id="694be-147">Right-click the report group to delete, and then select **Delete**.</span></span>
3. <span data-ttu-id="694be-148">Når det vises en bekreftelsesmelding, klikker du **Ja**.</span><span class="sxs-lookup"><span data-stu-id="694be-148">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="694be-149">Kontroller i kategorien Rapportgruppe</span><span class="sxs-lookup"><span data-stu-id="694be-149">Report Group tab controls</span></span>
<span data-ttu-id="694be-150">Tabellen nedenfor beskriver kontrollene i kategorien **Rapportgruppe**.</span><span class="sxs-lookup"><span data-stu-id="694be-150">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="694be-151">Styring</span><span class="sxs-lookup"><span data-stu-id="694be-151">Control</span></span></th>
<th><span data-ttu-id="694be-152">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="694be-152">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="694be-153">Overstyre firma, detaljer og datoinnstillinger fra individuelle rapportdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="694be-153">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="694be-154">Merk av for dette alternativet for å overstyre individuelle rapportdefinisjoner av rapportene i denne rapportgruppen for generering av bare disse rapportene.</span><span class="sxs-lookup"><span data-stu-id="694be-154">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="694be-155">Firmanavn</span><span class="sxs-lookup"><span data-stu-id="694be-155">Company name</span></span></td>
<td><span data-ttu-id="694be-156">Velg firmaet som skal brukes for rapportene.</span><span class="sxs-lookup"><span data-stu-id="694be-156">Select the company to use for the reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="694be-157">Detaljnivå</span><span class="sxs-lookup"><span data-stu-id="694be-157">Detail level</span></span></td>
<td><span data-ttu-id="694be-158">Angi detaljnivået som rapportene inneholder.</span><span class="sxs-lookup"><span data-stu-id="694be-158">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="694be-159"><strong>Økonomi</strong>– En sammendragsrapport på høyt nivå.</span><span class="sxs-lookup"><span data-stu-id="694be-159"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="694be-160">Du kan ikke drille ned til kontoer og dimensjoner, bortsett fra kontoene og dimensjonene som lagt til gjennom et rapporteringstre.</span><span class="sxs-lookup"><span data-stu-id="694be-160">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="694be-161"><strong>Økonomisk og Konto</strong> − En rapport som inneholder et overordnet sammendrag og kontodetaljer.</span><span class="sxs-lookup"><span data-stu-id="694be-161"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="694be-162"><strong>Økonomisk, Konto og Transaksjon</strong> − En rapport som inneholder et overordnet sammendrag og transaksjonsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="694be-162"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="694be-163">Provisorisk</span><span class="sxs-lookup"><span data-stu-id="694be-163">Provisional</span></span></td>
<td><span data-ttu-id="694be-164">Angi aktivitetstypene som rapportene inneholder.</span><span class="sxs-lookup"><span data-stu-id="694be-164">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="694be-165"><strong>Bare postert aktivitet</strong>− Inkluderer bare transaksjonene og saldoene som er postert i finansdataene.</span><span class="sxs-lookup"><span data-stu-id="694be-165"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="694be-166"><strong>Postert og upostert aktivitet</strong>− Inkluderer alle transaksjonene og saldoene som er registrert og postert i finansdataene.</span><span class="sxs-lookup"><span data-stu-id="694be-166"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="694be-167"><strong>Bare upostert aktivitet</strong>− Inkluderer bare transaksjonene som er registrert, men som ennå ikke er postert i finansdataene.</span><span class="sxs-lookup"><span data-stu-id="694be-167"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="694be-168">Ta med alle rapporteringsvalutaer</span><span class="sxs-lookup"><span data-stu-id="694be-168">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="694be-169">Alle tilleggsrapporteringsvalutaer som er konfigurert i Microsoft Dynamics ERP-systemet, vises her.</span><span class="sxs-lookup"><span data-stu-id="694be-169">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="694be-170">Merk av for dette alternativet for å generere tilleggsrapporter i valutaene som er angitt.</span><span class="sxs-lookup"><span data-stu-id="694be-170">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="694be-171">For å vise rapportene i nettvisningsprogrammet ved å klikke <strong>Valuta</strong>-knappen og velge en valuta.</span><span class="sxs-lookup"><span data-stu-id="694be-171">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="694be-172">Datoinformasjon ikke lagret med rapportdefinisjon</span><span class="sxs-lookup"><span data-stu-id="694be-172">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="694be-173">Basisperiode</span><span class="sxs-lookup"><span data-stu-id="694be-173">Base period</span></span></li>
<li><span data-ttu-id="694be-174">Basisår</span><span class="sxs-lookup"><span data-stu-id="694be-174">Base year</span></span></li>
<li><span data-ttu-id="694be-175">Periode som er dekket</span><span class="sxs-lookup"><span data-stu-id="694be-175">Period covered</span></span></li>
</ul>
<span data-ttu-id="694be-176">Bare innstillingene for standard basisperiode lagres med rapportdefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="694be-176">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="694be-177">Datoinformasjon lagret med rapportdefinisjon</span><span class="sxs-lookup"><span data-stu-id="694be-177">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="694be-178">Rapportdato</span><span class="sxs-lookup"><span data-stu-id="694be-178">Report date</span></span></li>
<li><span data-ttu-id="694be-179">Standard basisperiode</span><span class="sxs-lookup"><span data-stu-id="694be-179">Default base period</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="694be-180">Rapporter i gruppen</span><span class="sxs-lookup"><span data-stu-id="694be-180">Reports in group</span></span></td>
<td><span data-ttu-id="694be-181">Legg til, fjerne og endre rapportrekkefølgen i rapportgruppen.</span><span class="sxs-lookup"><span data-stu-id="694be-181">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="694be-182">Hvis du vil legge til rapportdefinisjoner i rapportgruppen, dobbeltklikker du rapportgruppen for å åpne den og klikker deretter <strong>Legg til</strong>.</span><span class="sxs-lookup"><span data-stu-id="694be-182">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="694be-183">Velg rapportene som skal inkluderes i rapportgruppen, og klikk deretter <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="694be-183">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="694be-184">Hvis du vil fjerne en rapport fra rapportgruppen, velger du den og klikker deretter <strong>Fjern</strong>.</span><span class="sxs-lookup"><span data-stu-id="694be-184">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="694be-185">Hvis du vil endre rekkefølgen som rapportene genereres i, velger du en rapport i listen og klikker deretter <strong>Flytt opp</strong> eller <strong>Flytt ned</strong>.</span><span class="sxs-lookup"><span data-stu-id="694be-185">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="694be-186">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="694be-186">Additional resources</span></span>

[<span data-ttu-id="694be-187">Finansrapportering</span><span class="sxs-lookup"><span data-stu-id="694be-187">Financial reporting</span></span>](financial-reporting-intro.md)
