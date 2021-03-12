---
title: Klargjøre en juridisk enhet for konsolideringsprosessen
description: Under en konsolidering samler du transaksjoner fra flere sett med kontoer for juridisk enhet i ett sett med kontoer for juridisk enhet. Dette emnet beskriver hvordan du klargjør en juridisk enhet for konsolidering.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: f6fce69724945448f961769dd383d1047a5d13c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990314"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="94878-104">Klargjøre en juridisk enhet for konsolideringsprosessen</span><span class="sxs-lookup"><span data-stu-id="94878-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94878-105">Under en konsolidering samler du transaksjoner fra flere sett med kontoer for juridisk enhet i ett sett med kontoer for juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="94878-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="94878-106">Dette emnet beskriver hvordan du klargjør en juridisk enhet for konsolidering.</span><span class="sxs-lookup"><span data-stu-id="94878-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="94878-107">Vi anbefaler at du bruker Management Reporter for Microsoft Dynamics 365 Finance til å kombinere de økonomiske resultatene for flere juridiske enheter i et konsolidert format.</span><span class="sxs-lookup"><span data-stu-id="94878-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="94878-108">Management Reporter lar deg opprette konsoliderte finansrapporter på tvers av juridiske enheter, bruke Excel til å importere konsolideringsdata fra andre kilder og omsette beløp til et hvilket som helst antall rapporteringsvalutaer uten å måtte kjøre konsolideringsprosessen i Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="94878-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="94878-109">Du kan skrive ut rapporter, for eksempel regnskapsoppgjør, fra den konsoliderte juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="94878-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="94878-110">Du kan imidlertid ikke bruke den konsoliderte juridiske enheten for daglige transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="94878-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="94878-111">Du kan konsolidere data fra juridiske enheter som bruker andre databaser enn den konsoliderte juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="94878-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="94878-112">Denne konsolideringsprosessen kalles en *importkonsolidering*.</span><span class="sxs-lookup"><span data-stu-id="94878-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="94878-113">Alternativt kan juridiske enheter bruke den samme databasen som den konsoliderte juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="94878-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="94878-114">Denne konsolideringsprosessen kalles en *online konsolidering*.</span><span class="sxs-lookup"><span data-stu-id="94878-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="94878-115">Den konsoliderte juridiske enheten samler resultatene og saldoene for datterselskapene.</span><span class="sxs-lookup"><span data-stu-id="94878-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="94878-116">Hvis du vil klargjøre en konsolidert juridisk enhet for en konsolidering, følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="94878-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="94878-117">Gå til **Økonomimodul \> Oppsett \> Organisasjon \> Juridiske enheter**.</span><span class="sxs-lookup"><span data-stu-id="94878-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="94878-118">Velg **Ny** for å opprette den nye juridiske enheten som skal være den konsoliderte juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="94878-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="94878-119">Merk av for **Bruk for finanskonsolideringsprosess**, og angi deretter informasjon om den konsoliderte juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="94878-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="94878-120">Sørg for å angi denne informasjon nøyaktig slik du vil at den skal vises på regnskapsoppgjør for den konsoliderte juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="94878-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="94878-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="94878-121">Close the page.</span></span>
5. <span data-ttu-id="94878-122">Velg den konsoliderte juridiske enheten i feltet i øvre høyre hjørne på siden, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="94878-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="94878-123">Gå til **Økonomimodul \> Oppsett \> Finans**.</span><span class="sxs-lookup"><span data-stu-id="94878-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="94878-124">Velg kontoplanen, den økonomiske kalenderen, regnskapsvalutaen, en valgfri rapporteringsvalutaen og standard valutakurstype for den konsoliderte juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="94878-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="94878-125">Gå til **Økonomimodul \> Oppsett \> Valuta \> Valutakurser**.</span><span class="sxs-lookup"><span data-stu-id="94878-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="94878-126">Definer valutakurser i relevante perioder for valutaene for de juridiske enhetene for datterselskap.</span><span class="sxs-lookup"><span data-stu-id="94878-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="94878-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="94878-127">Close the page.</span></span>
11. <span data-ttu-id="94878-128">Hvis den konsoliderte juridiske enheten har datterselskaper med utenlandske valutaer, følger du disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="94878-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="94878-129">Gå til **Økonomimodul \> Oppsett \> Postering \> Kontoer for automatiske transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="94878-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="94878-130">I feltet **Posteringstype** velger du en passende konto:</span><span class="sxs-lookup"><span data-stu-id="94878-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="94878-131">Hvis den juridiske enheten har utenlandske datterselskaper som er økonomisk eller driftsmessig avhengige av den overordnede juridiske enheten, velger du en passende konto for posteringstypen **Resultatkonto for konsolideringsdifferanser**.</span><span class="sxs-lookup"><span data-stu-id="94878-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="94878-132">Hvis du konsoliderer et datterselskap som er økonomisk og driftsmessig uavhengig av den overordnede juridiske enheten, eller en juridisk enhet som inneholder resultatene av flere datterselskaper som er økonomisk og driftsmessig uavhengige av den overordnede juridiske enheten, og hvis du bruker oversettingsmetoder til å konsolidere dataene, velger du en aktuell konto for posteringstypen **Balansekonto for konsolideringsdifferanser**.</span><span class="sxs-lookup"><span data-stu-id="94878-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="94878-133">I **Hovedkonto**-feltet velger du hovedkontoene som skal brukes til justeringer av revaluering av utenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="94878-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="94878-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="94878-134">Close the page.</span></span>

    <span data-ttu-id="94878-135">Hvis du oppretter den konsoliderte juridiske enheten tidlig i en periode, kan du revaluere beløpene i utenlandsk valuta etter hvert som valutakurser endres i konsolideringsperioden.</span><span class="sxs-lookup"><span data-stu-id="94878-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="94878-136">Den konsoliderte juridiske enheten er nå definert for den periodiske jobben **Konsolider**.</span><span class="sxs-lookup"><span data-stu-id="94878-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="94878-137">Du kan enten gjøre en importkonsolidering eller en online konsolidering.</span><span class="sxs-lookup"><span data-stu-id="94878-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="94878-138">Hvis du vil gjøre en importkonsolidering, kan du gå til **Økonomimodul \> Periodisk \> Konsolider \> Konsolider \[Importer fra\]**.</span><span class="sxs-lookup"><span data-stu-id="94878-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="94878-139">Hvis du vil gjøre en online konsolidering, kan du gå til **Økonomimodul \> Periodisk \> Konsolider \> Konsolider \[Online\]**.</span><span class="sxs-lookup"><span data-stu-id="94878-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="94878-140">Før du kan behandle konsolideringen, må du klargjøre de juridiske enhetene for datterselskap for konsolidering.</span><span class="sxs-lookup"><span data-stu-id="94878-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="94878-141">Hvis du vil ha mer informasjon, kan du se [Definere en juridisk enhet for datterselskap for konsolidering](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="94878-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>
