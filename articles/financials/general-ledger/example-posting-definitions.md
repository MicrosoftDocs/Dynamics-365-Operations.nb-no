---
title: Posteringsdefinisjoner
description: Denne artikkelen inneholder eksempler som viser hvordan posteringsdefinisjoner brukes for bestillingsdisposisjoner og budsjettbevilgninger.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1bbd9230219f11407bc7afbd59670c6287b77c02
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="posting-definition-examples"></a><span data-ttu-id="ce921-103">Eksempler på posteringsdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="ce921-103">Posting definition examples</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ce921-104">Denne artikkelen inneholder eksempler som viser hvordan posteringsdefinisjoner brukes for bestillingsdisposisjoner og budsjettbevilgninger.</span><span class="sxs-lookup"><span data-stu-id="ce921-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="ce921-105">Før du leser dette emnet, bør du være kjent med posteringsdefinisjoner og posteringsdefinisjoner for transaksjon.</span><span class="sxs-lookup"><span data-stu-id="ce921-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="ce921-106">Hvis du vil ha informasjon, se [Posteringsdefinisjoner](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="ce921-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="ce921-107">Eksemplene nedenfor kan settes opp på siden **Posteringsdefinisjoner**.</span><span class="sxs-lookup"><span data-stu-id="ce921-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="ce921-108">Hvert eksempel inneholder disse delene:</span><span class="sxs-lookup"><span data-stu-id="ce921-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="ce921-109">Posteringsdefinisjon – samsvarskriterier</span><span class="sxs-lookup"><span data-stu-id="ce921-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="ce921-110">Posteringsdefinisjon – genererte oppføringer</span><span class="sxs-lookup"><span data-stu-id="ce921-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="ce921-111">Transaksjoner med kontoer, dimensjonsverdiene og beløp</span><span class="sxs-lookup"><span data-stu-id="ce921-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="ce921-112">Finansoppføringer som er generert fra posteringsdefinisjonen</span><span class="sxs-lookup"><span data-stu-id="ce921-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="ce921-113">Når et samsvar oppstår mellom kontoer og dimensjonsverdier i **Samsvarskriterier**-ruten for posteringsdefinisjonen og kontoene og dimensjonsverdiene for transaksjonen, genereres finansoppføringer basert på **Genererte oppføringer**-ruten for posteringsdefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="ce921-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="ce921-114">Bruk siden **Definisjoner for transaksjonspostering** for å knytte en posteringsdefinisjon til en bestemt transaksjonstype.</span><span class="sxs-lookup"><span data-stu-id="ce921-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="ce921-115">Når du har knyttet en posteringsdefinisjon til en transaksjonstype og valgt**Bruk posteringsdefinisjoner** på siden **Parametere for økonomimodul**, må alle transaksjoner med den valgte transaksjonstypen bruke posteringsdefinisjoner.</span><span class="sxs-lookup"><span data-stu-id="ce921-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="ce921-116">Eksempel: bestillingsdisposisjoner</span><span class="sxs-lookup"><span data-stu-id="ce921-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="ce921-117">Når du aktiverer disposisjonsbehandling ved å velge **Aktiver disposisjonsprosess** på **Økonomiparametere**, må posteringsdefinisjoner brukes til å registrere disposisjoner i økonomimodulen for alle kontoer som skal reserveres.</span><span class="sxs-lookup"><span data-stu-id="ce921-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="ce921-118">I de fleste tilfeller reserveres alle utgiftskontoer i balansen.</span><span class="sxs-lookup"><span data-stu-id="ce921-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="ce921-119">Posteringsdefinisjoner for disposisjoner defineres for **Innkjøp**-modulen på **Posteringsdefinisjoner**-siden.</span><span class="sxs-lookup"><span data-stu-id="ce921-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="ce921-120">Deretter, i **Innkjøp**-området på siden **Definisjoner for transaksjonspostering**, kan du velge **Bestilling**-transaksjonstypen for å knytte posteringsdefinisjonen til bestillinger.</span><span class="sxs-lookup"><span data-stu-id="ce921-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="ce921-121">Alle bilagstransaksjoner for bestillingsdisposisjoner må være i balanse (det vil si debet må være lik kredit) i hver unike dimensjon på et bilag.</span><span class="sxs-lookup"><span data-stu-id="ce921-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="ce921-122">Posteringsdefinisjon – samsvarskriterier</span><span class="sxs-lookup"><span data-stu-id="ce921-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="ce921-123">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="ce921-123">Account structure</span></span>       | <span data-ttu-id="ce921-124">Kontonummer for samsvar</span><span class="sxs-lookup"><span data-stu-id="ce921-124">Match account number</span></span> | <span data-ttu-id="ce921-125">Prioritet</span><span class="sxs-lookup"><span data-stu-id="ce921-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="ce921-126">Kontostruktur – resultat</span><span class="sxs-lookup"><span data-stu-id="ce921-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="ce921-127">1</span><span class="sxs-lookup"><span data-stu-id="ce921-127">1</span></span>        |

<span data-ttu-id="ce921-128">*En tom verdi i feltet **Samsvarskontonummer** betyr at alle samsvarende kontoer i den definerte kontostrukturen er en del av den samsvarende regelen.</span><span class="sxs-lookup"><span data-stu-id="ce921-128">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="ce921-129">Posteringsdefinisjon – genererte oppføringer</span><span class="sxs-lookup"><span data-stu-id="ce921-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="ce921-130">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="ce921-130">Account structure</span></span> | <span data-ttu-id="ce921-131">Generert kontonummer</span><span class="sxs-lookup"><span data-stu-id="ce921-131">Generated account number</span></span>                    | <span data-ttu-id="ce921-132">Generert debet/kreditt</span><span class="sxs-lookup"><span data-stu-id="ce921-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="ce921-133">Saldo</span><span class="sxs-lookup"><span data-stu-id="ce921-133">Balance</span></span>           | <span data-ttu-id="ce921-134">300143 - - (disposisjonskonto)</span><span class="sxs-lookup"><span data-stu-id="ce921-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="ce921-135">Lik</span><span class="sxs-lookup"><span data-stu-id="ce921-135">Same</span></span>                   |
| <span data-ttu-id="ce921-136">Saldo</span><span class="sxs-lookup"><span data-stu-id="ce921-136">Balance</span></span>           | <span data-ttu-id="ce921-137">300144 -- (Reserver for disposisjonskonto)</span><span class="sxs-lookup"><span data-stu-id="ce921-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="ce921-138">Balanse</span><span class="sxs-lookup"><span data-stu-id="ce921-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="ce921-139">Transaksjoner med kontoer, dimensjonsverdiene og beløp</span><span class="sxs-lookup"><span data-stu-id="ce921-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="ce921-140">Kontoene og dimensjonsverdiene kommer fra regnskapsdistribusjonene du angir for en bestillingslinje, eller fra kontoer og dimensjoner som genereres automatisk basert på standardinnstillingene for leverandører, varer, kategorier og maler for dimensjonen.</span><span class="sxs-lookup"><span data-stu-id="ce921-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="ce921-141">Konto + dimensjoner</span><span class="sxs-lookup"><span data-stu-id="ce921-141">Account + dimensions</span></span>           | <span data-ttu-id="ce921-142">Debet</span><span class="sxs-lookup"><span data-stu-id="ce921-142">Debit</span></span>  | <span data-ttu-id="ce921-143">Kreditt</span><span class="sxs-lookup"><span data-stu-id="ce921-143">Credit</span></span> | <span data-ttu-id="ce921-144">Kommentar</span><span class="sxs-lookup"><span data-stu-id="ce921-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="ce921-145">606400-OU\_1-OU\_3566-opplæring</span><span class="sxs-lookup"><span data-stu-id="ce921-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="ce921-146">250,00</span><span class="sxs-lookup"><span data-stu-id="ce921-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="ce921-147">Finansoppføringer som er generert fra posteringsdefinisjonen</span><span class="sxs-lookup"><span data-stu-id="ce921-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="ce921-148">Genererte finansoppføringer opprettes for å registrere disposisjonene.</span><span class="sxs-lookup"><span data-stu-id="ce921-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="ce921-149">Konto + dimensjoner</span><span class="sxs-lookup"><span data-stu-id="ce921-149">Account + dimensions</span></span>           | <span data-ttu-id="ce921-150">Debet</span><span class="sxs-lookup"><span data-stu-id="ce921-150">Debit</span></span>  | <span data-ttu-id="ce921-151">Kreditt</span><span class="sxs-lookup"><span data-stu-id="ce921-151">Credit</span></span> | <span data-ttu-id="ce921-152">Kommentar</span><span class="sxs-lookup"><span data-stu-id="ce921-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="ce921-153">300143-OU\_1-OU\_3566-opplæring</span><span class="sxs-lookup"><span data-stu-id="ce921-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="ce921-154">250,00</span><span class="sxs-lookup"><span data-stu-id="ce921-154">250.00</span></span> |        |         |
| <span data-ttu-id="ce921-155">300144-OU\_1-OU\_3566-opplæring</span><span class="sxs-lookup"><span data-stu-id="ce921-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="ce921-156">250,00</span><span class="sxs-lookup"><span data-stu-id="ce921-156">250.00</span></span> |         |

<span data-ttu-id="ce921-157">I dette eksemplet samsvarer alle kontoer som inngår i Kontostruktur – resultat, kriteriene for posteringsdefinisjon.</span><span class="sxs-lookup"><span data-stu-id="ce921-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="ce921-158">Når 606500-OU\_1-OU\_3566-opplæring blir evaluert, opprettes derfor genererte oppføringer for kontoene som er definert i **Genererte oppføringer**-ruten for posteringsdefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="ce921-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="ce921-159">Eksempel: budsjettbevilgninger</span><span class="sxs-lookup"><span data-stu-id="ce921-159">Example: Budget appropriations</span></span>
<span data-ttu-id="ce921-160">Når du aktiverer budsjettbevilgning ved å velge **Aktiver budsjettbevilgning** på **Økonomiparametere**-siden, må posteringsdefinisjoner brukes til å registrere budsjettregisteroppføringer i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="ce921-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="ce921-161">Når en budsjettkontrollkonfigurasjon er aktivert og er slått på, kan posteringsdefinisjoner og posteringsdefinisjoner for transaksjon brukes til å støtte registreringen av oppføringer for avsetninger, endringer, overføringer, prosjekter, anleggsmidler og forsynings- og behovsprognoser til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="ce921-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="ce921-162">Hvis du vil definere en posteringsdefinisjon for budsjettregistreroppføringer som har budsjettypen **Opprinnelig budsjett** og som har avsetninger aktivert, velger du **Budsjett**-modulen på **Posteringsdefinisjoner**-siden.</span><span class="sxs-lookup"><span data-stu-id="ce921-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="ce921-163">Deretter, i **Budsjett**-området på siden **Definisjoner for transaksjonspostering**, kan du kan bruke budsjettkoder for å knytte posteringsdefinisjonen til budsjettregisteroppføringer med budsjettypen **Opprinnelig budsjett**.</span><span class="sxs-lookup"><span data-stu-id="ce921-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="ce921-164">Når budsjettbevilgninger og posteringsdefinisjoner er aktivert, registreres budsjettregisteroppføringene for budsjettkontroll, og i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="ce921-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="ce921-165">Posteringsdefinisjon – samsvarskriterier</span><span class="sxs-lookup"><span data-stu-id="ce921-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="ce921-166">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="ce921-166">Account structure</span></span>       | <span data-ttu-id="ce921-167">Kontonummer for samsvar</span><span class="sxs-lookup"><span data-stu-id="ce921-167">Match account number</span></span> | <span data-ttu-id="ce921-168">Prioritet</span><span class="sxs-lookup"><span data-stu-id="ce921-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="ce921-169">Kontostruktur – resultat</span><span class="sxs-lookup"><span data-stu-id="ce921-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="ce921-170">1</span><span class="sxs-lookup"><span data-stu-id="ce921-170">1</span></span>        |

<span data-ttu-id="ce921-171">*En tom verdi i feltet **Samsvarskontonummer** betyr at alle samsvarende kontoer i den definerte kontostrukturen er en del av den samsvarende regelen.</span><span class="sxs-lookup"><span data-stu-id="ce921-171">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="ce921-172">Posteringsdefinisjon – genererte oppføringer</span><span class="sxs-lookup"><span data-stu-id="ce921-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="ce921-173">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="ce921-173">Account structure</span></span> | <span data-ttu-id="ce921-174">Generert kontonummer</span><span class="sxs-lookup"><span data-stu-id="ce921-174">Generated account number</span></span>              | <span data-ttu-id="ce921-175">Generert debet/kreditt</span><span class="sxs-lookup"><span data-stu-id="ce921-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="ce921-176">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="ce921-176">Account structure</span></span> | <span data-ttu-id="ce921-177">300145 - - (konto for estimert omsetning)</span><span class="sxs-lookup"><span data-stu-id="ce921-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="ce921-178">Lik</span><span class="sxs-lookup"><span data-stu-id="ce921-178">Same</span></span>                   |
| <span data-ttu-id="ce921-179">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="ce921-179">Account structure</span></span> | <span data-ttu-id="ce921-180">300146 -- (bevilgningskonto)</span><span class="sxs-lookup"><span data-stu-id="ce921-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="ce921-181">Balanse</span><span class="sxs-lookup"><span data-stu-id="ce921-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="ce921-182">Transaksjoner med kontoer, dimensjonsverdiene og beløp</span><span class="sxs-lookup"><span data-stu-id="ce921-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="ce921-183">Du angir kontoene, dimensjonsverdiene og beløpene for budsjettkontooppføringen på siden **Budsjettregisteroppføring**.</span><span class="sxs-lookup"><span data-stu-id="ce921-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="ce921-184">Konto + dimensjoner</span><span class="sxs-lookup"><span data-stu-id="ce921-184">Account + dimensions</span></span>           | <span data-ttu-id="ce921-185">Debet</span><span class="sxs-lookup"><span data-stu-id="ce921-185">Debit</span></span> | <span data-ttu-id="ce921-186">Kreditt</span><span class="sxs-lookup"><span data-stu-id="ce921-186">Credit</span></span> | <span data-ttu-id="ce921-187">Kommentar</span><span class="sxs-lookup"><span data-stu-id="ce921-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="ce921-188">606400-OU\_1-OU\_3566-opplæring</span><span class="sxs-lookup"><span data-stu-id="ce921-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="ce921-189">250,00</span><span class="sxs-lookup"><span data-stu-id="ce921-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="ce921-190">Finansoppføringer som er generert fra posteringsdefinisjonen</span><span class="sxs-lookup"><span data-stu-id="ce921-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="ce921-191">Genererte finansposter opprettes for å registrere det opprinnelige budsjettet i hver dimensjon.</span><span class="sxs-lookup"><span data-stu-id="ce921-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="ce921-192">Konto + dimensjoner</span><span class="sxs-lookup"><span data-stu-id="ce921-192">Account + dimensions</span></span>           | <span data-ttu-id="ce921-193">Debet</span><span class="sxs-lookup"><span data-stu-id="ce921-193">Debit</span></span>  | <span data-ttu-id="ce921-194">Kreditt</span><span class="sxs-lookup"><span data-stu-id="ce921-194">Credit</span></span> | <span data-ttu-id="ce921-195">Kommentar</span><span class="sxs-lookup"><span data-stu-id="ce921-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="ce921-196">300145-OU\_1-OU\_3566-opplæring</span><span class="sxs-lookup"><span data-stu-id="ce921-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="ce921-197">250,00</span><span class="sxs-lookup"><span data-stu-id="ce921-197">250.00</span></span> |         |
| <span data-ttu-id="ce921-198">300146-OU\_1-OU\_3566-opplæring</span><span class="sxs-lookup"><span data-stu-id="ce921-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="ce921-199">250,00</span><span class="sxs-lookup"><span data-stu-id="ce921-199">250.00</span></span> |        |         |

<span data-ttu-id="ce921-200">I dette eksemplet samsvarer alle kontoer som inngår i Kontostruktur – resultat, kriteriene for posteringsdefinisjon.</span><span class="sxs-lookup"><span data-stu-id="ce921-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="ce921-201">Når 606400-OU\_1-OU\_3566-opplæring blir evaluert, opprettes derfor de genererte finanspostene.</span><span class="sxs-lookup"><span data-stu-id="ce921-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>






