---
title: Manglende åpningssaldoer ved årsavslutning
description: Dette emnet beskriver hvorfor åpningssaldoer kan mangle når du avslutter et år, og hvordan du gjenoppbygger disse saldoene hvis de mangler.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028579"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="fae86-103">Manglende åpningssaldoer ved årsavslutning</span><span class="sxs-lookup"><span data-stu-id="fae86-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fae86-104">Dette emnet beskriver hvorfor åpningssaldoer kan mangle når du avslutter et år, og hvordan du gjenoppbygger disse saldoene hvis de mangler.</span><span class="sxs-lookup"><span data-stu-id="fae86-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="fae86-105">Symptom</span><span class="sxs-lookup"><span data-stu-id="fae86-105">Symptom</span></span>

<span data-ttu-id="fae86-106">Hvorfor er det ingen startsaldoer etter at du har kjørt årsavslutning for økonomimodulen?</span><span class="sxs-lookup"><span data-stu-id="fae86-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="fae86-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="fae86-107">Resolution</span></span>

<span data-ttu-id="fae86-108">Her er ting du kan sjekke hvis du har avsluttet et år i økonomimodulen og deretter generert en råbalanse som ikke viser åpningssaldoer, for det neste regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="fae86-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="fae86-109">Hvis feltet **Angre forrige avslutning** er satt til **Ja**, blir den forrige årsavslutningen for det samme regnskapsåret tilbakeført.</span><span class="sxs-lookup"><span data-stu-id="fae86-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="fae86-110">Når du kjører en prosess for å tilbakeføre årsavslutningen, slettes alle oppføringer for både slutt- og åpningssaldoer som om året aldri var blitt avsluttet.</span><span class="sxs-lookup"><span data-stu-id="fae86-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="fae86-111">Bilagene slettes også.</span><span class="sxs-lookup"><span data-stu-id="fae86-111">The vouchers are also deleted.</span></span> <span data-ttu-id="fae86-112">Årsavslutningsprosessen kjøres ikke automatisk på nytt.</span><span class="sxs-lookup"><span data-stu-id="fae86-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="fae86-113">Du må starte prosessen på nytt, og denne gangen må du oppdatere alternativet **Angre forrige avslutning** til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="fae86-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="fae86-114">Dette scenarioet dekkes i emnet om årsavslutning i vanlige spørsmål.</span><span class="sxs-lookup"><span data-stu-id="fae86-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="fae86-115">Hvis du vil ha mer informasjon, kan du se [Vanlige spørsmål om årssluttaktiviteter](faq-year-end-activities.md).</span><span class="sxs-lookup"><span data-stu-id="fae86-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="fae86-116">Symptom</span><span class="sxs-lookup"><span data-stu-id="fae86-116">Symptom</span></span>

<span data-ttu-id="fae86-117">Jeg kjørte årsavslutning med alternativet **Angre forrige avslutning** satt til **Nei**, og jeg har fremdeles ikke åpningssaldoer for regnskapsåret mitt.</span><span class="sxs-lookup"><span data-stu-id="fae86-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="fae86-118">Løsning</span><span class="sxs-lookup"><span data-stu-id="fae86-118">Resolution</span></span>

<span data-ttu-id="fae86-119">Kontroller først statusen til den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="fae86-119">First check the status of the batch job.</span></span> <span data-ttu-id="fae86-120">Avslutning av et år omfatter en rekke separate oppgaver, men det mest kritiske trinnet er den satsvise oppgaven med oppgavebeskrivelsen **Trinn 5.0.0**.</span><span class="sxs-lookup"><span data-stu-id="fae86-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="fae86-121">Postering av åpningstransaksjonene, og eventuelt avslutningstransaksjonene, til økonomimodulen skjer i dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="fae86-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="fae86-122">[![Satsvis logg](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="fae86-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="fae86-123">Hvis dette trinnet ble avsluttet, men du ikke ser åpningssaldoer på siden **Forespørsel om råbalanse** (**Økonomimodul > Forespørsler og rapporter > Råbalanse**), kan du se gjennom resultatene for den satsvise jobben ved årsavslutning for å se om trinnet Gjenoppbygg saldoer er fullført.</span><span class="sxs-lookup"><span data-stu-id="fae86-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="fae86-124">[![Resultater av den satsvise jobben for årsavslutning](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="fae86-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="fae86-125">Hvis dette trinnet av en eller annen grunn har mislykkes, ble åpningstransaksjonene (og eventuelt avslutningstransaksjonene) sannsynligvis postert.</span><span class="sxs-lookup"><span data-stu-id="fae86-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="fae86-126">Du kan kontrollere at økonomimodultransaksjonene ble postert på riktig måte ved hjelp av siden **Forespørsel om bilagstransaksjoner** ved å angi bilagsnummeret og datoen som er angitt i dialogboksen for årsavslutning, for året du lukket (**Økonomimodul > Forespørsler og rapporter > Bilagstransaksjoner**).</span><span class="sxs-lookup"><span data-stu-id="fae86-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="fae86-127">[![Forespørsel om bilagstransaksjoner](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="fae86-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="fae86-128">Hvis åpningsbilagene (og eventuelt avslutningsbilagene) finnes, trenger du ikke å kjøre årsavslutningen på nytt.</span><span class="sxs-lookup"><span data-stu-id="fae86-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="fae86-129">Du kan i stedet se den neste delen for å få informasjon om hvordan du går videre.</span><span class="sxs-lookup"><span data-stu-id="fae86-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="fae86-130">Symptom</span><span class="sxs-lookup"><span data-stu-id="fae86-130">Symptom</span></span>

<span data-ttu-id="fae86-131">Trinnet Gjenoppbygg saldoer i årsavslutningen mislyktes. Må jeg kjøre hele årsavslutningsprosessen på nytt?</span><span class="sxs-lookup"><span data-stu-id="fae86-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="fae86-132">Løsning</span><span class="sxs-lookup"><span data-stu-id="fae86-132">Resolution</span></span>

<span data-ttu-id="fae86-133">Trinnet Gjenoppbygg saldoer oppdaterer økonomimodulsaldoene som brukes når forespørselen om råbalanse genereres.</span><span class="sxs-lookup"><span data-stu-id="fae86-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="fae86-134">Det er det siste trinnet i årsavslutningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="fae86-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="fae86-135">Hvis dette trinnet er det eneste trinnet som mislyktes, er transaksjonene i økonomimodulen postert.</span><span class="sxs-lookup"><span data-stu-id="fae86-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="fae86-136">Du trenger ikke å kjøre årsavslutningen på nytt.</span><span class="sxs-lookup"><span data-stu-id="fae86-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="fae86-137">Du kan kjøre prosessen for å gjenoppbygge saldoene manuelt ved å bruke siden **Finansdimensjonssett** (**Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjonssett**).</span><span class="sxs-lookup"><span data-stu-id="fae86-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="fae86-138">[![Knappen Gjenoppbygg saldoer på siden Finansdimensjonssett](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="fae86-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="fae86-139">Hvis det tar lang tid å behandle dette trinnet, anbefaler vi at du går gjennom anbefalte fremgangsmåter for finansdimensjonssett, som beskrevet i [Anbefalte fremgangsmåter for oppdatering av finansdimensjonssett](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span><span class="sxs-lookup"><span data-stu-id="fae86-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

