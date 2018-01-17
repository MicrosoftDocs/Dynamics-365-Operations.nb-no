---
title: Tilbakestille data mart for finansrapportering
description: Dette emnet beskriver hvordan du tilbakestiller data mart for finansrapportering.
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="10a86-103">Tilbakestille data mart for finansrapportering</span><span class="sxs-lookup"><span data-stu-id="10a86-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="10a86-104">Dette emnet forklarer hvordan du tilbakestiller data mart for finansrapportering for følgende versjoner:</span><span class="sxs-lookup"><span data-stu-id="10a86-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="10a86-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting versjon 7.2.6.0 og nyere</span><span class="sxs-lookup"><span data-stu-id="10a86-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="10a86-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting versjon 7.0.10000.4 og nyere</span><span class="sxs-lookup"><span data-stu-id="10a86-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="10a86-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (lokal)</span><span class="sxs-lookup"><span data-stu-id="10a86-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="10a86-108">Hvis du vil ha Finance and Operations Financial reporting versjon 7.2.6.0, kan du laste ned KB 4052514 fra <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span><span class="sxs-lookup"><span data-stu-id="10a86-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="10a86-109">Tilbakestille data mart for finansrapportering for Finance and Operations Financial reporting versjon 7.2.6.0 og nyere</span><span class="sxs-lookup"><span data-stu-id="10a86-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="10a86-110">Tilbakestille datamart for finansrapportering fra Rapportutforming</span><span class="sxs-lookup"><span data-stu-id="10a86-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="10a86-111">Trinnene i denne prosessen støttes for Finance and Operations Financial reporting versjon 7.2.6.0 og senere.</span><span class="sxs-lookup"><span data-stu-id="10a86-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="10a86-112">Hvis du har en eldre versjon, kan du kontakte kundestøtteteamet for å få hjelp.</span><span class="sxs-lookup"><span data-stu-id="10a86-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="10a86-113">I bestemte situasjoner må du kanskje tilbakestille data mart for finansrapportering.</span><span class="sxs-lookup"><span data-stu-id="10a86-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="10a86-114">Du kan fullføre denne oppgaven i Rapportutforming-klienten.</span><span class="sxs-lookup"><span data-stu-id="10a86-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="10a86-115">Her er noen scenarier der du kanskje må tilbakestille data mart:</span><span class="sxs-lookup"><span data-stu-id="10a86-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="10a86-116">Finance and Operations-databasen ble gjenopprettet, men data mart-databasen ble ikke gjenopprettet.</span><span class="sxs-lookup"><span data-stu-id="10a86-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="10a86-117">Du kan se uriktige data for en periode.</span><span class="sxs-lookup"><span data-stu-id="10a86-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="10a86-118">Kundestøtte ber deg om å tilbakestille data mart-databasen som en del av et trinn i feilsøkingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="10a86-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="10a86-119">Data mart-tilbakestillingen bør bare utføres når det foregår lite behandling i databasen.</span><span class="sxs-lookup"><span data-stu-id="10a86-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="10a86-120">Finansrapportering blir ikke tilgjengelig under tilbakestillingen.</span><span class="sxs-lookup"><span data-stu-id="10a86-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="10a86-121">Tilbakestill data mart</span><span class="sxs-lookup"><span data-stu-id="10a86-121">Reset the data mart</span></span>

<span data-ttu-id="10a86-122">Hvis du vil tilbakestille data mart, går du til rapportutforming og velger **Tilbakestill data mart** på **Verktøy**-menyen.</span><span class="sxs-lookup"><span data-stu-id="10a86-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="10a86-123">Dialogboksen som vises, har to deler: **Statistikk** og **Tilbakestill**.</span><span class="sxs-lookup"><span data-stu-id="10a86-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="10a86-124">[![Dialogboksen Tilbakestill data mart](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="10a86-124">[![Reset Data Mart dialog box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="10a86-125">Integreringsforsøk</span><span class="sxs-lookup"><span data-stu-id="10a86-125">Integration attempts</span></span>

<span data-ttu-id="10a86-126">**Integreringsforsøk**-rutenettet viser hvor mange ganger systemet har forsøkt å integrere transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="10a86-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="10a86-127">Systemet fortsetter å prøve å integrere data i en periode med dager hvis de første få forsøkene ikke lykkes.</span><span class="sxs-lookup"><span data-stu-id="10a86-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="10a86-128">Du vil vite at data mart må tilbakestilles hvis antall forsøk er 8 eller mer, og hvis det er mange dimensjonskombinasjoner eller transaksjonsposter.</span><span class="sxs-lookup"><span data-stu-id="10a86-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="10a86-129">I så fall vil ikke dataene rapporteres.</span><span class="sxs-lookup"><span data-stu-id="10a86-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="10a86-130">Datastatus</span><span class="sxs-lookup"><span data-stu-id="10a86-130">Data status</span></span>

<span data-ttu-id="10a86-131">**Datastatus**-rutenettet gir en oversikt over transaksjoner, valutakurser og dimensjonsverdier i data mart.</span><span class="sxs-lookup"><span data-stu-id="10a86-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="10a86-132">Mange foreldede oppføringer angir at det har oppstått mange oppdateringer av postene.</span><span class="sxs-lookup"><span data-stu-id="10a86-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="10a86-133">Dette kan føre til at rapportgenereringstidene kan gå saktere.</span><span class="sxs-lookup"><span data-stu-id="10a86-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="10a86-134">Feiljusterte hovedkontokategorier</span><span class="sxs-lookup"><span data-stu-id="10a86-134">Misaligned main account categories</span></span>

<span data-ttu-id="10a86-135">Hvis du bruker en versjon som er eldre enn Microsoft Dynamics 365 for Finance and Operations Financial reporting versjon 7.2.1, må du kanskje tilbakestille data mart hvis du gir kontoer nytt navn og flytter kontoer mellom kontokategorier.</span><span class="sxs-lookup"><span data-stu-id="10a86-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="10a86-136">Disse handlingene kan føre til at hovedkontokategorier blir feiljustert.</span><span class="sxs-lookup"><span data-stu-id="10a86-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="10a86-137">**Feiljusterte hovedkontokategorier**-feltet viser om du opplever dette problemet.</span><span class="sxs-lookup"><span data-stu-id="10a86-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="10a86-138">Tilbakestille data mart i Finance and Operations Financial reporting versjon 7.2.6.0</span><span class="sxs-lookup"><span data-stu-id="10a86-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="10a86-139">Hvis du vil tilbakestille data mart i Finance and Operations Financial reporting versjon 7.2.6.0 og tidligere, går du til **Tilbakestill data mart**-dialogboksen, merker av for **Tilbakestill data mart** og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="10a86-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="10a86-140">Du bør bare tilbakestille data mart under planlagt nedetid.</span><span class="sxs-lookup"><span data-stu-id="10a86-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="10a86-141">[![Avmerkingsboksen Tilbakestill data mart](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="10a86-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="10a86-142">Tilbakestille data mart og velge en årsak i Microsoft Dynamics 365 for Finance and Operations Financial reporting versjon 7.3.0</span><span class="sxs-lookup"><span data-stu-id="10a86-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="10a86-143">Hvis du finner ut at det kreves en tilbakestilling av data mart, merker du av for **Tilbakestill data mart**, og velger deretter en årsak i **Årsak**-feltet.</span><span class="sxs-lookup"><span data-stu-id="10a86-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="10a86-144">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="10a86-144">The following options are available:</span></span>

- <span data-ttu-id="10a86-145">**Manglende eller ugyldige data** – Basert på statistikken har du fastslått at data kan mangle.</span><span class="sxs-lookup"><span data-stu-id="10a86-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="10a86-146">Før du fortsetter, anbefaler vi at du arbeider med støtte for å fastslå årsaken.</span><span class="sxs-lookup"><span data-stu-id="10a86-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="10a86-147">**Gjenopprett database** – Finance and Operations-databasen ble gjenopprettet, men databasen for data-mart for finansrapportering ble ikke gjenopprettet.</span><span class="sxs-lookup"><span data-stu-id="10a86-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="10a86-148">**Andre** – Du tilbakestiller data mart av en annen grunn.</span><span class="sxs-lookup"><span data-stu-id="10a86-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="10a86-149">Hvis du er redd for at det er et problem, kan du kontakte kundestøtte for å identifisere det.</span><span class="sxs-lookup"><span data-stu-id="10a86-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

<span data-ttu-id="10a86-150">[![Tilbakestill datatorg](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="10a86-150">[![Reset data mart](./media/Integration.png)](./media/Integration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="10a86-151">Kontroller at alle tilbakestillingsoppgaver for datatorg har fullført en innledende belastning før du begynner en tilbakestilling.</span><span class="sxs-lookup"><span data-stu-id="10a86-151">Verify that all data mart reset tasks have completed an initial load before you begin a reset.</span></span> <span data-ttu-id="10a86-152">Du kan kontrollere dette ved å se etter en verdi i kolonnen Klokkeslett for forrige kjøring ved å velge **Verktøy** &gt; **Integreringsstatus**.</span><span class="sxs-lookup"><span data-stu-id="10a86-152">You can confirm this by looking for a value in the Last Runtime column by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="10a86-153">Fjern brukere og firmaer</span><span class="sxs-lookup"><span data-stu-id="10a86-153">Clear users and companies</span></span>

<span data-ttu-id="10a86-154">Merk av for **Fjern brukere og firmaer** hvis du har gjenopprettet databasen, men deretter har gjort endringer i brukere eller selskaper.</span><span class="sxs-lookup"><span data-stu-id="10a86-154">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="10a86-155">Du bør sjeldent få behov for å merke av i denne boksen.</span><span class="sxs-lookup"><span data-stu-id="10a86-155">You should rarely have to select this check box.</span></span>

<span data-ttu-id="10a86-156">Når du er klar til å starte tilbakestillingen, velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="10a86-156">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="10a86-157">Du blir bedt om å bekrefte at du er klar til å starte prosessen.</span><span class="sxs-lookup"><span data-stu-id="10a86-157">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="10a86-158">Legg merke til at finansrapportering ikke er tilgjengelig under tilbakestillingen og den første dataintegreringen som skjer etterpå.</span><span class="sxs-lookup"><span data-stu-id="10a86-158">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="10a86-159">Hvis du vil vise statusen for integreringen, velger du **Verktøy** &gt; **Integreringsstatus** for å se sist gang integreringen ble kjørt og statusen.</span><span class="sxs-lookup"><span data-stu-id="10a86-159">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="10a86-160">[![Vise statusen for integreringen](./media/New-integration.PNG)](./media/New-integration.PNG)</span><span class="sxs-lookup"><span data-stu-id="10a86-160">[![View the status of the integration](./media/New-integration.PNG)](./media/New-integration.PNG)</span></span>

> [!NOTE]
> <span data-ttu-id="10a86-161">Tilbakestillingen er fullført når alle tilordninger viser statusen RanToCompletion og vinduet Integreringsstatus viser "Integrering er fullført" i hjørnet nederst til venstre.</span><span class="sxs-lookup"><span data-stu-id="10a86-161">The reset is finished when all mappings show the status of RanToCompletion and the Integration Status window says “Integration complete” in the bottom-left corner.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="10a86-162">Tilbakestille data mart for finansrapportering for Finance and Operations Financial reporting versjon 7.0.10000.4 og nyere</span><span class="sxs-lookup"><span data-stu-id="10a86-162">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="10a86-163">Hvis du gjenoppretter Finance and Operations-databasen fra en sikkerhetskopi eller kopierer databasen fra et annet miljø, må du følge trinnene i denne delen for å sikre at data mart for finansrapportering bruker den gjenopprettede Finance and Operations-databasen på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="10a86-163">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="10a86-164">Fremgangsmåten i denne prosessen støttes for Microsoft Dynamics AX-programmet versjon 7.0.1 (mai 2016) (programbygg 7.0.1265.23014 og Financial reporting bygg 7.0.10000.4) og nyere.</span><span class="sxs-lookup"><span data-stu-id="10a86-164">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="10a86-165">Hvis du har en tidligere versjon av Finance and Operations, kan du kontakte kundestøtte for å få hjelp.</span><span class="sxs-lookup"><span data-stu-id="10a86-165">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="10a86-166">Eksportere rapportdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="10a86-166">Export report definitions</span></span>

<span data-ttu-id="10a86-167">Først gjør du følgende for å eksportere rapportutformingene fra Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="10a86-167">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="10a86-168">I Rapportutforming velger du **Firma** &gt; **Byggeblokkgrupper**.</span><span class="sxs-lookup"><span data-stu-id="10a86-168">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="10a86-169">Velg byggeblokkgruppen du vil eksportere, og velg deretter **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="10a86-169">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10a86-170">For Finance and Operations støttes bare én byggeblokkgruppe, **Standard**.</span><span class="sxs-lookup"><span data-stu-id="10a86-170">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="10a86-171">Velg rapportdefinisjonene som skal eksporteres:</span><span class="sxs-lookup"><span data-stu-id="10a86-171">Select the report definitions to export:</span></span>

    - <span data-ttu-id="10a86-172">Hvis du vil eksportere alle rapportdefinisjonene og de tilknyttede byggeblokkene, velger du **Merk alle**.</span><span class="sxs-lookup"><span data-stu-id="10a86-172">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="10a86-173">Hvis du vil eksportere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, velger du den aktuelle kategorien og velger deretter elementene som skal eksporteres.</span><span class="sxs-lookup"><span data-stu-id="10a86-173">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="10a86-174">Trykk og hold inne Ctrl-tasten for å velge flere varer i en kategori. Når du velger rapporter som skal eksporteres, velges de tilhørende radene, kolonnene, trærne og dimensjonssettene.</span><span class="sxs-lookup"><span data-stu-id="10a86-174">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="10a86-175">Velg **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="10a86-175">Select **Export**.</span></span>
5. <span data-ttu-id="10a86-176">Skriv inn et filnavn, og velger en sikkert plassering der du vil lagre de eksporterte rapportdefinisjonene.</span><span class="sxs-lookup"><span data-stu-id="10a86-176">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="10a86-177">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="10a86-177">Select **Save**.</span></span>

<span data-ttu-id="10a86-178">Du kan kopiere eller laste opp filen til en sikker plassering.</span><span class="sxs-lookup"><span data-stu-id="10a86-178">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="10a86-179">På denne måten kan filen importeres til et annet miljø senere.</span><span class="sxs-lookup"><span data-stu-id="10a86-179">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="10a86-180">Du finner informasjon om hvordan du bruker en Microsoft Azure-lagringskonto i [Overføre data med kommandolinjeverktøyet AzCopy](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="10a86-180">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="10a86-181">Microsoft tilbyr ingen lagringskonto som en del av Finance and Operations-avtalen.</span><span class="sxs-lookup"><span data-stu-id="10a86-181">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="10a86-182">Du må kjøpe en lagringskonto eller bruke en lagringskonto fra et eget Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="10a86-182">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="10a86-183">Vær oppmerksom på virkemåten til stasjon D på virtuelle Azure-maskiner (VM-er).</span><span class="sxs-lookup"><span data-stu-id="10a86-183">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="10a86-184">Ikke lagre de eksporterte byggeblokkgruppene permanent på stasjon D. Hvis du vil ha mer informasjon om midlertidige stasjoner, kan du se [Forstå den midlertidige stasjonen på virtuelle Windows Azure-maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="10a86-184">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="10a86-185">Stoppe tjenester</span><span class="sxs-lookup"><span data-stu-id="10a86-185">Stop services</span></span>

<span data-ttu-id="10a86-186">Følgende Microsoft Windows-tjenester vil ha åpne tilkoblinger til Finance and Operations-databasen.</span><span class="sxs-lookup"><span data-stu-id="10a86-186">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="10a86-187">Derfor må du bruke Microsoft Eksternt skrivebord til å koble til alle datamaskinene i miljøet, og deretter bruke services.msc til å stoppe disse tjenestene.</span><span class="sxs-lookup"><span data-stu-id="10a86-187">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="10a86-188">Webpubliseringstjenesten (for alle AOS-datamaskiner (Application Object-servere))</span><span class="sxs-lookup"><span data-stu-id="10a86-188">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="10a86-189">Partistyringstjenesten for Microsoft Dynamics 365 for Finance and Operations (bare for ikke-private AOS-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="10a86-189">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="10a86-190">Prosesstjenesten for Management Reporter 2012 (bare på Business intelligence [BI]-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="10a86-190">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="10a86-191">Tilbakestill</span><span class="sxs-lookup"><span data-stu-id="10a86-191">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="10a86-192">Last ned den siste MinorVersionDataUpgrade.zip-pakken</span><span class="sxs-lookup"><span data-stu-id="10a86-192">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="10a86-193">Last ned den siste MinorVersionDataUpgrade.zip-pakken.</span><span class="sxs-lookup"><span data-stu-id="10a86-193">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="10a86-194">For instruksjoner om hvordan du finner og laster ned riktig versjon av dataoppgraderingspakken, kan du se [Last ned den nyeste distribuerbare dataoppgraderingspakken](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="10a86-194">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> 

<span data-ttu-id="10a86-195">En oppgradering er ikke nødvendig for å laste ned MinorVersionDataUpgrade.zip-pakken.</span><span class="sxs-lookup"><span data-stu-id="10a86-195">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="10a86-196">Du må derfor bare følge trinnene i delen "Last ned den nyeste distribuerbare dataoppgraderingspakken" i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="10a86-196">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="10a86-197">Du kan hoppe over alle de andre trinnene i emnet.</span><span class="sxs-lookup"><span data-stu-id="10a86-197">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="10a86-198">Kjøre skript på Finance and Operations-databasen</span><span class="sxs-lookup"><span data-stu-id="10a86-198">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="10a86-199">Kjør skriptene nedenfor på Finance and Operations-databasen (ikke mot finansrapporteringsdatabasen):</span><span class="sxs-lookup"><span data-stu-id="10a86-199">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="10a86-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="10a86-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="10a86-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="10a86-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="10a86-202">Disse skriptene bidrar til å sikre at innstillinger for brukere, roller og endringssporing er riktige.</span><span class="sxs-lookup"><span data-stu-id="10a86-202">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="10a86-203">Kjøre en Windows PowerShell-kommando for å tilbakestille databasen</span><span class="sxs-lookup"><span data-stu-id="10a86-203">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="10a86-204">På AOS-datamaskinen starter du Microsoft Windows PowerShell som administrator, og kjører følgende kommandoer for å tilbakestille integreringen mellom Finance and Operations og finansrapportering.</span><span class="sxs-lookup"><span data-stu-id="10a86-204">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="10a86-205">Her finner du en forklaring på parameterne i **Reset-DatamartIntegration**-kommandoen:</span><span class="sxs-lookup"><span data-stu-id="10a86-205">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="10a86-206">Gyldige verdier for **-Reason** er **SERVICING**, **BADDATA** og **OTHER**.</span><span class="sxs-lookup"><span data-stu-id="10a86-206">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="10a86-207">Parameteren **-ReasonDetail** er fritekst.</span><span class="sxs-lookup"><span data-stu-id="10a86-207">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="10a86-208">Reason og reason detail blir registrert i telemetri / miljøovervåking.</span><span class="sxs-lookup"><span data-stu-id="10a86-208">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="10a86-209">Når du har kjørt kommandoene, får du spørsmål om å angi **Y** for å bekrefte at du vil tilbakestille databasen.</span><span class="sxs-lookup"><span data-stu-id="10a86-209">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="10a86-210">Starte tjenester på nytt</span><span class="sxs-lookup"><span data-stu-id="10a86-210">Restart services</span></span>

<span data-ttu-id="10a86-211">Bruk Services.msc til å starte tjenestene du stoppet tidligere:</span><span class="sxs-lookup"><span data-stu-id="10a86-211">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="10a86-212">Webpubliseringstjenesten (for alle AOS-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="10a86-212">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="10a86-213">Partistyringstjenesten for Microsoft Dynamics 365 for Finance and Operations (bare for ikke-private AOS-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="10a86-213">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="10a86-214">Prosesstjenesten for Management Reporter 2012 (bare for BI-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="10a86-214">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="10a86-215">Importere rapportdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="10a86-215">Import report definitions</span></span>

<span data-ttu-id="10a86-216">Importer rapportutformingene fra Rapportutforming ved hjelp av filen som ble opprettet under eksporten.</span><span class="sxs-lookup"><span data-stu-id="10a86-216">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="10a86-217">I Rapportutforming velger du **Firma** &gt; **Byggeblokkgrupper**.</span><span class="sxs-lookup"><span data-stu-id="10a86-217">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="10a86-218">Velg byggeblokkgruppen du vil eksportere, og velg deretter **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="10a86-218">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10a86-219">For Finance and Operations støttes bare én byggeblokkgruppe, **Standard**.</span><span class="sxs-lookup"><span data-stu-id="10a86-219">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="10a86-220">Velg **Standard**-byggeblokken, og velg deretter **Importer**.</span><span class="sxs-lookup"><span data-stu-id="10a86-220">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="10a86-221">Velg filen som inneholder de eksporterte rapportdefinisjonene, og velg deretter **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="10a86-221">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="10a86-222">Velg rapportdefinisjonene som skal importeres, i dialogboksen **Importer**:</span><span class="sxs-lookup"><span data-stu-id="10a86-222">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="10a86-223">Hvis du vil importere alle rapportdefinisjonene og de tilknyttede byggeblokkene, velger du **Merk alle**.</span><span class="sxs-lookup"><span data-stu-id="10a86-223">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="10a86-224">Hvis du vil importere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, merker du rapportene, radene, kolonnene, trærne eller dimensjonssettene som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="10a86-224">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="10a86-225">Velg **Import**.</span><span class="sxs-lookup"><span data-stu-id="10a86-225">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="10a86-226">Tilbakestille data mart for finansrapportering for Finance and Operations (lokal)</span><span class="sxs-lookup"><span data-stu-id="10a86-226">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="10a86-227">Be alle brukerne om å avslutte Rapportutforming og Finansrapportering-området i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10a86-227">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="10a86-228">Kjør følgende skript på Finansrapportering-databasen (MRDB).</span><span class="sxs-lookup"><span data-stu-id="10a86-228">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="10a86-229">Avkort eller slett alle postene fra tabellen FINANCIALREPORTS i Finance and Operations-databasen (AXDB).</span><span class="sxs-lookup"><span data-stu-id="10a86-229">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="10a86-230">Avkort eller slett alle postene fra tabellen FINANCIALREPORTVERSION hvis denne tabellen finnes i Finance and Operations-databasen.</span><span class="sxs-lookup"><span data-stu-id="10a86-230">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="10a86-231">Hvis tabellen ikke finnes i Finance and Operations-databasen, hopper du over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="10a86-231">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="10a86-232">Kjør **ResetDatamart**-skriptet på Finansrapportering-databasen.</span><span class="sxs-lookup"><span data-stu-id="10a86-232">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="10a86-233">Dette skriptet deaktiverer data mart-integreringen, sletter alle data mart-dataene og aktiverer deretter data mart-integreringen på nytt.</span><span class="sxs-lookup"><span data-stu-id="10a86-233">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="10a86-234">Etter tilbakestillingen, kan du bekrefte den nye datainnlastingen manuelt ved å kjøre følgende spørring mot Finansrapportering-databasen.</span><span class="sxs-lookup"><span data-stu-id="10a86-234">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="10a86-235">Kontroller at alle rader har verdien **LastRunTime**, og at **StateType** er satt til **5**.</span><span class="sxs-lookup"><span data-stu-id="10a86-235">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="10a86-236">En **StateType**-verdi på **5** angir at dataene ble lastet inn på nytt.</span><span class="sxs-lookup"><span data-stu-id="10a86-236">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="10a86-237">En verdi på **7** angir en feilstatus.</span><span class="sxs-lookup"><span data-stu-id="10a86-237">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="10a86-238">Noen ganger har organisasjonshierarkikartet denne tilstanden første gang den kjøres.</span><span class="sxs-lookup"><span data-stu-id="10a86-238">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="10a86-239">Feilstatusen må imidlertid løses automatisk.</span><span class="sxs-lookup"><span data-stu-id="10a86-239">However, the faulted state but should be automatically resolved.</span></span>

