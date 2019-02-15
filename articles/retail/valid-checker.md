---
title: Konsekvenskontroll for detaljhandelstransaksjon
description: Dette emnet beskriver funksjonaliteten for konsekvenskontroll for detaljhandelstransaksjon i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "302699"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="5c157-103">Konsekvenskontroll for detaljhandelstransaksjon</span><span class="sxs-lookup"><span data-stu-id="5c157-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="5c157-104">Dette emnet beskriver funksjonaliteten for konsekvenskontroll for detaljhandelstransaksjon som blir introdusert i Microsoft Dynamics 365 for Finance and Operations versjon 8.1.3.</span><span class="sxs-lookup"><span data-stu-id="5c157-104">This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="5c157-105">Konsekvenskontrollen identifiserer og isolerer inkonsekvente transaksjoner før de blir plukket opp av utdragsposteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="5c157-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="5c157-106">Når et utdrag posteres i Retail, kan postering mislykkes på grunn av inkonsekvente data i transaksjonstabellene.</span><span class="sxs-lookup"><span data-stu-id="5c157-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="5c157-107">Dataproblemet kan forårsakes av uforutsette problemer i POS-programmet, eller hvis transaksjoner ikke ble riktig importert fra POS-tredjepartssystemer.</span><span class="sxs-lookup"><span data-stu-id="5c157-107">The data issue may be caused by by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="5c157-108">Eksempler på hvordan disse inkonsekvensene kan vises:</span><span class="sxs-lookup"><span data-stu-id="5c157-108">Examples of how these inconsistencies may appear include:</span></span> 

  - <span data-ttu-id="5c157-109">Transaksjonsbeløpet i toppteksttabellen samsvarer ikke med transaksjonsbeløpet på linjene.</span><span class="sxs-lookup"><span data-stu-id="5c157-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
  - <span data-ttu-id="5c157-110">Linjeantallet i toppteksttabellen samsvarer ikke med antallet linjer i transaksjonstabellen.</span><span class="sxs-lookup"><span data-stu-id="5c157-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
  - <span data-ttu-id="5c157-111">Avgifter i toppteksttabellen samsvarer ikke med mva-beløpet på linjene.</span><span class="sxs-lookup"><span data-stu-id="5c157-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 
  
<span data-ttu-id="5c157-112">Når inkonsekvente transaksjoner blir plukket opp av prosessen, blir inkonsekvente salgsfakturaer og betalingsjournaler opprettet, og derfor mislykkes hele utdragsposteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="5c157-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="5c157-113">Gjenoppretting av utdrag fra en slik tilstand omfatter avanserte datakorrigeringer på tvers av flere transaksjonstabeller.</span><span class="sxs-lookup"><span data-stu-id="5c157-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="5c157-114">Konsekvenskontrollen for detaljhandelstransaksjon hindrer slike problemer.</span><span class="sxs-lookup"><span data-stu-id="5c157-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="5c157-115">Diagrammet nedenfor illustrerer posteringsprosessen med konsekvenskontrollen for transaksjon.</span><span class="sxs-lookup"><span data-stu-id="5c157-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="5c157-116">![Utdragsposteringsprosess med konsekvenskontroll for detaljhandelstransaksjon](./media/validchecker.png "Utdragsposteringsprosess med konsekvenskontroll for detaljhandelstransaksjon")</span><span class="sxs-lookup"><span data-stu-id="5c157-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transsaction consistency checker")</span></span>

<span data-ttu-id="5c157-117">Den satsvise prosessen **Valider butikktransaksjoner** kontrollerer konsekvensen i transaksjonstabellene for detaljhandel for følgende scenarier.</span><span class="sxs-lookup"><span data-stu-id="5c157-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="5c157-118">Kundekonto – validerer at kundekontoen i transaksjonstabellene for detaljhandel finnes i malen Hovedkontorkunde.</span><span class="sxs-lookup"><span data-stu-id="5c157-118">Customer account - Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="5c157-119">Linjeantall – validerer at antallet linjer, som gjengitt i transaksjonstoppteksttabellen, samsvarer med antallet linjer i salgstransaksjonstabellene.</span><span class="sxs-lookup"><span data-stu-id="5c157-119">Line count - Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="5c157-120">Definere konsekvenskontrollen</span><span class="sxs-lookup"><span data-stu-id="5c157-120">Set up the consistency checker</span></span>
<span data-ttu-id="5c157-121">Konfigurer den satsvise prosessen Valider butikktransaksjoner på **Detaljhandel \> Detaljhandel-IT \> POS-postering** for periodiske kjøringer.</span><span class="sxs-lookup"><span data-stu-id="5c157-121">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="5c157-122">Den satsvise jobben kan planlegges basert på butikkens organisasjonshierarki, på samme måte som prosessene Beregne utdrag satsvis og Postere utdrag satsvis blir definert.</span><span class="sxs-lookup"><span data-stu-id="5c157-122">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="5c157-123">Det anbefales at du konfigurerer denne satsvise prosessen til å kjøre flere ganger daglig, og planlegg den slik at den kjøres på slutten av hver kjøring av P-jobb.</span><span class="sxs-lookup"><span data-stu-id="5c157-123">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="5c157-124">Resultater av valideringsprosess</span><span class="sxs-lookup"><span data-stu-id="5c157-124">Results of validation process</span></span>
<span data-ttu-id="5c157-125">Resultatene av valideringskontrollen av den satsvise prosessen er kodet på den aktuelle detaljhandelstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="5c157-125">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="5c157-126">Feltet **Valideringsstatus** i transaksjonsposten for detaljhandel er satt til **Vellykket** eller **Feil**, og datoen for siste valideringskjøring vises i feltet **Tidspunkt for siste validering**.</span><span class="sxs-lookup"><span data-stu-id="5c157-126">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="5c157-127">Hvis du vil vise mer beskrivende feiltekst som er knyttet til en valideringsfeil, velger du den relevante transaksjonsposten for detaljhandel og klikker knappen **Valideringsfeil**.</span><span class="sxs-lookup"><span data-stu-id="5c157-127">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="5c157-128">Transaksjoner som ikke består valideringskontrollen, og transaksjoner som ennå ikke er validert, vil ikke trekkes inn i utdrag.</span><span class="sxs-lookup"><span data-stu-id="5c157-128">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="5c157-129">I løpet av prosessen Beregn utdrag vil brukere bli varslet hvis det finnes transaksjoner som kunne ha vært inkludert i utdraget, men som ikke ble inkludert.</span><span class="sxs-lookup"><span data-stu-id="5c157-129">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="5c157-130">Hvis det finnes en valideringsfeil, er den eneste måten å rette opp feilen på, å kontakte Microsofts kundestøtte.</span><span class="sxs-lookup"><span data-stu-id="5c157-130">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="5c157-131">Denne funksjonen vil bli lagt til i en fremtidig versjon slik at brukere kan fikse postene som mislyktes i brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="5c157-131">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="5c157-132">Loggings- og overvåkingsfunksjoner vil også bli gjort tilgjengelige for sporing av historikken for endringene.</span><span class="sxs-lookup"><span data-stu-id="5c157-132">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="5c157-133">Flere valideringsregler for å støtte flere scenarier vil bli lagt til i en fremtidig versjon.</span><span class="sxs-lookup"><span data-stu-id="5c157-133">Additional validation rules to support more scenarios will be added in a future release.</span></span>
