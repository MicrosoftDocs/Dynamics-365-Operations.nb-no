---
title: Organisere rapportkomponenter i rapportutforming
description: "Når du har utformet byggeblokker og genererte rapporter, er det nyttig å organisere disse objektene slik at de blir enklere for brukerne å finne. Denne artikkelen beskriver hvordan du organiserer eksisterende rapporter, byggeblokker og objekter i rapportutforming."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7207febc58dbab1df5551ae0f74ad74d9ced8e56
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="5a72f-104">Organisere rapportkomponenter i rapportutforming</span><span class="sxs-lookup"><span data-stu-id="5a72f-104">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a72f-105">Når du har utformet byggeblokker og genererte rapporter, er det nyttig å organisere disse objektene slik at de blir enklere for brukerne å finne.</span><span class="sxs-lookup"><span data-stu-id="5a72f-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="5a72f-106">Denne artikkelen beskriver hvordan du organiserer eksisterende rapporter, byggeblokker og objekter i rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="5a72f-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="5a72f-107">Du kan gi nytt navn til mapper, rapporter, byggeblokker og andre objekter i rapportutforming, for å bidra til å organisere filene dine.</span><span class="sxs-lookup"><span data-stu-id="5a72f-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="5a72f-108">Avhengig av hvilken type objekt du gir nytt navn, må du kanskje oppdatere tilknytninger til dette objektet.</span><span class="sxs-lookup"><span data-stu-id="5a72f-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="5a72f-109">Gi nytt navn til en mappe eller byggeblokk i Rapportutforming</span><span class="sxs-lookup"><span data-stu-id="5a72f-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="5a72f-110">I Rapportutforming kan du gi nytt navn til mapper, rapportdefinisjoner, raddefinisjoner, kolonnedefinisjoner og rapporteringstredefinisjoner.</span><span class="sxs-lookup"><span data-stu-id="5a72f-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span> <span data-ttu-id="5a72f-111">**Obs!** Når du gir nytt navn til en byggeblokk, må du oppdatere alle rapporteringsdefinisjoner som bruker byggeblokken.</span><span class="sxs-lookup"><span data-stu-id="5a72f-111">**Note:** When you rename a building block, you must update any reporting definitions that use the building block.</span></span> <span data-ttu-id="5a72f-112">Hvis ikke, kan ikke en ny rapport genereres.</span><span class="sxs-lookup"><span data-stu-id="5a72f-112">Otherwise, a new report can't be generated.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="5a72f-113">Gi nytt navn til en mappe eller byggeblokk i Rapportutforming</span><span class="sxs-lookup"><span data-stu-id="5a72f-113">Rename a folder or building block in Report Designer</span></span>

1.  <span data-ttu-id="5a72f-114">I Report Designer kan du bruke navigasjonsruten til å finne mappen eller objektet du vil gi nytt navn.</span><span class="sxs-lookup"><span data-stu-id="5a72f-114">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2.  <span data-ttu-id="5a72f-115">Høyreklikk mappen eller objektet, og klikk deretter **Gi nytt navn**.</span><span class="sxs-lookup"><span data-stu-id="5a72f-115">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="5a72f-116">**Navn**-feltet i navigasjonsruten blir tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="5a72f-116">The **Name** field in the navigation pane becomes available.</span></span>
3.  <span data-ttu-id="5a72f-117">Skriv inn et nytt navn, og trykk deretter Enter.</span><span class="sxs-lookup"><span data-stu-id="5a72f-117">Type a new name, and then press Enter.</span></span>
4.  <span data-ttu-id="5a72f-118">Hvis byggeblokken er en raddefinisjon, kolonnedefinisjon eller rapporteringstredefinisjon, må du oppdatere andre byggeblokker som er knyttet til det.</span><span class="sxs-lookup"><span data-stu-id="5a72f-118">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="5a72f-119">Høyreklikk byggeblokken du ga nytt navn i trinn 3, velg **Tilknytninger** og velg deretter et element i listen for å oppdatere det.</span><span class="sxs-lookup"><span data-stu-id="5a72f-119">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5.  <span data-ttu-id="5a72f-120">Gjenta trinn 4 til alle tilknyttede elementer er oppdaterte.</span><span class="sxs-lookup"><span data-stu-id="5a72f-120">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="5a72f-121">Opprette og administrere rapportgrupper.</span><span class="sxs-lookup"><span data-stu-id="5a72f-121">Create and manage report groups</span></span>
<span data-ttu-id="5a72f-122">Du kan gruppere rapportdefinisjoner for å generere flere rapporter samtidig.</span><span class="sxs-lookup"><span data-stu-id="5a72f-122">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="5a72f-123">Hvis du vil opprette, endre, slette og generere rapportgrupper, må du ha rolle som utformer eller administrator.</span><span class="sxs-lookup"><span data-stu-id="5a72f-123">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="5a72f-124">Brukere som har generatorrollen kan generere rapportgrupper og kan også endre innstillingen for brukerrapportdefinisjonene for rapportgrupper.</span><span class="sxs-lookup"><span data-stu-id="5a72f-124">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="5a72f-125">Opprette en rapportgruppe</span><span class="sxs-lookup"><span data-stu-id="5a72f-125">Create a report group</span></span>

1.  <span data-ttu-id="5a72f-126">Klikk **Rapportgrupper** i navigasjonsruten i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="5a72f-126">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="5a72f-127">På **Fil**-menhyen klikker du **Ny** &gt; **Rapportgruppedefinisjon** for å åpne en ny rapportgruppe i visningsvinduet.</span><span class="sxs-lookup"><span data-stu-id="5a72f-127">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="5a72f-128">Du kan også klikke **Rapportgruppe**-knappen ![Rapportgruppe](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Rapportgruppe") på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="5a72f-128">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3.  <span data-ttu-id="5a72f-129">Klikk kategorien **Rapportgruppe**. For å overstyre informasjonen om de enkelte rapportdefinisjonene for genereringen av denne rapporten, merker du av for **Overstyr selskap, detalj og datoinnstillinger fra de enkelte rapportdefinisjonene**.</span><span class="sxs-lookup"><span data-stu-id="5a72f-129">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="5a72f-130">Innstillingene for firmanavnet, detaljnivået, provisorisk og datoinformasjon, fylles ut automatisk, men du kan foreta oppdateringer.</span><span class="sxs-lookup"><span data-stu-id="5a72f-130">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4.  <span data-ttu-id="5a72f-131">Hvis du vil generere flere rapporter som viser rapporteringsvalutaene, merker du av for **Inkluder alle rapporteringsvalutaer**.</span><span class="sxs-lookup"><span data-stu-id="5a72f-131">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="5a72f-132">Du kan deretter gå til flere visninger ved å klikke **Valuta** i webvisningen når du viser rapporten.</span><span class="sxs-lookup"><span data-stu-id="5a72f-132">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5.  <span data-ttu-id="5a72f-133">I feltet **Rapporter i gruppen** klikker du **Legg til** for å velge rapportene som skal tas med i rapportgruppen.</span><span class="sxs-lookup"><span data-stu-id="5a72f-133">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="5a72f-134">Hvis du vil velge flere rapporter i dialogboksen **Legg til**, holder du nede CTRL-tasten mens du merker rapporter.</span><span class="sxs-lookup"><span data-stu-id="5a72f-134">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="5a72f-135">Når du er ferdig med å velge rapporter, klikker du **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a72f-135">When you've finished selecting reports, click **OK**.</span></span>
6.  <span data-ttu-id="5a72f-136">Klikk **Fil** &gt; **Lagre** for å lagre den nye rapportgruppen.</span><span class="sxs-lookup"><span data-stu-id="5a72f-136">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="5a72f-137">Endre en rapportgruppe</span><span class="sxs-lookup"><span data-stu-id="5a72f-137">Modify a report group</span></span>

1.  <span data-ttu-id="5a72f-138">Klikk **Rapportgrupper** i navigasjonsruten i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="5a72f-138">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="5a72f-139">Dobbeltklikk rapportgruppen du vil endre.</span><span class="sxs-lookup"><span data-stu-id="5a72f-139">Double-click the report group to modify.</span></span>
3.  <span data-ttu-id="5a72f-140">I kategorien **Rapportgruppe** gjør du de ønskede endringene.</span><span class="sxs-lookup"><span data-stu-id="5a72f-140">On the **Report Group** tab, make the changes that you want.</span></span>
4.  <span data-ttu-id="5a72f-141">På **Fil**-menyen klikker du **Lagre** for å lagre den endrede rapportgruppen. Du kan også klikke **Lagre**-knappen ![Lagre](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Lagre") på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="5a72f-141">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

<span data-ttu-id="5a72f-142">**Obs!** Hvis du har planlagt rapporter slik at de genereres med jevne mellomrom, kan du overstyre disse innstillingene og generere en rapport umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="5a72f-142">**Note:** If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="5a72f-143">Generere en rapport for en rapportgruppe</span><span class="sxs-lookup"><span data-stu-id="5a72f-143">Generate a report group report</span></span>

1.  <span data-ttu-id="5a72f-144">Klikk **Rapportgrupper** i navigasjonsruten i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="5a72f-144">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="5a72f-145">Åpne rapportgruppen som skal genereres.</span><span class="sxs-lookup"><span data-stu-id="5a72f-145">Open the report group to generate.</span></span>
3.  <span data-ttu-id="5a72f-146">Klikk **Generer rapport**-knappen ![Generer rapport](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generer rapport") for å generere rapporter.</span><span class="sxs-lookup"><span data-stu-id="5a72f-146">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="5a72f-147">Slette en rapportgruppe</span><span class="sxs-lookup"><span data-stu-id="5a72f-147">Delete a report group</span></span>

1.  <span data-ttu-id="5a72f-148">Klikk **Rapportgrupper** i navigasjonsruten i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="5a72f-148">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="5a72f-149">Høyreklikk rapportgruppen som skal slettes, og velg deretter **Slett**.</span><span class="sxs-lookup"><span data-stu-id="5a72f-149">Right-click the report group to delete, and then select **Delete**.</span></span>
3.  <span data-ttu-id="5a72f-150">Når det vises en bekreftelsesmelding, klikker du **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5a72f-150">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="5a72f-151">Kontroller i kategorien Rapportgruppe</span><span class="sxs-lookup"><span data-stu-id="5a72f-151">Report Group tab controls</span></span>
<span data-ttu-id="5a72f-152">Tabellen nedenfor beskriver kontrollene i kategorien **Rapportgruppe**.</span><span class="sxs-lookup"><span data-stu-id="5a72f-152">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a72f-153">Styring</span><span class="sxs-lookup"><span data-stu-id="5a72f-153">Control</span></span></th>
<th><span data-ttu-id="5a72f-154">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5a72f-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5a72f-155">Overstyre firma, detaljer og datoinnstillinger fra individuelle rapportdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="5a72f-155">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="5a72f-156">Merk av for dette alternativet for å overstyre individuelle rapportdefinisjoner av rapportene i denne rapportgruppen for generering av bare disse rapportene.</span><span class="sxs-lookup"><span data-stu-id="5a72f-156">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a72f-157">Firmanavn</span><span class="sxs-lookup"><span data-stu-id="5a72f-157">Company name</span></span></td>
<td><span data-ttu-id="5a72f-158">Velg firmaet som skal brukes for rapportene.</span><span class="sxs-lookup"><span data-stu-id="5a72f-158">Select the company to use for the reports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a72f-159">Detaljnivå</span><span class="sxs-lookup"><span data-stu-id="5a72f-159">Detail level</span></span></td>
<td><span data-ttu-id="5a72f-160">Angi detaljnivået som rapportene inneholder.</span><span class="sxs-lookup"><span data-stu-id="5a72f-160">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="5a72f-161"><strong>Økonomi</strong>– En sammendragsrapport på høyt nivå.</span><span class="sxs-lookup"><span data-stu-id="5a72f-161"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="5a72f-162">Du kan ikke drille ned til kontoer og dimensjoner, bortsett fra kontoene og dimensjonene som lagt til gjennom et rapporteringstre.</span><span class="sxs-lookup"><span data-stu-id="5a72f-162">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="5a72f-163"><strong>Økonomisk og Konto</strong> − En rapport som inneholder et overordnet sammendrag og kontodetaljer.</span><span class="sxs-lookup"><span data-stu-id="5a72f-163"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="5a72f-164"><strong>Økonomisk, Konto og Transaksjon</strong> − En rapport som inneholder et overordnet sammendrag og transaksjonsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="5a72f-164"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a72f-165">Provisorisk</span><span class="sxs-lookup"><span data-stu-id="5a72f-165">Provisional</span></span></td>
<td><span data-ttu-id="5a72f-166">Angi aktivitetstypene som rapportene inneholder.</span><span class="sxs-lookup"><span data-stu-id="5a72f-166">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="5a72f-167"><strong>Bare postert aktivitet</strong>− Inkluderer bare transaksjonene og saldoene som er postert i finansdataene.</span><span class="sxs-lookup"><span data-stu-id="5a72f-167"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="5a72f-168"><strong>Postert og upostert aktivitet</strong>− Inkluderer alle transaksjonene og saldoene som er registrert og postert i finansdataene.</span><span class="sxs-lookup"><span data-stu-id="5a72f-168"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="5a72f-169"><strong>Bare upostert aktivitet</strong>− Inkluderer bare transaksjonene som er registrert, men som ennå ikke er postert i finansdataene.</span><span class="sxs-lookup"><span data-stu-id="5a72f-169"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a72f-170">Ta med alle rapporteringsvalutaer</span><span class="sxs-lookup"><span data-stu-id="5a72f-170">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="5a72f-171">Alle tilleggsrapporteringsvalutaer som er konfigurert i Microsoft Dynamics ERP-systemet, vises her.</span><span class="sxs-lookup"><span data-stu-id="5a72f-171">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="5a72f-172">Merk av for dette alternativet for å generere tilleggsrapporter i valutaene som er angitt.</span><span class="sxs-lookup"><span data-stu-id="5a72f-172">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="5a72f-173">For å vise rapportene i nettvisningsprogrammet ved å klikke <strong>Valuta</strong>-knappen og velge en valuta.</span><span class="sxs-lookup"><span data-stu-id="5a72f-173">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a72f-174">Datoinformasjon ikke lagret med rapportdefinisjon</span><span class="sxs-lookup"><span data-stu-id="5a72f-174">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="5a72f-175">Basisperiode</span><span class="sxs-lookup"><span data-stu-id="5a72f-175">Base period</span></span></li>
<li><span data-ttu-id="5a72f-176">Basisår</span><span class="sxs-lookup"><span data-stu-id="5a72f-176">Base year</span></span></li>
<li><span data-ttu-id="5a72f-177">Periode som er dekket</span><span class="sxs-lookup"><span data-stu-id="5a72f-177">Period covered</span></span></li>
</ul>
<span data-ttu-id="5a72f-178">Bare innstillingene for standard basisperiode lagres med rapportdefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="5a72f-178">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a72f-179">Datoinformasjon lagret med rapportdefinisjon</span><span class="sxs-lookup"><span data-stu-id="5a72f-179">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="5a72f-180">Rapportdato</span><span class="sxs-lookup"><span data-stu-id="5a72f-180">Report date</span></span></li>
<li><span data-ttu-id="5a72f-181">Standard basisperiode</span><span class="sxs-lookup"><span data-stu-id="5a72f-181">Default base period</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a72f-182">Rapporter i gruppen</span><span class="sxs-lookup"><span data-stu-id="5a72f-182">Reports in group</span></span></td>
<td><span data-ttu-id="5a72f-183">Legg til, fjerne og endre rapportrekkefølgen i rapportgruppen.</span><span class="sxs-lookup"><span data-stu-id="5a72f-183">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="5a72f-184">Hvis du vil legge til rapportdefinisjoner i rapportgruppen, dobbeltklikker du rapportgruppen for å åpne den og klikker deretter <strong>Legg til</strong>.</span><span class="sxs-lookup"><span data-stu-id="5a72f-184">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="5a72f-185">Velg rapportene som skal inkluderes i rapportgruppen, og klikk deretter <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="5a72f-185">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="5a72f-186">Hvis du vil fjerne en rapport fra rapportgruppen, velger du den og klikker deretter <strong>Fjern</strong>.</span><span class="sxs-lookup"><span data-stu-id="5a72f-186">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="5a72f-187">Hvis du vil endre rekkefølgen som rapportene genereres i, velger du en rapport i listen og klikker deretter <strong>Flytt opp</strong> eller <strong>Flytt ned</strong>.</span><span class="sxs-lookup"><span data-stu-id="5a72f-187">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="5a72f-188">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5a72f-188">Additional resources</span></span>
--------

[<span data-ttu-id="5a72f-189">Finansrapportering</span><span class="sxs-lookup"><span data-stu-id="5a72f-189">Financial reporting</span></span>](financial-reporting-intro.md)




