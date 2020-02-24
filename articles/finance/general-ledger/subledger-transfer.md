---
title: Overføring av underfinans til økonomimodul
description: Dette emnet beskriver funksjoner i Microsoft Dynamics 365 Finance som er knyttet til overføring av underfinans i økonomimodulen.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1ae10f406148e213fd0272d1387f15606233be27
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000453"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="3666e-103">Overføring av underfinans til økonomimodul</span><span class="sxs-lookup"><span data-stu-id="3666e-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3666e-104">Dette emnet beskriver funksjoner i Microsoft Dynamics 365 Finance som er knyttet til reglene for overføring av bunker med underfinansjournaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="3666e-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="3666e-105">I versjon 8.1 ble det gjort endringer i å tillate overføring av regler, som avskrev det synkrone alternativet.</span><span class="sxs-lookup"><span data-stu-id="3666e-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the Synchronous option.</span></span> <span data-ttu-id="3666e-106">Hvis du vil ha mer informasjon, kan du se [Funksjoner som er fjernet eller avskrevet for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="3666e-106">For more information, see [Removed or deprecated features for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="3666e-107">Følgende alternativer er tilgjengelige for overføring av underfinansbunker.</span><span class="sxs-lookup"><span data-stu-id="3666e-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="3666e-108">Asynkron – Dette alternativet vil umiddelbart planlegge overføring av regnskapspostene fra underfinans til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="3666e-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="3666e-109">Økonomimodulbilaget vil bli registrert så snart ressurser er ledige for å behandle denne forespørselen på serveren.</span><span class="sxs-lookup"><span data-stu-id="3666e-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="3666e-110">Planlagt parti – Dette alternativet legger til regnskapsposter fra underfinans som overføres til behandlingskøen i økonomimodulen, der postene blir behandlet i mottatte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="3666e-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="3666e-111">Økonomimodulbilaget vil bli registrert på det planlagte tidspunktet hvis ressurser er ledige for å behandle denne satsvise jobben på serveren.</span><span class="sxs-lookup"><span data-stu-id="3666e-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="3666e-112">I versjon 10.0.8 ble det gjort forbedringer for å forbedre ytelsen til Asynkron-alternativet.</span><span class="sxs-lookup"><span data-stu-id="3666e-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchrounous option.</span></span> <span data-ttu-id="3666e-113">Denne funksjonen aktiveres under funksjonsnavnet **Ytelsesoptimalisering for overføring av underfinans til økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="3666e-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="3666e-114">Denne funksjonen forbedrer overføring av data fra underfinans til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="3666e-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="3666e-115">Den gjør prosessen mer effektiv, og den grupperer sammen sett med mindre transaksjoner som skal overføres.</span><span class="sxs-lookup"><span data-stu-id="3666e-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="3666e-116">Dette gjør det mulig å bruke partiserveren mer effektivt.</span><span class="sxs-lookup"><span data-stu-id="3666e-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="3666e-117">Denne funksjonen krever at partiserveren er konfigurert, tilkoblet og fungerer for at alternativet for asynkron overføring skal fungere.</span><span class="sxs-lookup"><span data-stu-id="3666e-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchrounous transfer option to work.</span></span> 
