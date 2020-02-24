---
title: Detaljhandelsutdrag
description: Dette emnet beskriver hvordan utdrag opprettes og posteres.
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 4409811d2ef60174a316db10307dc7af4697398c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023575"
---
# <a name="retail-statements"></a><span data-ttu-id="49a1a-103">Detaljhandelsutdrag</span><span class="sxs-lookup"><span data-stu-id="49a1a-103">Retail statements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49a1a-104">I Dynamics 365 Commerce brukes posteringsprosessen for utdraget til å ta hensyn til transaksjoner som forekommer i sky-salgsstedet eller Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="49a1a-104">In Dynamics 365 Commerce, the statement posting process is used to account for the transactions that occur in Cloud point of sale (POS) or Modern POS (MPOS).</span></span> <span data-ttu-id="49a1a-105">Posteringsprosessen for utdrag bruker distribusjonstidsplanen til å hente et sett med salgsstedstransaksjoner til klienten på hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="49a1a-105">The statement posting process uses the distribution schedule to pull a set of POS transactions into the headquarters (HQ) client.</span></span> <span data-ttu-id="49a1a-106">Parameterne som er definert på sidene **Handelsparametere** og **Butikker**, brukes til å velge transaksjonene som hentes til enkeltstående utdrag.</span><span class="sxs-lookup"><span data-stu-id="49a1a-106">The parameters that are defined on the **Commerce parameters** and **Stores** pages are used to select the transactions that are pulled into individual statements.</span></span>

<span data-ttu-id="49a1a-107">Illustrasjonen nedenfor viser utdragposteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="49a1a-107">The following illustration shows the statement posting process.</span></span> <span data-ttu-id="49a1a-108">I denne prosessen vil transaksjoner som registreres i salgsstedet, overføres til klienten ved hjelp av planleggeren i Commerce.</span><span class="sxs-lookup"><span data-stu-id="49a1a-108">In this process, transactions that are recorded in the POS are transmitted to the client by using the Commerce scheduler.</span></span> <span data-ttu-id="49a1a-109">Når klienten mottar transaksjonene, kan du opprette, beregne og bokføre transaksjonskontoutdraget for butikken.</span><span class="sxs-lookup"><span data-stu-id="49a1a-109">After the client receives the transactions, you can create, calculate, and post the transaction statement for the store.</span></span>

<span data-ttu-id="49a1a-110">[![Utdragsposteringsprosess](./media/retail-statements.png)](./media/retail-statements.png)</span><span class="sxs-lookup"><span data-stu-id="49a1a-110">[![Statement posting process](./media/retail-statements.png)](./media/retail-statements.png)</span></span>

## <a name="creating-and-posting-statements"></a><span data-ttu-id="49a1a-111">Opprette og postere utdrag</span><span class="sxs-lookup"><span data-stu-id="49a1a-111">Creating and posting statements</span></span>

<span data-ttu-id="49a1a-112">Du kan opprette et utdrag manuelt eller ved hjelp av satsvise prosesser du konfigurerer for å kjøre regelmessig i løpet av dagen.</span><span class="sxs-lookup"><span data-stu-id="49a1a-112">You can create a statement manually or by using batch processes that you set up to run periodically throughout the day.</span></span> <span data-ttu-id="49a1a-113">I begge tilfeller brukes fremgangsmåten nedenfor til å opprette og postere utdrag.</span><span class="sxs-lookup"><span data-stu-id="49a1a-113">In both cases, the following steps are used to create and post statements.</span></span>

### <a name="create-the-statement"></a><span data-ttu-id="49a1a-114">Opprett utdraget</span><span class="sxs-lookup"><span data-stu-id="49a1a-114">Create the statement</span></span>

<span data-ttu-id="49a1a-115">Dette trinnet identifiserer butikken som utdraget opprettes manuelt for.</span><span class="sxs-lookup"><span data-stu-id="49a1a-115">This step identifies the store that the statement is manually created for.</span></span> <span data-ttu-id="49a1a-116">Hvis du konfigurerer en satsvis prosess, kan du opprette utdrag for alle butikker automatisk, basert på en tidsplan du definerer.</span><span class="sxs-lookup"><span data-stu-id="49a1a-116">If you configure a batch process, you can automatically create statements for all stores, based on a schedule that you define.</span></span>

### <a name="calculate-the-statement"></a><span data-ttu-id="49a1a-117">Beregne utdraget</span><span class="sxs-lookup"><span data-stu-id="49a1a-117">Calculate the statement</span></span>

<span data-ttu-id="49a1a-118">I dette trinnet velges transaksjonslinjene basert på kriterier som er definert for hver butikk på sidene **Handelsparametere** og **Butikker**.</span><span class="sxs-lookup"><span data-stu-id="49a1a-118">In this step, the transaction lines are selected based on criteria that are defined for each store on the **Commerce parameters** and **Stores** pages.</span></span> <span data-ttu-id="49a1a-119">På disse sidene kan du definere kriteriene og angi hvordan transaksjonene skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="49a1a-119">On these pages, you define the criteria and specify how the transactions are calculated.</span></span> <span data-ttu-id="49a1a-120">Hvis du vil vise en liste over transaksjonene som er inkludert i utdraget før du kan beregne utdraget, bruker du siden **Transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="49a1a-120">To view a list of the transactions that are included in the statement before you calculate the statement, use the **Transactions** page.</span></span>

<span data-ttu-id="49a1a-121">Utdragsberegningen bruker kasseoppgjør fra kassene som opptelt beløp.</span><span class="sxs-lookup"><span data-stu-id="49a1a-121">Statement calculation uses tender declarations from the registers as the counted amount.</span></span> <span data-ttu-id="49a1a-122">Du kan eventuelt angi det opptelte beløpet manuelt.</span><span class="sxs-lookup"><span data-stu-id="49a1a-122">Alternatively, you can enter the counted amount manually.</span></span> <span data-ttu-id="49a1a-123">Utdraget viser differansen mellom salgsbeløpet for transaksjonene og det faktiske, opptelte beløpet i alle betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="49a1a-123">The statement shows the difference between the sales amount for the transactions and the actual counted amount in all payment methods.</span></span> <span data-ttu-id="49a1a-124">Utdraget posteres bare hvis denne differansen er mindre enn maksimal posteringsdifferanse som er angitt for butikken.</span><span class="sxs-lookup"><span data-stu-id="49a1a-124">The statement is posted only if this difference is less than the maximum posting difference that is defined for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="49a1a-125">Utdragsberegningsprosessen bruker den globale nummerserien.</span><span class="sxs-lookup"><span data-stu-id="49a1a-125">The statement calculation process uses the global number sequence.</span></span>

<span data-ttu-id="49a1a-126">Når du beregner et utdrag, omfatter beregningen følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="49a1a-126">When you calculate a statement, the calculation includes the following tasks:</span></span>

- <span data-ttu-id="49a1a-127">For det valgte datoområdet kan du merke transaksjoner som ikke ble inkludert i forrige utdragsberegning.</span><span class="sxs-lookup"><span data-stu-id="49a1a-127">For the selected date range, mark transactions that weren't included in a previous statement calculation.</span></span>
- <span data-ttu-id="49a1a-128">Beregn det totale beløpet som ble betalt i de valgte transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="49a1a-128">Calculate the total amounts that were tendered in the selected transactions.</span></span> <span data-ttu-id="49a1a-129">Resultatene vises i utdragslinjene, avhengig av utdragsmetoden:</span><span class="sxs-lookup"><span data-stu-id="49a1a-129">The results are shown on the statement lines, depending on the statement method:</span></span>

    - <span data-ttu-id="49a1a-130">Hvis utdragsmetoden er **Total**, opprettes en linje for hver betalingsmåte i de valgte transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="49a1a-130">If the statement method is **Total**, a line is created for each payment method in the selected transactions.</span></span>
    - <span data-ttu-id="49a1a-131">Hvis utdragsmetoden er **Stab**, opprettes en linje for hver betalingsmåte i transaksjonene som ble foretatt av det valgte stabsmedlemmet.</span><span class="sxs-lookup"><span data-stu-id="49a1a-131">If the statement method is **Staff**, a line is created for each payment method in transactions that were performed by the selected staff member.</span></span>
    - <span data-ttu-id="49a1a-132">Hvis utdragsmetoden er **Salgsstedsterminal**, opprettes en linje for hver betalingsmåte i transaksjoner som ble utført for den valgte kassen.</span><span class="sxs-lookup"><span data-stu-id="49a1a-132">If the statement method is **POS terminal**, a line is created for each payment method in transactions that were performed on the selected register.</span></span>
    - <span data-ttu-id="49a1a-133">Hvis utdragsmetoden er **Skift**, opprettes en linje for hver betalingsmåte i transaksjoner som ble utført under et skift.</span><span class="sxs-lookup"><span data-stu-id="49a1a-133">If the statement method is **Shift**, a line is created for each payment method in transactions that were performed during a shift.</span></span>

<span data-ttu-id="49a1a-134">Hvis det er merket av for **Del etter utdragsmetode** på siden **Lagre**, et separat utdrag opprettes basert på verdien som er valgt i feltet **Utdragsmetode**.</span><span class="sxs-lookup"><span data-stu-id="49a1a-134">If the **Split by Statement method** check box is selected on the **Stores** page, a separate statement is created based on the value that is selected in the **Statement method** field.</span></span>

<span data-ttu-id="49a1a-135">Hvis arbeidstiden i butikken overskrider midnatt, kan du konfigurere postering av utdrag slik at det er basert på endt arbeidsdag i stedet for endt kalenderdag.</span><span class="sxs-lookup"><span data-stu-id="49a1a-135">If your store's operating hours extend past midnight, you can configure statement posting so that it's based on the end of the business day instead of the end of the calendar day.</span></span>

<span data-ttu-id="49a1a-136">På **Lagre**-siden, i hurtigkategorien **Utdrag/avslutning** i feltet **Slutt på arbeidsdag** angir du tidspunktet som den siste transaksjonen må registreres innen, for å bli inkludert i utdraget for denne arbeidsdagen.</span><span class="sxs-lookup"><span data-stu-id="49a1a-136">On the **Stores** page, on the **Statement/closing** FastTab, in the **End of business day** field, enter the time that the last transaction must be recorded to be included in the business day's statement.</span></span> <span data-ttu-id="49a1a-137">Merk av for **Poster som arbeidsdag** for å postere transaksjonene i løpet av samme arbeidsdag.</span><span class="sxs-lookup"><span data-stu-id="49a1a-137">Select the **Post as business day** check box to post the transactions within the same business day.</span></span> <span data-ttu-id="49a1a-138">Når utdraget er postert, kan transaksjoner som er registrert på samme arbeidsdag, inkluderes i den samme salgsordren, selv om enkelte transaksjoner skjer før midnatt og andre transaksjoner skjer etter midnatt.</span><span class="sxs-lookup"><span data-stu-id="49a1a-138">When the statement is posted, transactions that are recorded within the same business day can be included on the same sales order, even if some transactions occur before midnight and other transactions occur after midnight.</span></span>

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a><span data-ttu-id="49a1a-139">Eksempel: Postere et utdrag for en arbeidsdag som strekker seg over to dager i kalenderen</span><span class="sxs-lookup"><span data-stu-id="49a1a-139">Example: Post a statement for a business day that extends over two calendar days</span></span>

<span data-ttu-id="49a1a-140">Et lager er åpent mellom 08:00 og 03:00, og **Poster som arbeidsdag** er merket av i butikkens konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="49a1a-140">A store is open between 8:00 AM and 3:00 AM, and the **Post as business day** check box is selected in the store's configuration.</span></span> <span data-ttu-id="49a1a-141">31. mai registrerer lageret transaksjoner mellom 08:00 og midnatt.</span><span class="sxs-lookup"><span data-stu-id="49a1a-141">On May 31, the store records transactions between 8:00 AM and midnight.</span></span> <span data-ttu-id="49a1a-142">Lageret registrerer også transaksjoner mellom 12:01 og 03:00 1. juni.</span><span class="sxs-lookup"><span data-stu-id="49a1a-142">The store also records transactions between 12:01 AM and 3:00 AM on June 1.</span></span>

<span data-ttu-id="49a1a-143">Når butikken posterer oppgaven for avslutning av arbeidsdagen, vil salgsordren genereres, inkludere alle transaksjoner som ble registrert i arbeidstiden mellom 08:00 og 03:00, selv om transaksjonene fant sted i løpet av to dager, 31. mai og 1. juni.</span><span class="sxs-lookup"><span data-stu-id="49a1a-143">When the store posts its statement for the close of the business day, the sales order that is generated includes all transactions that were recorded between the business hours of 8:00 AM and 3:00 AM, even though the transactions occurred on two days, May 31 and June 1.</span></span>

<span data-ttu-id="49a1a-144">Hvis merket for **Poster som arbeidsdag** fjernes for den samme butikken, genereres separate salgsordrer når butikken posterer oppgaven for avslutning av arbeidsdagen.</span><span class="sxs-lookup"><span data-stu-id="49a1a-144">If the **Post as business day** check box is cleared for the same store, separate sales orders are generated when the store posts its statement for the close of the business day.</span></span> <span data-ttu-id="49a1a-145">Én salgsordre inneholder transaksjoner som ble registrert mellom arbeidstiden 08:00 og midnatt den 31. mai, og den andre salgsordren inneholder transaksjoner som ble registrert mellom virketimene 12:01 og 03:00. den 1. juni.</span><span class="sxs-lookup"><span data-stu-id="49a1a-145">One sales order includes the transactions that were recorded between the business hours of 8:00 AM and midnight on May 31, and the second sales order includes the transactions that were recorded between the business hours of 12:01 AM and 3:00 AM on June 1.</span></span>

> [!NOTE]
> <span data-ttu-id="49a1a-146">Før du kan opprette utdrag, må du lukke skiftene i utdragsperioden.</span><span class="sxs-lookup"><span data-stu-id="49a1a-146">Before you can create statements, you should close the shifts in the statement period.</span></span>

### <a name="post-the-statement"></a><span data-ttu-id="49a1a-147">Postere utdraget</span><span class="sxs-lookup"><span data-stu-id="49a1a-147">Post the statement</span></span>

<span data-ttu-id="49a1a-148">Når du posterer et utdrag, opprettes salgsordrer og fakturaer for salgene i utdraget.</span><span class="sxs-lookup"><span data-stu-id="49a1a-148">When you post a statement, sales orders and invoices are created for the sales in the statement.</span></span>

- <span data-ttu-id="49a1a-149">Hentesalg aggregeres i én salgsordre og faktureres til standardkunden som er tilordnet butikken.</span><span class="sxs-lookup"><span data-stu-id="49a1a-149">Cash and carry sales are aggregated onto one sales order, and are invoiced for the default customer who is assigned to the store.</span></span>
- <span data-ttu-id="49a1a-150">Salg der en kunde ble lagt til for transaksjonen i POS, genererer separate salgsordrer og fakturaer, én for hver unike kunde.</span><span class="sxs-lookup"><span data-stu-id="49a1a-150">Sales for which a customer was added to the transaction in POS generate separate sales orders and invoices, one for each unique customer.</span></span>

<span data-ttu-id="49a1a-151">Betalingsjournaler opprettes automatisk for betalingene i utdraget, og lageret oppdateres for salgsstedsbutikken.</span><span class="sxs-lookup"><span data-stu-id="49a1a-151">Payment journals are automatically created for the payments in the statement, and the inventory is updated for the POS store.</span></span>
