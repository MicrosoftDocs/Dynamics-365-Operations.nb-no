---
title: Rapport for sammenligning av lagervarepriser
description: Lær hvordan du genererer rapport for sammenligning av lagervarepriser og deretter bla gjennom og/eller eksportere resultatet.
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 73e43a685f390fd718028de6add0370dfcd6cf3b
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759646"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="df4eb-103">Rapport for sammenligning av lagervarepriser</span><span class="sxs-lookup"><span data-stu-id="df4eb-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df4eb-104">Dette emnet forklarer hvordan du kjører en rapport for **sammenligning av lagervarepriser** og gjør utdataene tilgjengelig digitalt, enten som en interaktiv side i Dynamics 365 Supply Chain Management eller som et eksportert dokument i et av flere formater.</span><span class="sxs-lookup"><span data-stu-id="df4eb-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="df4eb-105">Når du viser rapporten i nettleseren, justeres kolonner og aggregatsaldoer dynamisk, avhengig av det konfigurerte oppsettet.</span><span class="sxs-lookup"><span data-stu-id="df4eb-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="df4eb-106">Du kan sortere resultatene, filtrere dem, drille ned til dataene og mye mer.</span><span class="sxs-lookup"><span data-stu-id="df4eb-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="df4eb-107">Rapportresultater lagres i dataenheten **Sammenlign varepriser**, slik at du kan filtrere og eksportere resultatene til et format som for eksempel CSV eller Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="df4eb-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="df4eb-108">Rapporten for **sammenligning av lagervarepriser** er nyttig i tilfeller der utdataene inneholder mange linjer.</span><span class="sxs-lookup"><span data-stu-id="df4eb-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="df4eb-109">Utdataene vil for eksempel inneholde mange linjer hvis du har mer enn 40 000 varer som inneholder en uavsluttet varepris i kostversjonen.</span><span class="sxs-lookup"><span data-stu-id="df4eb-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="df4eb-110">Aktivere sammenligning av lagervarepriser</span><span class="sxs-lookup"><span data-stu-id="df4eb-110">Enable compare item prices storage</span></span>

<span data-ttu-id="df4eb-111">Før du kan bruke denne funksjonen, må du aktivere den i systemet.</span><span class="sxs-lookup"><span data-stu-id="df4eb-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="df4eb-112">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="df4eb-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="df4eb-113">Her vises funksjonen som:</span><span class="sxs-lookup"><span data-stu-id="df4eb-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="df4eb-114">**Modul** - Kostnadsstyring</span><span class="sxs-lookup"><span data-stu-id="df4eb-114">**Module** - Cost management</span></span>
- <span data-ttu-id="df4eb-115">**Funksjonsnavn** – Sammenligning av lagervarepriser</span><span class="sxs-lookup"><span data-stu-id="df4eb-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="df4eb-116">Generer en rapport for sammenligning av lagervarepriser</span><span class="sxs-lookup"><span data-stu-id="df4eb-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="df4eb-117">Følg denne fremgangsmåten for å generere og lagre en rapport for **sammenligning av lagervarepriser**:</span><span class="sxs-lookup"><span data-stu-id="df4eb-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="df4eb-118">Gå til **Kostnadsstyring > Forespørsler og rapporter > Forhåndsbestemte kostnadsrapporter > Sammenligning av lagervarepriser**.</span><span class="sxs-lookup"><span data-stu-id="df4eb-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="df4eb-119">Velg **Ny** for å åpne ruten **Sammenlign varepriser**.</span><span class="sxs-lookup"><span data-stu-id="df4eb-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="df4eb-120">Angi følgende alternativer for å definere hvilke priser som skal sammenlignes i rapporten:</span><span class="sxs-lookup"><span data-stu-id="df4eb-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="df4eb-121">På hurtigfanen **Parametere** gir du rapporten et **navn** og bruker feltene i delene **Ventende priser som skal sammenlignes** og **Priser som brukes for sammenligning** til å definere hvilke priser og datoer som skal sammenlignes.</span><span class="sxs-lookup"><span data-stu-id="df4eb-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="df4eb-122">I hurtigfanen **Poster som skal inkluderes** definerer du filtre og betingelser for å definere hvilke data som skal tas med i rapporten.</span><span class="sxs-lookup"><span data-stu-id="df4eb-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="df4eb-123">På hurtigfanen **Kjør i bakgrunnen** definerer du hvordan, når og frekvensen for når du ønsker å generere rapporten.</span><span class="sxs-lookup"><span data-stu-id="df4eb-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="df4eb-124">Denne rapporten blir alltid utført som en del av en satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="df4eb-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="df4eb-125">Velg **OK** for å bruke innstillingene og lukke ruten.</span><span class="sxs-lookup"><span data-stu-id="df4eb-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="df4eb-126">Når den satsvise jobben er fullført, vil den vises på siden **Sammenligning av lagervarepriser**.</span><span class="sxs-lookup"><span data-stu-id="df4eb-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="df4eb-127">Det kan hende at du må oppdatere siden for å se rapporten.</span><span class="sxs-lookup"><span data-stu-id="df4eb-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="df4eb-128">Se nærmere på rapporten for sammenligning av lagervarepriser</span><span class="sxs-lookup"><span data-stu-id="df4eb-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="df4eb-129">Når du har generert en rapport, kan du vise og utforske den når som helst på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="df4eb-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="df4eb-130">Gå til **Kostnadsstyring > Forespørsler og rapporter > Forhåndsbestemte kostnadsrapporter > Sammenligning av lagervarepriser**.</span><span class="sxs-lookup"><span data-stu-id="df4eb-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="df4eb-131">Velg en rapport fra listen.</span><span class="sxs-lookup"><span data-stu-id="df4eb-131">Select a report from the list.</span></span>

1. <span data-ttu-id="df4eb-132">Gjør ett av følgende:</span><span class="sxs-lookup"><span data-stu-id="df4eb-132">Do one of the following:</span></span>

    - <span data-ttu-id="df4eb-133">Velg **Oversikt** for å få en oversikt over rapportresultatene.</span><span class="sxs-lookup"><span data-stu-id="df4eb-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="df4eb-134">Velg **Vis detaljer** for å få en mer detaljert visning av rapporten</span><span class="sxs-lookup"><span data-stu-id="df4eb-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="df4eb-135">Når den valgte visningen åpnes, kan du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="df4eb-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="df4eb-136">Velg nesten hvilken som helst kolonneoverskrift for å sortere eller filtrere tabellen etter verdier i denne kolonnen, på samme måte som med de fleste standardskjemaene i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="df4eb-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="df4eb-137">Merk at du ikke kan sortere eller filtrere kolonnen **Nettoprisendring i prosent** fordi det er et beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="df4eb-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="df4eb-138">Velg **Dimensjonsvisningvisning** for å åpne en rute der du kan velge hvilken dimensjonskolonne som skal tas med i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="df4eb-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="df4eb-139">Sett **Lagre oppsett** til **Ja** hvis du vil lagre disse innstillingene slik at de blir bevart neste gang du åpner rapporten.</span><span class="sxs-lookup"><span data-stu-id="df4eb-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="df4eb-140">Velg **OK** for å bruke innstillingene og lukke.</span><span class="sxs-lookup"><span data-stu-id="df4eb-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="df4eb-141">Velg en hvilken som helst rad i skjemaet, og velg deretter **Vis detaljer** for å se mer informasjon om den valgte varen.</span><span class="sxs-lookup"><span data-stu-id="df4eb-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="df4eb-142">Du kan drille ned til dataene herfra.</span><span class="sxs-lookup"><span data-stu-id="df4eb-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="df4eb-143">Velg en hvilken som helst rad i skjemaet, og velg deretter **Vis sammenligningsdiagram** for å se en interaktiv grafisk fremstilling av resultatene slik de er relatert til det valgte elementet.</span><span class="sxs-lookup"><span data-stu-id="df4eb-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="df4eb-144">Du kan utforske disse resultatene ved å velge ulike grafiske elementer i diagrammet og diagramforklaringen.</span><span class="sxs-lookup"><span data-stu-id="df4eb-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="df4eb-145">Velg en hvilken som helst rad i skjemaet, og velg deretter **Vis beregningsdetaljer** for å se mer informasjon om beregninger relatert til den valgte varen.</span><span class="sxs-lookup"><span data-stu-id="df4eb-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="df4eb-146">Du kan drille ned til dataene herfra.</span><span class="sxs-lookup"><span data-stu-id="df4eb-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="df4eb-147">Eksportere rapporten for sammenligning av lagervarepriser</span><span class="sxs-lookup"><span data-stu-id="df4eb-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="df4eb-148">Hver rapport du genererer, lagres i dataenheten **Sammenlign varepriser**.</span><span class="sxs-lookup"><span data-stu-id="df4eb-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="df4eb-149">Du kan bruke standardfunksjonene i Supply Chain Management til å eksportere data fra denne enheten til alle støttede dataformater, inkludert CSV eller Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="df4eb-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="df4eb-150">Nedenfor vises et eksempel på hvordan du eksporterer en rapport for **sammenligning av lagervarepriser**:</span><span class="sxs-lookup"><span data-stu-id="df4eb-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="df4eb-151">Gå til **Systemadministrasjon > Arbeidsområder > Databehandling**.</span><span class="sxs-lookup"><span data-stu-id="df4eb-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="df4eb-152">Velg **Eksporter**-knappen i delen **Databehandling**.</span><span class="sxs-lookup"><span data-stu-id="df4eb-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="df4eb-153">Siden **Eksporers** åpnes, som du vil bruke til å konfigurere eksportjobben.</span><span class="sxs-lookup"><span data-stu-id="df4eb-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="df4eb-154">Start ved å gi jobben et **gruppenavn**.</span><span class="sxs-lookup"><span data-stu-id="df4eb-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="df4eb-155">I delen **Valgte enheter** velger du **Legg til enhet** for å åpne en dialogboks der du kan angi følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="df4eb-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="df4eb-156">**Enhetsnavn** – Velg **Sammenlign varepriser**.</span><span class="sxs-lookup"><span data-stu-id="df4eb-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="df4eb-157">**Måldataformat** – Velg formatet du vil eksportere til.</span><span class="sxs-lookup"><span data-stu-id="df4eb-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="df4eb-158">Velg **Legg til** for å legge til en ny rad, og velg deretter **Lukk** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="df4eb-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="df4eb-159">Vanligvis eksporterer du én rapport om gangen.</span><span class="sxs-lookup"><span data-stu-id="df4eb-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="df4eb-160">Hvis du vil gjøre dette, definerer du et **filter** for raden du nettopp la til, i **Forespørsel**-ruten.</span><span class="sxs-lookup"><span data-stu-id="df4eb-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="df4eb-161">På denne måten kan du definere hvilke rapporter fra enheten **Sammenlign varepriser** som du vil inkludere i eksporten.</span><span class="sxs-lookup"><span data-stu-id="df4eb-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="df4eb-162">Angi følgende filteralternativer for å eksportere en enkelt rapport:</span><span class="sxs-lookup"><span data-stu-id="df4eb-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="df4eb-163">I kategorien **Område** velger du **Legg til** for å legge til en ny rad.</span><span class="sxs-lookup"><span data-stu-id="df4eb-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="df4eb-164">Sett **Tabell** til **Sammenlign varepriser**.</span><span class="sxs-lookup"><span data-stu-id="df4eb-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="df4eb-165">Sett **Avledet tabell** til **Sammenlign varepriser**.</span><span class="sxs-lookup"><span data-stu-id="df4eb-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="df4eb-166">Sett **Felt** til feltet som du vil filtrere etter.</span><span class="sxs-lookup"><span data-stu-id="df4eb-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="df4eb-167">Vanligvis vil du bruke **Kjørenavn** eller **Kjøretid**.</span><span class="sxs-lookup"><span data-stu-id="df4eb-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="df4eb-168">Angi **Kriterier** til verdien fra det valgte feltet som du vil søke etter (enten navnet på rapporten eller klokkeslettet da rapporten ble generert).</span><span class="sxs-lookup"><span data-stu-id="df4eb-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="df4eb-169">Hvis det er nødvendig, legger du til flere rader i **Område**-tabellen til du har unikt angitt hvilken rapport du vil søke etter.</span><span class="sxs-lookup"><span data-stu-id="df4eb-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="df4eb-170">Velg **OK** for å lagre innstillingene og lukke.</span><span class="sxs-lookup"><span data-stu-id="df4eb-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="df4eb-171">Velg **Lagre** for å lagre eksportoppsettet.</span><span class="sxs-lookup"><span data-stu-id="df4eb-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="df4eb-172">Åpne kategorien **Eksportalternativer**, og velg **Eksporter nå** for å generere eksportfilen.</span><span class="sxs-lookup"><span data-stu-id="df4eb-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="df4eb-173">Siden **Kjøringssammendrag** åpnes, der du kan se statusen for eksportjobben og en liste over enheter som ble eksportert.</span><span class="sxs-lookup"><span data-stu-id="df4eb-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="df4eb-174">Velg enheten **Sammenlign varepriser** som er oppført i området **Behandlingsstatus for enhet**, og velg deretter **Last ned fil** for å laste ned dataene som er eksportert fra denne enheten.</span><span class="sxs-lookup"><span data-stu-id="df4eb-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="df4eb-175">Hvis du vil ha mer informasjon om hvordan du bruker databehandling til å eksportere data, se [Oversikt over dataimport- og -eksportjobber](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="df4eb-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
