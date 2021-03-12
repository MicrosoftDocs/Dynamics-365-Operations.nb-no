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
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: de9328f69938151c5558d41263d36b873d117e4b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975489"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="9846b-103">Overføring av underfinans til økonomimodul</span><span class="sxs-lookup"><span data-stu-id="9846b-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9846b-104">Dette emnet beskriver funksjoner i Microsoft Dynamics 365 Finance som er knyttet til reglene for overføring av bunker med underfinansjournaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="9846b-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="9846b-105">I versjon 8.1 ble det gjort endringer for å tillate overføring av regler, som avskrev **Synkron**-alternativet.</span><span class="sxs-lookup"><span data-stu-id="9846b-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="9846b-106">Hvis du vil ha mer informasjon, kan du se [Funksjoner som er fjernet eller avskrevet for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="9846b-106">For more information, see [Removed or deprecated features for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="9846b-107">Følgende alternativer er tilgjengelige for overføring av underfinansbunker.</span><span class="sxs-lookup"><span data-stu-id="9846b-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="9846b-108">Asynkron – Dette alternativet vil umiddelbart planlegge overføring av regnskapspostene fra underfinans til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="9846b-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="9846b-109">Økonomimodulbilaget vil bli registrert så snart ressurser er ledige for å behandle denne forespørselen på serveren.</span><span class="sxs-lookup"><span data-stu-id="9846b-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="9846b-110">Planlagt parti – Dette alternativet legger til regnskapsposter fra underfinans som overføres til behandlingskøen i økonomimodulen, der postene blir behandlet i mottatte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="9846b-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="9846b-111">Økonomimodulbilaget vil bli registrert på det planlagte tidspunktet hvis ressurser er ledige for å behandle denne satsvise jobben på serveren.</span><span class="sxs-lookup"><span data-stu-id="9846b-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="9846b-112">I versjon 10.0.8 ble det gjort forbedringer for å forbedre ytelsen til Asynkron-alternativet.</span><span class="sxs-lookup"><span data-stu-id="9846b-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="9846b-113">Denne funksjonen aktiveres under funksjonsnavnet **Ytelsesoptimalisering for overføring av underfinans til økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="9846b-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="9846b-114">Denne funksjonen forbedrer overføring av data fra underfinans til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="9846b-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="9846b-115">Den gjør prosessen mer effektiv, og den grupperer sammen sett med mindre transaksjoner som skal overføres.</span><span class="sxs-lookup"><span data-stu-id="9846b-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="9846b-116">Dette gjør det mulig å bruke partiserveren mer effektivt.</span><span class="sxs-lookup"><span data-stu-id="9846b-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="9846b-117">Denne funksjonen krever at partiserveren er konfigurert, tilkoblet og fungerer for at alternativet for asynkron overføring skal fungere.</span><span class="sxs-lookup"><span data-stu-id="9846b-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 
