---
title: Tilbakestille data mart for finansrapportering
description: Dette emnet beskriver hvordan du tilbakestiller data mart for finansrapportering.
author: aolson
manager: AnnBe
ms.date: 12/01/2017
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
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: nb-no
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="1f10f-103">Tilbakestille data mart for finansrapportering</span><span class="sxs-lookup"><span data-stu-id="1f10f-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1f10f-104">Dette emnet forklarer hvordan du tilbakestiller data mart for finansrapportering for følgende versjoner:</span><span class="sxs-lookup"><span data-stu-id="1f10f-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="1f10f-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting versjon 7.2.6.0 og nyere</span><span class="sxs-lookup"><span data-stu-id="1f10f-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="1f10f-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting versjon 7.0.10000.4 og nyere</span><span class="sxs-lookup"><span data-stu-id="1f10f-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="1f10f-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (lokal)</span><span class="sxs-lookup"><span data-stu-id="1f10f-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="1f10f-108">Hvis du vil ha Finance and Operations Financial reporting versjon 7.2.6.0, kan du laste ned KB 4052514 fra <https://support.microsoft.com/en-us/help/4052514>.</span><span class="sxs-lookup"><span data-stu-id="1f10f-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://support.microsoft.com/en-us/help/4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="1f10f-109">Tilbakestille data mart for finansrapportering for Finance and Operations Financial reporting versjon 7.2.6.0 og nyere</span><span class="sxs-lookup"><span data-stu-id="1f10f-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="1f10f-110">Tilbakestille datamart for finansrapportering fra Rapportutforming</span><span class="sxs-lookup"><span data-stu-id="1f10f-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="1f10f-111">Trinnene i denne prosessen støttes for Finance and Operations Financial reporting versjon 7.2.6.0 og senere.</span><span class="sxs-lookup"><span data-stu-id="1f10f-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="1f10f-112">Hvis du har en eldre versjon, kan du kontakte kundestøtteteamet for å få hjelp.</span><span class="sxs-lookup"><span data-stu-id="1f10f-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="1f10f-113">I bestemte situasjoner må du kanskje tilbakestille data mart for finansrapportering.</span><span class="sxs-lookup"><span data-stu-id="1f10f-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="1f10f-114">Du kan fullføre denne oppgaven i Rapportutforming-klienten.</span><span class="sxs-lookup"><span data-stu-id="1f10f-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="1f10f-115">Her er noen scenarier der du kanskje må tilbakestille data mart:</span><span class="sxs-lookup"><span data-stu-id="1f10f-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="1f10f-116">Finance and Operations-databasen ble gjenopprettet, men data mart-databasen ble ikke gjenopprettet.</span><span class="sxs-lookup"><span data-stu-id="1f10f-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="1f10f-117">Du kan se uriktige data for en periode.</span><span class="sxs-lookup"><span data-stu-id="1f10f-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="1f10f-118">Kundestøtte ber deg om å tilbakestille data mart-databasen som en del av et trinn i feilsøkingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="1f10f-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="1f10f-119">Data mart-tilbakestillingen bør bare utføres når det foregår lite behandling i databasen.</span><span class="sxs-lookup"><span data-stu-id="1f10f-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="1f10f-120">Finansrapportering blir ikke tilgjengelig under tilbakestillingen.</span><span class="sxs-lookup"><span data-stu-id="1f10f-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="1f10f-121">Tilbakestill data mart</span><span class="sxs-lookup"><span data-stu-id="1f10f-121">Reset the data mart</span></span>

<span data-ttu-id="1f10f-122">Hvis du vil tilbakestille data mart, går du til rapportutforming og velger **Tilbakestill data mart** på **Verktøy**-menyen.</span><span class="sxs-lookup"><span data-stu-id="1f10f-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="1f10f-123">Dialogboksen som vises, har to deler: **Statistikk** og **Tilbakestill**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="1f10f-124">[![Dialogboksen Tilbakestill data mart](./media/Statistics.png)](./media/Statistics.png)</span><span class="sxs-lookup"><span data-stu-id="1f10f-124">[![Reset Data Mart dialog box](./media/Statistics.png)](./media/Statistics.png)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="1f10f-125">Integreringsforsøk</span><span class="sxs-lookup"><span data-stu-id="1f10f-125">Integration attempts</span></span>

<span data-ttu-id="1f10f-126">**Integreringsforsøk**-rutenettet viser hvor mange ganger systemet har forsøkt å integrere transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="1f10f-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="1f10f-127">Systemet fortsetter å prøve å integrere data i en periode med dager hvis de første få forsøkene ikke lykkes.</span><span class="sxs-lookup"><span data-stu-id="1f10f-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="1f10f-128">Du vil vite at data mart må tilbakestilles hvis antall forsøk er 8 eller mer, og hvis det er mange dimensjonskombinasjoner eller transaksjonsposter.</span><span class="sxs-lookup"><span data-stu-id="1f10f-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="1f10f-129">I så fall vil ikke dataene rapporteres.</span><span class="sxs-lookup"><span data-stu-id="1f10f-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="1f10f-130">Datastatus</span><span class="sxs-lookup"><span data-stu-id="1f10f-130">Data status</span></span>

<span data-ttu-id="1f10f-131">**Datastatus**-rutenettet gir en oversikt over transaksjoner, valutakurser og dimensjonsverdier i data mart.</span><span class="sxs-lookup"><span data-stu-id="1f10f-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="1f10f-132">Mange foreldede oppføringer angir at det har oppstått mange oppdateringer av postene.</span><span class="sxs-lookup"><span data-stu-id="1f10f-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="1f10f-133">Dette kan føre til at rapportgenereringstidene kan gå saktere.</span><span class="sxs-lookup"><span data-stu-id="1f10f-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="1f10f-134">Feiljusterte hovedkontokategorier</span><span class="sxs-lookup"><span data-stu-id="1f10f-134">Misaligned main account categories</span></span>

<span data-ttu-id="1f10f-135">Hvis du bruker en versjon som er eldre enn Microsoft Dynamics 365 for Finance and Operations Financial reporting versjon 7.2.1, må du kanskje tilbakestille data mart hvis du gir kontoer nytt navn og flytter kontoer mellom kontokategorier.</span><span class="sxs-lookup"><span data-stu-id="1f10f-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="1f10f-136">Disse handlingene kan føre til at hovedkontokategorier blir feiljustert.</span><span class="sxs-lookup"><span data-stu-id="1f10f-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="1f10f-137">**Feiljusterte hovedkontokategorier**-feltet viser om du opplever dette problemet.</span><span class="sxs-lookup"><span data-stu-id="1f10f-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="1f10f-138">Tilbakestille data mart i Finance and Operations Financial reporting versjon 7.2.6.0</span><span class="sxs-lookup"><span data-stu-id="1f10f-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="1f10f-139">Hvis du vil tilbakestille data mart i Finance and Operations Financial reporting versjon 7.2.6.0 og tidligere, går du til **Tilbakestill data mart**-dialogboksen, merker av for **Tilbakestill data mart** og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="1f10f-140">Du bør bare tilbakestille data mart under planlagt nedetid.</span><span class="sxs-lookup"><span data-stu-id="1f10f-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="1f10f-141">[![Avmerkingsboksen Tilbakestill data mart](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="1f10f-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="1f10f-142">Tilbakestille data mart og velge en årsak i Microsoft Dynamics 365 for Finance and Operations Financial reporting versjon 7.3.0</span><span class="sxs-lookup"><span data-stu-id="1f10f-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="1f10f-143">Hvis du finner ut at det kreves en tilbakestilling av data mart, merker du av for **Tilbakestill data mart**, og velger deretter en årsak i **Årsak**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1f10f-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="1f10f-144">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="1f10f-144">The following options are available:</span></span>

- <span data-ttu-id="1f10f-145">**Manglende eller ugyldige data** – Basert på statistikken har du fastslått at data kan mangle.</span><span class="sxs-lookup"><span data-stu-id="1f10f-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="1f10f-146">Før du fortsetter, anbefaler vi at du arbeider med støtte for å fastslå årsaken.</span><span class="sxs-lookup"><span data-stu-id="1f10f-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="1f10f-147">**Gjenopprett database** – Finance and Operations-databasen ble gjenopprettet, men databasen for data-mart for finansrapportering ble ikke gjenopprettet.</span><span class="sxs-lookup"><span data-stu-id="1f10f-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="1f10f-148">**Andre** – Du tilbakestiller data mart av en annen grunn.</span><span class="sxs-lookup"><span data-stu-id="1f10f-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="1f10f-149">Hvis du er redd for at det er et problem, kan du kontakte kundestøtte for å identifisere det.</span><span class="sxs-lookup"><span data-stu-id="1f10f-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

> [!NOTE]
> <span data-ttu-id="1f10f-150">Kontroller at alle eksisterende oppgaver har fullført integreringen før du fullfører trinnene.</span><span class="sxs-lookup"><span data-stu-id="1f10f-150">Verify that all existing tasks have finished integrating before you complete the steps.</span></span> <span data-ttu-id="1f10f-151">Du kan vise statusen for integreringen ved å velge **Verktøy** &gt; **Integreringsstatus**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-151">You can view the status of the integration by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="1f10f-152">Fjern brukere og firmaer</span><span class="sxs-lookup"><span data-stu-id="1f10f-152">Clear users and companies</span></span>

<span data-ttu-id="1f10f-153">Merk av for **Fjern brukere og firmaer** hvis du har gjenopprettet databasen, men deretter har gjort endringer i brukere eller selskaper.</span><span class="sxs-lookup"><span data-stu-id="1f10f-153">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="1f10f-154">Du bør sjeldent få behov for å merke av i denne boksen.</span><span class="sxs-lookup"><span data-stu-id="1f10f-154">You should rarely have to select this check box.</span></span>

<span data-ttu-id="1f10f-155">Når du er klar til å starte tilbakestillingen, velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-155">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="1f10f-156">Du blir bedt om å bekrefte at du er klar til å starte prosessen.</span><span class="sxs-lookup"><span data-stu-id="1f10f-156">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="1f10f-157">Legg merke til at finansrapportering ikke er tilgjengelig under tilbakestillingen og den første dataintegreringen som skjer etterpå.</span><span class="sxs-lookup"><span data-stu-id="1f10f-157">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="1f10f-158">Hvis du vil vise statusen for integreringen, velger du **Verktøy** &gt; **Integreringsstatus** for å se sist gang integreringen ble kjørt og statusen.</span><span class="sxs-lookup"><span data-stu-id="1f10f-158">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="1f10f-159">[![Vise statusen for integreringen](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="1f10f-159">[![View the status of the integration](./media/Integration.png)](./media/Integration.png)</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="1f10f-160">Tilbakestille data mart for finansrapportering for Finance and Operations Financial reporting versjon 7.0.10000.4 og nyere</span><span class="sxs-lookup"><span data-stu-id="1f10f-160">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="1f10f-161">Hvis du gjenoppretter Finance and Operations-databasen fra en sikkerhetskopi eller kopierer databasen fra et annet miljø, må du følge trinnene i denne delen for å sikre at data mart for finansrapportering bruker den gjenopprettede Finance and Operations-databasen på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="1f10f-161">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="1f10f-162">Fremgangsmåten i denne prosessen støttes for Microsoft Dynamics AX-programmet versjon 7.0.1 (mai 2016) (programbygg 7.0.1265.23014 og Financial reporting bygg 7.0.10000.4) og nyere.</span><span class="sxs-lookup"><span data-stu-id="1f10f-162">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="1f10f-163">Hvis du har en tidligere versjon av Finance and Operations, kan du kontakte kundestøtte for å få hjelp.</span><span class="sxs-lookup"><span data-stu-id="1f10f-163">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="1f10f-164">Eksportere rapportdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="1f10f-164">Export report definitions</span></span>

<span data-ttu-id="1f10f-165">Først gjør du følgende for å eksportere rapportutformingene fra Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="1f10f-165">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="1f10f-166">I Rapportutforming velger du **Firma** &gt; **Byggeblokkgrupper**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-166">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="1f10f-167">Velg byggeblokkgruppen du vil eksportere, og velg deretter **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-167">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1f10f-168">For Finance and Operations støttes bare én byggeblokkgruppe, **Standard**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-168">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="1f10f-169">Velg rapportdefinisjonene som skal eksporteres:</span><span class="sxs-lookup"><span data-stu-id="1f10f-169">Select the report definitions to export:</span></span>

    - <span data-ttu-id="1f10f-170">Hvis du vil eksportere alle rapportdefinisjonene og de tilknyttede byggeblokkene, velger du **Merk alle**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-170">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="1f10f-171">Hvis du vil eksportere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, velger du den aktuelle kategorien og velger deretter elementene som skal eksporteres.</span><span class="sxs-lookup"><span data-stu-id="1f10f-171">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="1f10f-172">Trykk og hold inne Ctrl-tasten for å velge flere varer i en kategori. Når du velger rapporter som skal eksporteres, velges de tilhørende radene, kolonnene, trærne og dimensjonssettene.</span><span class="sxs-lookup"><span data-stu-id="1f10f-172">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="1f10f-173">Velg **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-173">Select **Export**.</span></span>
5. <span data-ttu-id="1f10f-174">Skriv inn et filnavn, og velger en sikkert plassering der du vil lagre de eksporterte rapportdefinisjonene.</span><span class="sxs-lookup"><span data-stu-id="1f10f-174">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="1f10f-175">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-175">Select **Save**.</span></span>

<span data-ttu-id="1f10f-176">Du kan kopiere eller laste opp filen til en sikker plassering.</span><span class="sxs-lookup"><span data-stu-id="1f10f-176">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="1f10f-177">På denne måten kan filen importeres til et annet miljø senere.</span><span class="sxs-lookup"><span data-stu-id="1f10f-177">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="1f10f-178">Du finner informasjon om hvordan du bruker en Microsoft Azure-lagringskonto i [Overføre data med kommandolinjeverktøyet AzCopy](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="1f10f-178">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="1f10f-179">Microsoft tilbyr ingen lagringskonto som en del av Finance and Operations-avtalen.</span><span class="sxs-lookup"><span data-stu-id="1f10f-179">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="1f10f-180">Du må kjøpe en lagringskonto eller bruke en lagringskonto fra et eget Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f10f-180">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="1f10f-181">Vær oppmerksom på virkemåten til stasjon D på virtuelle Azure-maskiner (VM-er).</span><span class="sxs-lookup"><span data-stu-id="1f10f-181">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="1f10f-182">Ikke lagre de eksporterte byggeblokkgruppene permanent på stasjon D. Hvis du vil ha mer informasjon om midlertidige stasjoner, kan du se [Forstå den midlertidige stasjonen på virtuelle Windows Azure-maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="1f10f-182">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="1f10f-183">Stoppe tjenester</span><span class="sxs-lookup"><span data-stu-id="1f10f-183">Stop services</span></span>

<span data-ttu-id="1f10f-184">Følgende Microsoft Windows-tjenester vil ha åpne tilkoblinger til Finance and Operations-databasen.</span><span class="sxs-lookup"><span data-stu-id="1f10f-184">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="1f10f-185">Derfor må du bruke Microsoft Eksternt skrivebord til å koble til alle datamaskinene i miljøet, og deretter bruke services.msc til å stoppe disse tjenestene.</span><span class="sxs-lookup"><span data-stu-id="1f10f-185">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="1f10f-186">Webpubliseringstjenesten (for alle AOS-datamaskiner (Application Object-servere))</span><span class="sxs-lookup"><span data-stu-id="1f10f-186">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="1f10f-187">Partistyringstjenesten for Microsoft Dynamics 365 for Finance and Operations (bare for ikke-private AOS-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="1f10f-187">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="1f10f-188">Prosesstjenesten for Management Reporter 2012 (bare på Business intelligence [BI]-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="1f10f-188">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="1f10f-189">Tilbakestill</span><span class="sxs-lookup"><span data-stu-id="1f10f-189">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="1f10f-190">Last ned den siste MinorVersionDataUpgrade.zip-pakken</span><span class="sxs-lookup"><span data-stu-id="1f10f-190">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="1f10f-191">Last ned den siste MinorVersionDataUpgrade.zip-pakken.</span><span class="sxs-lookup"><span data-stu-id="1f10f-191">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="1f10f-192">For instruksjoner om hvordan du finner og laster ned riktig versjon av dataoppgraderingspakken, kan du se [Last ned den nyeste distribuerbare dataoppgraderingspakken](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span><span class="sxs-lookup"><span data-stu-id="1f10f-192">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="1f10f-193">En oppgradering er ikke nødvendig for å laste ned MinorVersionDataUpgrade.zip-pakken.</span><span class="sxs-lookup"><span data-stu-id="1f10f-193">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="1f10f-194">Du må derfor bare følge trinnene i delen "Last ned den nyeste distribuerbare dataoppgraderingspakken" i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="1f10f-194">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="1f10f-195">Du kan hoppe over alle de andre trinnene i emnet.</span><span class="sxs-lookup"><span data-stu-id="1f10f-195">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="1f10f-196">Kjøre skript på Finance and Operations-databasen</span><span class="sxs-lookup"><span data-stu-id="1f10f-196">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="1f10f-197">Kjør skriptene nedenfor på Finance and Operations-databasen (ikke mot finansrapporteringsdatabasen):</span><span class="sxs-lookup"><span data-stu-id="1f10f-197">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="1f10f-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="1f10f-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="1f10f-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="1f10f-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="1f10f-200">Disse skriptene bidrar til å sikre at innstillinger for brukere, roller og endringssporing er riktige.</span><span class="sxs-lookup"><span data-stu-id="1f10f-200">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="1f10f-201">Kjøre en Windows PowerShell-kommando for å tilbakestille databasen</span><span class="sxs-lookup"><span data-stu-id="1f10f-201">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="1f10f-202">På AOS-datamaskinen starter du Microsoft Windows PowerShell som administrator, og kjører følgende kommandoer for å tilbakestille integreringen mellom Finance and Operations og finansrapportering.</span><span class="sxs-lookup"><span data-stu-id="1f10f-202">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="1f10f-203">Her finner du en forklaring på parameterne i **Reset-DatamartIntegration**-kommandoen:</span><span class="sxs-lookup"><span data-stu-id="1f10f-203">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="1f10f-204">Gyldige verdier for **-Reason** er **SERVICING**, **BADDATA** og **OTHER**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-204">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="1f10f-205">Parameteren **-ReasonDetail** er fritekst.</span><span class="sxs-lookup"><span data-stu-id="1f10f-205">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="1f10f-206">Reason og reason detail blir registrert i telemetri / miljøovervåking.</span><span class="sxs-lookup"><span data-stu-id="1f10f-206">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="1f10f-207">Når du har kjørt kommandoene, får du spørsmål om å angi **Y** for å bekrefte at du vil tilbakestille databasen.</span><span class="sxs-lookup"><span data-stu-id="1f10f-207">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="1f10f-208">Starte tjenester på nytt</span><span class="sxs-lookup"><span data-stu-id="1f10f-208">Restart services</span></span>

<span data-ttu-id="1f10f-209">Bruk Services.msc til å starte tjenestene du stoppet tidligere:</span><span class="sxs-lookup"><span data-stu-id="1f10f-209">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="1f10f-210">Webpubliseringstjenesten (for alle AOS-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="1f10f-210">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="1f10f-211">Partistyringstjenesten for Microsoft Dynamics 365 for Finance and Operations (bare for ikke-private AOS-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="1f10f-211">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="1f10f-212">Prosesstjenesten for Management Reporter 2012 (bare for BI-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="1f10f-212">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="1f10f-213">Importere rapportdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="1f10f-213">Import report definitions</span></span>

<span data-ttu-id="1f10f-214">Importer rapportutformingene fra Rapportutforming ved hjelp av filen som ble opprettet under eksporten.</span><span class="sxs-lookup"><span data-stu-id="1f10f-214">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="1f10f-215">I Rapportutforming velger du **Firma** &gt; **Byggeblokkgrupper**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-215">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="1f10f-216">Velg byggeblokkgruppen du vil eksportere, og velg deretter **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-216">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1f10f-217">For Finance and Operations støttes bare én byggeblokkgruppe, **Standard**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-217">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="1f10f-218">Velg **Standard**-byggeblokken, og velg deretter **Importer**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-218">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="1f10f-219">Velg filen som inneholder de eksporterte rapportdefinisjonene, og velg deretter **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-219">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="1f10f-220">Velg rapportdefinisjonene som skal importeres, i dialogboksen **Importer**:</span><span class="sxs-lookup"><span data-stu-id="1f10f-220">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="1f10f-221">Hvis du vil importere alle rapportdefinisjonene og de tilknyttede byggeblokkene, velger du **Merk alle**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-221">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="1f10f-222">Hvis du vil importere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, merker du rapportene, radene, kolonnene, trærne eller dimensjonssettene som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="1f10f-222">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="1f10f-223">Velg **Import**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-223">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="1f10f-224">Tilbakestille data mart for finansrapportering for Finance and Operations (lokal)</span><span class="sxs-lookup"><span data-stu-id="1f10f-224">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="1f10f-225">Be alle brukerne om å avslutte Rapportutforming og Finansrapportering-området i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1f10f-225">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="1f10f-226">Kjør følgende skript på Finansrapportering-databasen (MRDB).</span><span class="sxs-lookup"><span data-stu-id="1f10f-226">Run the following script against the Financial reporting database (MRDB).</span></span>

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

3. <span data-ttu-id="1f10f-227">Avkort eller slett alle postene fra tabellen FINANCIALREPORTS i Finance and Operations-databasen (AXDB).</span><span class="sxs-lookup"><span data-stu-id="1f10f-227">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="1f10f-228">Avkort eller slett alle postene fra tabellen FINANCIALREPORTVERSION hvis denne tabellen finnes i Finance and Operations-databasen.</span><span class="sxs-lookup"><span data-stu-id="1f10f-228">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="1f10f-229">Hvis tabellen ikke finnes i Finance and Operations-databasen, hopper du over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="1f10f-229">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="1f10f-230">Kjør **ResetDatamart**-skriptet på Finansrapportering-databasen.</span><span class="sxs-lookup"><span data-stu-id="1f10f-230">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="1f10f-231">Dette skriptet deaktiverer data mart-integreringen, sletter alle data mart-dataene og aktiverer deretter data mart-integreringen på nytt.</span><span class="sxs-lookup"><span data-stu-id="1f10f-231">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

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

6. <span data-ttu-id="1f10f-232">Etter tilbakestillingen, kan du bekrefte den nye datainnlastingen manuelt ved å kjøre følgende spørring mot Finansrapportering-databasen.</span><span class="sxs-lookup"><span data-stu-id="1f10f-232">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="1f10f-233">Kontroller at alle rader har verdien **LastRunTime**, og at **StateType** er satt til **5**.</span><span class="sxs-lookup"><span data-stu-id="1f10f-233">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="1f10f-234">En **StateType**-verdi på **5** angir at dataene ble lastet inn på nytt.</span><span class="sxs-lookup"><span data-stu-id="1f10f-234">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="1f10f-235">En verdi på **7** angir en feilstatus.</span><span class="sxs-lookup"><span data-stu-id="1f10f-235">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="1f10f-236">Noen ganger har organisasjonshierarkikartet denne tilstanden første gang den kjøres.</span><span class="sxs-lookup"><span data-stu-id="1f10f-236">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="1f10f-237">Feilstatusen må imidlertid løses automatisk.</span><span class="sxs-lookup"><span data-stu-id="1f10f-237">However, the faulted state but should be automatically resolved.</span></span>

