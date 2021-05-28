---
title: Avgift posteres til feil finanskonto i bilaget
description: Dette emnet gir feilsøkingsinformasjon som kan hjelpe når skatt posteres til feil finanskonto i bilaget.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020097"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a><span data-ttu-id="df57a-103">Avgift posteres til feil finanskonto i bilaget</span><span class="sxs-lookup"><span data-stu-id="df57a-103">Tax is posted to the wrong ledger account in the voucher</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df57a-104">Under postering kan avgift posteres til feil finanskonto i bilaget.</span><span class="sxs-lookup"><span data-stu-id="df57a-104">During posting, tax might be posted to the wrong ledger account in the voucher.</span></span> <span data-ttu-id="df57a-105">Hvis du vil feilsøke dette problemet, følger du trinnene i de følgende delene etter behov.</span><span class="sxs-lookup"><span data-stu-id="df57a-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span> <span data-ttu-id="df57a-106">Eksemplene i dette emnet bruker en salgsordre som forretningsdokument.</span><span class="sxs-lookup"><span data-stu-id="df57a-106">The examples in this topic use a sales order as the business document.</span></span>

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a><span data-ttu-id="df57a-107">Finn mva-koden til den feil posterte mva-transaksjonen</span><span class="sxs-lookup"><span data-stu-id="df57a-107">Find the tax code of the incorrectly posted tax transaction</span></span>

1. <span data-ttu-id="df57a-108">Velg transaksjonen du vil arbeide med, på **Bilagstransaksjoner**-siden, og velg deretter **Postert merverdiavgift**.</span><span class="sxs-lookup"><span data-stu-id="df57a-108">On the **Voucher transactions** page, select the transaction that you want to work with, and then select **Posted sales tax**.</span></span>

    <span data-ttu-id="df57a-109">[![Postert merverdiavgift-knappen på bilagstransaksjonssiden](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="df57a-109">[![Posted sales tax button on the Voucher transactions page](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span></span>

2. <span data-ttu-id="df57a-110">Se gjennom verdien i **Mva-kode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="df57a-110">Review the value in the **Sales tax code** field.</span></span> <span data-ttu-id="df57a-111">I dette eksemplet er den **Mva 19**.</span><span class="sxs-lookup"><span data-stu-id="df57a-111">In this example, it's **VAT 19**.</span></span>

    <span data-ttu-id="df57a-112">[![Mva-kode-feltet på siden Postert merverdiavgift](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="df57a-112">[![Sales tax code field on the Posted sales tax page](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span></span>

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a><span data-ttu-id="df57a-113">Kontroller finansposteringsgruppen for mva-koden</span><span class="sxs-lookup"><span data-stu-id="df57a-113">Check the ledger posting group of the tax code</span></span>

1. <span data-ttu-id="df57a-114">Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-koder**.</span><span class="sxs-lookup"><span data-stu-id="df57a-114">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="df57a-115">Søk etter og velg avgiftskoden, og gå deretter gjennom verdien i feltet **Finansposteringsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="df57a-115">Find and select the tax code, and then review the value in the **Ledger posting group** field.</span></span> <span data-ttu-id="df57a-116">I dette eksemplet er den **Mva**.</span><span class="sxs-lookup"><span data-stu-id="df57a-116">In this example, it's **VAT**.</span></span>

    <span data-ttu-id="df57a-117">[![Feltet Finansposteringsgruppe på siden Mva-koder](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="df57a-117">[![Ledger posting group field on the Sales tax codes page](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span></span>

3. <span data-ttu-id="df57a-118">Verdien i feltet **Finansposteringsgruppe** er en kobling.</span><span class="sxs-lookup"><span data-stu-id="df57a-118">The value in the **Ledger posting group** field is a link.</span></span> <span data-ttu-id="df57a-119">Hvis du vil vise detaljer om gruppens konfigurasjon, velger du koblingen.</span><span class="sxs-lookup"><span data-stu-id="df57a-119">To view the details of the group's configuration, select the link.</span></span> <span data-ttu-id="df57a-120">Du kan også velge og holde (eller høyreklikke) i feltet og velge **Vis detaljer**.</span><span class="sxs-lookup"><span data-stu-id="df57a-120">Alternatively, select and hold (or right-click) in the field, and then select **View details**.</span></span>

    <span data-ttu-id="df57a-121">[![Vis detaljer-kommando](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="df57a-121">[![View details command](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span></span>

4. <span data-ttu-id="df57a-122">I feltet **Utgående merverdiavgif** må du kontrollere at kontonummeret er riktig i henhold til transaksjonstypen.</span><span class="sxs-lookup"><span data-stu-id="df57a-122">In the **Sales tax payable** field, verify that the account number is correct, according to the transaction type.</span></span> <span data-ttu-id="df57a-123">Hvis ikke velger du riktig konto.</span><span class="sxs-lookup"><span data-stu-id="df57a-123">If it isn't, select the correct account to post to.</span></span> <span data-ttu-id="df57a-124">I dette eksemplet skal merverdiavgiften for salgsordren posteres til betalingskonto for merverdiavgift 222200.</span><span class="sxs-lookup"><span data-stu-id="df57a-124">In this example, the sales tax of the sales order should be posted to sales tax payable account 222200.</span></span>

    <span data-ttu-id="df57a-125">[![Feltet Konto, utgående mva på siden Finansposteringsgrupper](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png).</span><span class="sxs-lookup"><span data-stu-id="df57a-125">[![Sales tax payable field on the Ledger posting groups page](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span></span>

    <span data-ttu-id="df57a-126">Følgende tabell inneholder informasjon om hvert felt på siden **Finansposteringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="df57a-126">The following table provides information about each field on the **Ledger posting groups** page.</span></span>

    | <span data-ttu-id="df57a-127">Felt</span><span class="sxs-lookup"><span data-stu-id="df57a-127">Field</span></span>                  | <span data-ttu-id="df57a-128">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="df57a-128">Description</span></span> |
    |------------------------|-------------|
    | <span data-ttu-id="df57a-129">Konto, utgående mva</span><span class="sxs-lookup"><span data-stu-id="df57a-129">Sales tax payable</span></span>      | <span data-ttu-id="df57a-130">Hovedkontoen for utgående merverdiavgift som skal betales til skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="df57a-130">The main account for outgoing sales taxes that are payable to the tax authority.</span></span> |
    | <span data-ttu-id="df57a-131">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="df57a-131">Sales tax receivable</span></span>   | <span data-ttu-id="df57a-132">Hovedkontoen for inngående mva som mottas fra skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="df57a-132">The main account for incoming taxes that are received from the tax authority.</span></span> |
    | <span data-ttu-id="df57a-133">Use tax-utgift</span><span class="sxs-lookup"><span data-stu-id="df57a-133">Use tax expense</span></span>        | <span data-ttu-id="df57a-134">Hovedkontoen som brukes til å postere fradragsberettiget use tax som leverandører ikke krever eller rapporterer til skattemyndighetene som en del av GST/HST (Goods and Services Tax / Avstemt mva) for Den europeiske union.</span><span class="sxs-lookup"><span data-stu-id="df57a-134">The main account that is used to post deductible use taxes that vendors don't claim or report to the tax authority as part of European Union (EU) reverse charge Goods and Services Tax (GST)/Harmonized Sales Tax (HST).</span></span> <span data-ttu-id="df57a-135">Alternativet **Use tax** må velges for mva-koden i mva-gruppen som skal brukes i transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="df57a-135">**Use tax** must be selected for the sales tax code in the sales tax group that is used in the transaction.</span></span> <span data-ttu-id="df57a-136">Dette feltet er ikke tilgjengelig hvis **Bruk avgiftsregler for merverdiavgift** er valgt på siden **Økonomiparametere**.</span><span class="sxs-lookup"><span data-stu-id="df57a-136">This field isn't available if **Apply sales tax taxation rules** is selected on the **General ledger parameters** page.</span></span> |
    | <span data-ttu-id="df57a-137">Forfalt use tax</span><span class="sxs-lookup"><span data-stu-id="df57a-137">Use tax payable</span></span>        | <span data-ttu-id="df57a-138">Hovedkontoen som brukes til å postere innkommende use tax som betales til skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="df57a-138">The main account that is used to post incoming use taxes that are payable to tax authorities.</span></span> |
    | <span data-ttu-id="df57a-139">Utligningskonto</span><span class="sxs-lookup"><span data-stu-id="df57a-139">Settlement account</span></span>     | <span data-ttu-id="df57a-140">Hovedkontoen som brukes til å postere nettosaldoen for finanskontoene som er angitt i feltene **Forfalt use tax** og **Inngående merverdiavgift**.</span><span class="sxs-lookup"><span data-stu-id="df57a-140">The main account that is used to post the net balance of the ledger accounts that are specified in the **Use tax payable** and **Sales tax receivable** fields.</span></span> |
    | <span data-ttu-id="df57a-141">Leverandørkontantrabatt</span><span class="sxs-lookup"><span data-stu-id="df57a-141">Vendor cash discount</span></span>   | <span data-ttu-id="df57a-142">Hovedkontoen som brukes til å postere en kontorabatt for mva-koder knyttet til denne finansposteringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="df57a-142">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |
    | <span data-ttu-id="df57a-143">Kundekontantrabatt</span><span class="sxs-lookup"><span data-stu-id="df57a-143">Customer case discount</span></span> | <span data-ttu-id="df57a-144">Hovedkontoen som brukes til å postere en kontorabatt for mva-koder knyttet til denne finansposteringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="df57a-144">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |

    <span data-ttu-id="df57a-145">Hvis du vil ha mer informasjon, kan du se [Definere finansposteringsgrupper for merverdiavgift](tasks/set-up-ledger-posting-groups-sales-tax.md).</span><span class="sxs-lookup"><span data-stu-id="df57a-145">For more information, see, [Set up Ledger posting groups for sales tax](tasks/set-up-ledger-posting-groups-sales-tax.md)</span></span>

## <a name="debug-in-code-to-check-ledger-dimensions"></a><span data-ttu-id="df57a-146">Feilsøke i kode for å kontrollere finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="df57a-146">Debug in code to check ledger dimensions</span></span>

<span data-ttu-id="df57a-147">I koden bestemmes posteringskontoen av finansdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="df57a-147">In the code, the posting account is determined by the ledger dimension.</span></span> <span data-ttu-id="df57a-148">Finansdimensjonen lagrer post-IDen til en konto i databasen.</span><span class="sxs-lookup"><span data-stu-id="df57a-148">The ledger dimension saves the record ID of an account in the database.</span></span>

1. <span data-ttu-id="df57a-149">Legg til et stoppunkt ved metodene **Tax::saveAndPost()** og **Tax::post()** for en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="df57a-149">For a sales order, add a breakpoint at the **Tax::saveAndPost()** and **Tax::post()** methods.</span></span> <span data-ttu-id="df57a-150">Vær oppmerksom på verdien til **\_LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="df57a-150">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="df57a-151">[![Eksempel på salgsordrekode som har et stoppunkt](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="df57a-151">[![Sales order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span></span>

    <span data-ttu-id="df57a-152">Legg til et stoppunkt ved metodene **TaxPost::saveAndPost()** og **TaxPost::postToTaxTrans()** for en bestilling.</span><span class="sxs-lookup"><span data-stu-id="df57a-152">For a purchase order, add a breakpoint at the **TaxPost::saveAndPost()** and **TaxPost::postToTaxTrans()** methods.</span></span> <span data-ttu-id="df57a-153">Vær oppmerksom på verdien til **\_LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="df57a-153">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="df57a-154">[![Eksempel på bestillingskode som har et stoppunkt](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span><span class="sxs-lookup"><span data-stu-id="df57a-154">[![Purchase order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span></span>

2. <span data-ttu-id="df57a-155">Kjør følgende SQL-spørring for å finne visningsverdien til kontoen i databasen, basert på post-IDen som er lagret av finansdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="df57a-155">Run the following SQL query to find the display value of the account in the database, based on the record ID that is saved by the ledger dimension.</span></span>

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    <span data-ttu-id="df57a-156">[![Visningsverdi for post-IDen](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span><span class="sxs-lookup"><span data-stu-id="df57a-156">[![Display value of the record ID](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span></span>

3. <span data-ttu-id="df57a-157">Undersøk kallstakken for å finne ut hvor **_ledgerDimension**-verdien er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="df57a-157">Examine the callstack to find where the **_ledgerDimension** value is assigned.</span></span> <span data-ttu-id="df57a-158">Vanligvis kommer verdien fra **TmpTaxWorkTrans**.</span><span class="sxs-lookup"><span data-stu-id="df57a-158">Usually, the value is from **TmpTaxWorkTrans**.</span></span> <span data-ttu-id="df57a-159">I dette tilfellet bør du legge til et stoppunkt ved **TmpTaxWorkTrans::insert()** og **TmpTaxWorkTrans::update()** for å finne hvor verdien er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="df57a-159">In this case, you should add a breakpoint at **TmpTaxWorkTrans::insert()** and **TmpTaxWorkTrans::update()** to find where the value assigned.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="df57a-160">Fastslå om det finnes tilpasning</span><span class="sxs-lookup"><span data-stu-id="df57a-160">Determine whether customization exists</span></span>

<span data-ttu-id="df57a-161">Hvis du har fullført trinnene i de forrige delene, men ikke har funnet problemet, må du avgjøre om det finnes tilpasning.</span><span class="sxs-lookup"><span data-stu-id="df57a-161">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="df57a-162">Hvis det ikke finnes noen tilpasning, oppretter du en Microsoft-tjenesteforespørsel for mer støtte.</span><span class="sxs-lookup"><span data-stu-id="df57a-162">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
