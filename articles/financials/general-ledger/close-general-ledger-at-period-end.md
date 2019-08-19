---
title: Lukke økonomimodulen ved periodeslutt
description: Dette emnet beskriver oppgavene som vanligvis utføres når du utfører en periodeavslutning for økonomimodulen.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eca533ed1621ec3507d8510f75842c0f0165275
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839551"
---
# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="72fbc-103">Lukke økonomimodulen ved periodeslutt</span><span class="sxs-lookup"><span data-stu-id="72fbc-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72fbc-104">Dette emnet beskriver oppgavene som vanligvis utføres når du utfører en periodeavslutning for økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="72fbc-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="72fbc-105">I Økonomimodul kan du fullføre avslutningsprosedyrer for en periode eller et år.</span><span class="sxs-lookup"><span data-stu-id="72fbc-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="72fbc-106">Avslutningsprosesser gjør systemet klart for en ny periode.</span><span class="sxs-lookup"><span data-stu-id="72fbc-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="72fbc-107">Hvis du vil klargjøre systemet for et nytt år, må du kjøre årsavslutningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="72fbc-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="72fbc-108">Hver organisasjon har forskjellige prosesser og trinn som utføres på slutten av en periode.</span><span class="sxs-lookup"><span data-stu-id="72fbc-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="72fbc-109">Her er noen av de valgfrie trinnene for periodeslutt:</span><span class="sxs-lookup"><span data-stu-id="72fbc-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="72fbc-110">Fullfør alle oppgavene for alle andre moduler, for eksempel Kunder, Leverandører og Beholdning.</span><span class="sxs-lookup"><span data-stu-id="72fbc-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="72fbc-111">Kontroller at alle journaler er postert.</span><span class="sxs-lookup"><span data-stu-id="72fbc-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="72fbc-112">Kjør revaluering av utenlandsk valuta for å generere eventuelle urealiserte fortjeneste- eller tapsbeløp.</span><span class="sxs-lookup"><span data-stu-id="72fbc-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="72fbc-113">Utlign transaksjoner for hver finanskonto.</span><span class="sxs-lookup"><span data-stu-id="72fbc-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="72fbc-114">Behandle eventuelle nødvendige fordelinger.</span><span class="sxs-lookup"><span data-stu-id="72fbc-114">Process any required allocations.</span></span>
-   <span data-ttu-id="72fbc-115">Poster periodesluttjusteringer manuelt.</span><span class="sxs-lookup"><span data-stu-id="72fbc-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="72fbc-116">Journalfør transaksjoner, og se gjennom **Finansjournal**-rapporten.</span><span class="sxs-lookup"><span data-stu-id="72fbc-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="72fbc-117">Foreta en konsolidering ved å bruke et konsolideringsfirma eller Finansrapportering.</span><span class="sxs-lookup"><span data-stu-id="72fbc-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="72fbc-118">Generer regnskapsoppgjør ved periodeslutt ved å bruke Finansrapportering.</span><span class="sxs-lookup"><span data-stu-id="72fbc-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="72fbc-119">Sett finansperioder til **På vent**, slik at ingen ytterligere postering forekommer.</span><span class="sxs-lookup"><span data-stu-id="72fbc-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="72fbc-120">Du kan også begrense en periode til en bestemt brukergruppe mens periodesluttaktiviteter forekommer, slik at du oppnår bedre kontroll.</span><span class="sxs-lookup"><span data-stu-id="72fbc-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="72fbc-121">Det er ikke lurt å sette perioder til **Lukket permanent**, fordi du kan ikke åpne en periode som er lukket, på nytt.</span><span class="sxs-lookup"><span data-stu-id="72fbc-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="72fbc-122">Arbeidsområdet Regnskapsperiodeavslutning kan brukes til å ordne og spore oppgavene som kreves for forskjellige prosesser for periodeslutt.</span><span class="sxs-lookup"><span data-stu-id="72fbc-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="72fbc-123">Hvis du vil ha mer informasjon, kan du se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="72fbc-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="72fbc-124">Arbeidsområde for regnskapsperiodeavslutning</span><span class="sxs-lookup"><span data-stu-id="72fbc-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="72fbc-125">Årsavslutning</span><span class="sxs-lookup"><span data-stu-id="72fbc-125">Year end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="72fbc-126">Lukke masseregnskapsperiode</span><span class="sxs-lookup"><span data-stu-id="72fbc-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)




