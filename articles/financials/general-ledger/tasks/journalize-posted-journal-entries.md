---
title: Journalføre posterte journaloppføringer
description: Denne fremgangsmåten viser hvordan du journalfører posterte journaloppføringer.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: cbf7ee8063487303cd4c8d2b76a8b44bacc86193
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846397"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="3e7b7-103">Journalføre posterte journaloppføringer</span><span class="sxs-lookup"><span data-stu-id="3e7b7-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3e7b7-104">Denne fremgangsmåten viser hvordan du journalfører posterte journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="3e7b7-105">Denne prosedyren bruker demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="3e7b7-106">Valider innstillingene for journalføring under Økonomimodul > Finansoppsett > Parametere for økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="3e7b7-107">Feltet Utvidet finansjournal kan settes til Ja eller Nei.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="3e7b7-108">Hvis Ja, blir rapportutdataene forskjellige.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="3e7b7-109">Velg om perioden kan lukkes hvis journalføringsprosessen ikke har blitt kjørt.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="3e7b7-110">Hvis dette alternativet er satt til Ja, kan ikke perioden lukkes før journalføringsprosessen er fullført for denne perioden.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="3e7b7-111">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-111">Close the page.</span></span>
5. <span data-ttu-id="3e7b7-112">Gå til Økonomimodul > Periodiske oppgaver > Journalføring.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="3e7b7-113">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-113">Click Filter.</span></span>
7. <span data-ttu-id="3e7b7-114">Uthev raden med filterkriteriene som du vil definere.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="3e7b7-115">Angi eller velg filterkriteriene i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="3e7b7-116">Klikk OK for å lukke filtersiden.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="3e7b7-117">Klikk OK for å starte journalføringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="3e7b7-118">En rapport blir generert når prosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-118">A report will be generated after the process is complete.</span></span>  

