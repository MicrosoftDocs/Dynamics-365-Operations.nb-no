---
title: Journalføre posterte journaloppføringer
description: Denne fremgangsmåten viser hvordan du journalfører posterte journaloppføringer.
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f50ee568df492bcd811d2fefb1784bb55b50384b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145058"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="ad440-103">Journalføre posterte journaloppføringer</span><span class="sxs-lookup"><span data-stu-id="ad440-103">Journalize posted journal entries</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad440-104">Denne fremgangsmåten viser hvordan du journalfører posterte journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="ad440-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="ad440-105">Denne prosedyren bruker demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="ad440-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="ad440-106">I **Navigasjonsrute** går du til **Moduler > Økonomimodul > Finansoppsett > Parametere for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="ad440-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="ad440-107">Feltet **Utvidet finansjournal** kan settes til Ja eller Nei.</span><span class="sxs-lookup"><span data-stu-id="ad440-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="ad440-108">Hvis Ja, blir rapportutdataene forskjellige.</span><span class="sxs-lookup"><span data-stu-id="ad440-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="ad440-109">Velg om perioden kan lukkes hvis journalføringsprosessen ikke har blitt kjørt.</span><span class="sxs-lookup"><span data-stu-id="ad440-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="ad440-110">Hvis dette alternativet er satt til Ja, kan ikke perioden lukkes før journalføringsprosessen er fullført for denne perioden.</span><span class="sxs-lookup"><span data-stu-id="ad440-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="ad440-111">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ad440-111">Close the page.</span></span>
5. <span data-ttu-id="ad440-112">Gå til **Moduler > Økonomimodul > Periodiske oppgaver > Journalføring** i **Navigasjonsruten**.</span><span class="sxs-lookup"><span data-stu-id="ad440-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="ad440-113">Klikk **Filter**.</span><span class="sxs-lookup"><span data-stu-id="ad440-113">Click **Filter**.</span></span>
7. <span data-ttu-id="ad440-114">Uthev raden med filterkriteriene som du vil definere.</span><span class="sxs-lookup"><span data-stu-id="ad440-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="ad440-115">Angi eller velg filterkriteriene i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ad440-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="ad440-116">Klikk på **OK** for å lukke filtersiden.</span><span class="sxs-lookup"><span data-stu-id="ad440-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="ad440-117">Klikk på **OK** for å starte journalføringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="ad440-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="ad440-118">En rapport blir generert når prosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="ad440-118">A report will be generated after the process is complete.</span></span>  

