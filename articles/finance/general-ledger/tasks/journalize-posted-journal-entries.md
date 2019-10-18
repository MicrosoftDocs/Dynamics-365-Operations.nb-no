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
ms.openlocfilehash: e20229ca910aa0d7d820434c22edf5a27030bba5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175565"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="54072-103">Journalføre posterte journaloppføringer</span><span class="sxs-lookup"><span data-stu-id="54072-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54072-104">Denne fremgangsmåten viser hvordan du journalfører posterte journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="54072-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="54072-105">Denne prosedyren bruker demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="54072-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="54072-106">I **Navigasjonsrute** går du til **Moduler > Økonomimodul > Finansoppsett > Parametere for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="54072-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="54072-107">Feltet **Utvidet finansjournal** kan settes til Ja eller Nei.</span><span class="sxs-lookup"><span data-stu-id="54072-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="54072-108">Hvis Ja, blir rapportutdataene forskjellige.</span><span class="sxs-lookup"><span data-stu-id="54072-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="54072-109">Velg om perioden kan lukkes hvis journalføringsprosessen ikke har blitt kjørt.</span><span class="sxs-lookup"><span data-stu-id="54072-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="54072-110">Hvis dette alternativet er satt til Ja, kan ikke perioden lukkes før journalføringsprosessen er fullført for denne perioden.</span><span class="sxs-lookup"><span data-stu-id="54072-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="54072-111">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="54072-111">Close the page.</span></span>
5. <span data-ttu-id="54072-112">Gå til **Moduler > Økonomimodul > Periodiske oppgaver > Journalføring** i **Navigasjonsruten**.</span><span class="sxs-lookup"><span data-stu-id="54072-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="54072-113">Klikk **Filter**.</span><span class="sxs-lookup"><span data-stu-id="54072-113">Click **Filter**.</span></span>
7. <span data-ttu-id="54072-114">Uthev raden med filterkriteriene som du vil definere.</span><span class="sxs-lookup"><span data-stu-id="54072-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="54072-115">Angi eller velg filterkriteriene i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="54072-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="54072-116">Klikk på **OK** for å lukke filtersiden.</span><span class="sxs-lookup"><span data-stu-id="54072-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="54072-117">Klikk på **OK** for å starte journalføringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="54072-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="54072-118">En rapport blir generert når prosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="54072-118">A report will be generated after the process is complete.</span></span>  

