---
title: Eksportere data for et datterselskap til filer
description: Dette emnet beskriver hvordan du forbereder å eksportere data fra Microsoft Dynamics 365 Finance og deretter importerer dem til en konsolidert juridisk enhet.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: bae0a28c59f327e47378eef6392d5e304bbde9a8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826184"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="d38e7-103">Eksportere data for et datterselskap til filer</span><span class="sxs-lookup"><span data-stu-id="d38e7-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d38e7-104">Du bruker siden **Eksport** (**Systemadministrasjon \> Arbeidsområder \> Importer/Eksporter**) til å forberede eksport av data fra datterselskapene til filer som deretter kan importeres til en konsolidert juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="d38e7-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="d38e7-105">Hvis du vil ha mer informasjon om import- og eksportprosesser, se [Oversikt over dataimport- og -eksportjobber](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="d38e7-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="d38e7-106">Opprette en juridisk enhet for konsolideringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="d38e7-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="d38e7-107">Hvis du vil ha informasjon om hvordan du oppretter juridiske enheter, kan du se [Opprette en juridisk enhet](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span><span class="sxs-lookup"><span data-stu-id="d38e7-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="d38e7-108">Hvis du vil ha mer informasjon, kan du se [Klargjøre en juridisk enhet for bruk i konsolideringsprosessen](prepare-company-for-consolidation.md), og [Definere en juridisk enhet for datterselskap for konsolidering](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="d38e7-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="d38e7-109">Gå til **Konsolideringer \> Eksport av firmasaldoer**.</span><span class="sxs-lookup"><span data-stu-id="d38e7-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="d38e7-110">På siden **Eksport av firmasaldoer**, i kategorien **Vilkår**, angir du detaljene for konsolideringen ved å angi følgende felt.</span><span class="sxs-lookup"><span data-stu-id="d38e7-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="d38e7-111">Felt</span><span class="sxs-lookup"><span data-stu-id="d38e7-111">Field</span></span>                             | <span data-ttu-id="d38e7-112">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d38e7-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="d38e7-113">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="d38e7-113">Main account</span></span>                      | <span data-ttu-id="d38e7-114">Angi kontoene som skal konsolideres.</span><span class="sxs-lookup"><span data-stu-id="d38e7-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="d38e7-115">Hvis du vil inkludere alle kontoene, lar du dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="d38e7-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="d38e7-116">Bruke konsolideringskonto</span><span class="sxs-lookup"><span data-stu-id="d38e7-116">Use consolidation account</span></span>         | <span data-ttu-id="d38e7-117">Hvis du har angitt konsolideringskontoer, setter du dette alternativet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d38e7-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="d38e7-118">Velg konsernkonto fra</span><span class="sxs-lookup"><span data-stu-id="d38e7-118">Select consolidation account from</span></span> | <span data-ttu-id="d38e7-119">Velg enten **Hovedkonto** eller **Konsolideringskontogruppe**.</span><span class="sxs-lookup"><span data-stu-id="d38e7-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="d38e7-120">Konsernkontogruppe</span><span class="sxs-lookup"><span data-stu-id="d38e7-120">Consolidation account group</span></span>       | <span data-ttu-id="d38e7-121">Velg en konsolideringskontogruppe for konsolideringskontoen som du valgte.</span><span class="sxs-lookup"><span data-stu-id="d38e7-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="d38e7-122">Konsolideringsperiode</span><span class="sxs-lookup"><span data-stu-id="d38e7-122">Consolidation period</span></span>              | <span data-ttu-id="d38e7-123">Angi "fra"- og "til"-datoer for konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="d38e7-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="d38e7-124">Inkluder faktiske beløp</span><span class="sxs-lookup"><span data-stu-id="d38e7-124">Include actual amounts</span></span>            | <span data-ttu-id="d38e7-125">Sett dette alternativet til **Ja** for å inkludere faktiske beløp.</span><span class="sxs-lookup"><span data-stu-id="d38e7-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="d38e7-126">Inkluder budsjettbeløp</span><span class="sxs-lookup"><span data-stu-id="d38e7-126">Include budget amounts</span></span>            | <span data-ttu-id="d38e7-127">Sett dette alternativet til **Ja** for å inkludere budsjettbeløp i konsolideringer.</span><span class="sxs-lookup"><span data-stu-id="d38e7-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="d38e7-128">Budsjettmodeller</span><span class="sxs-lookup"><span data-stu-id="d38e7-128">Budget models</span></span>                     | <span data-ttu-id="d38e7-129">Angi budsjettmodellen som skal tas med.</span><span class="sxs-lookup"><span data-stu-id="d38e7-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="d38e7-130">Angi detaljene for konsolideringen i kategorien **Finansdimensjoner**:</span><span class="sxs-lookup"><span data-stu-id="d38e7-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="d38e7-131">Angi finansdimensjonsinformasjonen som skal overføres fra transaksjonene i kontoene i datterselskapet, til transaksjonene i den konsoliderte juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="d38e7-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="d38e7-132">Velg finansdimensjonene i listen.</span><span class="sxs-lookup"><span data-stu-id="d38e7-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="d38e7-133">Identifiser riktig spesifikasjon for hver finansdimensjon som konsolideres.</span><span class="sxs-lookup"><span data-stu-id="d38e7-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="d38e7-134">De tilgjengelige alternativene er **Dimensjon**, **Gruppedimensjon**, **Firmakontoer** og **Konto**.</span><span class="sxs-lookup"><span data-stu-id="d38e7-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="d38e7-135">Med alternativet for **Gruppedimensjon** kan du definere dimensjonsverdien som brukes av gruppen med firmaer som konsolideres.</span><span class="sxs-lookup"><span data-stu-id="d38e7-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="d38e7-136">Angi segmentrekkefølgen du vil konsolidere i.</span><span class="sxs-lookup"><span data-stu-id="d38e7-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="d38e7-137">I kategorien **Juridiske enheter** følger du disse trinnene for å angi den juridiske enheten du eksporterer:</span><span class="sxs-lookup"><span data-stu-id="d38e7-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="d38e7-138">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d38e7-138">Select **New**.</span></span>
    2. <span data-ttu-id="d38e7-139">I feltet **Kilde for juridisk enhet** angir du den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="d38e7-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="d38e7-140">Hvis de samme kriteriene gjelder for flere datterselskaper som er i samme databaser, kan du overføre data fra disse datterselskapene til separate eksportfiler i én enkelt operasjon.</span><span class="sxs-lookup"><span data-stu-id="d38e7-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="d38e7-141">Opprett en linje for hver juridiske enhet for datterselskap med kontoer som skal eksporteres til filer.</span><span class="sxs-lookup"><span data-stu-id="d38e7-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="d38e7-142">Disse filene vil senere bli importert til den konsoliderte juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="d38e7-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="d38e7-143">Angi navnet på selskapet og navnet på eksportfilen som opprettes under eksportprosessen, for hvert datterselskap.</span><span class="sxs-lookup"><span data-stu-id="d38e7-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="d38e7-144">I feltet **Kontotypen for konverteringsavvik** velger du **Resultat** eller **Balanse**.</span><span class="sxs-lookup"><span data-stu-id="d38e7-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="d38e7-145">Angi et filnavn for eksportfilen som skal opprettes.</span><span class="sxs-lookup"><span data-stu-id="d38e7-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="d38e7-146">Velg **OK** for å kjøre eksporten.</span><span class="sxs-lookup"><span data-stu-id="d38e7-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="d38e7-147">Når eksporten er fullført, får du en melding som viser hvor mange poster som ble lagret i hver fil.</span><span class="sxs-lookup"><span data-stu-id="d38e7-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="d38e7-148">Du kan deretter importere filene til den konsoliderte juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="d38e7-148">You can then import the files into the consolidated legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]