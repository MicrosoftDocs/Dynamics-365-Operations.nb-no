---
title: "Angi startsaldoer for lønn"
description: "Emnet beskriver fremgangsmåten for å angi startsaldoer for inntektskoder, fradrag, fordeler og avgifter. Denne informasjonen er nyttig for partnere for å overføre eller overføre data til en ny lønnsimplementering fra et annet system."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 1e7bdfca55e1bdaba0b5ebdf55b46744e584ab2c
ms.contentlocale: nb-no
ms.lasthandoff: 12/18/2018

---

# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="ad784-104">Angi startsaldoer for lønn</span><span class="sxs-lookup"><span data-stu-id="ad784-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad784-105">Emnet beskriver fremgangsmåten for å angi startsaldoer for inntektskoder, fradrag, fordeler og avgifter.</span><span class="sxs-lookup"><span data-stu-id="ad784-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="ad784-106">Denne informasjonen er nyttig for partnere som overfører eller overfører data til en ny lønnsimplementering fra et annet system.</span><span class="sxs-lookup"><span data-stu-id="ad784-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="ad784-107">Ved klargjøring for å angi startsaldoer for lønn, kontrollerer vi følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="ad784-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="ad784-108">Ansattposter er angitt og tilgjengelige i systemet</span><span class="sxs-lookup"><span data-stu-id="ad784-108">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="ad784-109">Følgende data blir definert og tilordnet til ansatte:</span><span class="sxs-lookup"><span data-stu-id="ad784-109">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="ad784-110">Lønnssykluser og lønnsperioder</span><span class="sxs-lookup"><span data-stu-id="ad784-110">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="ad784-111">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="ad784-111">Earning codes</span></span>
    - <span data-ttu-id="ad784-112">Avgifter</span><span class="sxs-lookup"><span data-stu-id="ad784-112">Taxes</span></span>
    - <span data-ttu-id="ad784-113">Fordeler og fradrag</span><span class="sxs-lookup"><span data-stu-id="ad784-113">Benefits and deductions</span></span>

- <span data-ttu-id="ad784-114">Firmaet skal har valgt en dato der startsaldoer for lønn kan angis.</span><span class="sxs-lookup"><span data-stu-id="ad784-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="ad784-115">Informasjonen ble samlet om alle inntekter, fordeler/fradrag, fordelsbidrag, avgifter for ansatte, og arbeidstakeravgifter og arbeidsgiveravgifter deres og år til dato-beløp fra det gamle systemet.</span><span class="sxs-lookup"><span data-stu-id="ad784-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="ad784-116">Når du planlegger å skrive inn startsaldoer, bør du vurdere hvor detaljert dataene skal være.</span><span class="sxs-lookup"><span data-stu-id="ad784-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="ad784-117">De fleste bedrifter angir et enkelt, konsolidert år til dato-beløp.</span><span class="sxs-lookup"><span data-stu-id="ad784-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="ad784-118">Hvis du trenger mer informasjon, kan du imidlertid angi saldoer kvartalsvis.</span><span class="sxs-lookup"><span data-stu-id="ad784-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="ad784-119">Når nødvendig detaljnivå bestemmes, bestemmes også hvor mange manuelle lønnsoppgaver som må opprettes for hver arbeider.</span><span class="sxs-lookup"><span data-stu-id="ad784-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="ad784-120">For ett enkelt år til dato-beløp trengs det bare ett manuelt utdrag for hver ansatt.</span><span class="sxs-lookup"><span data-stu-id="ad784-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="ad784-121">Hvis vil gjøre dette bruker du år-til-dato-beløp fra den siste lønnsoppgaven fra forrige systemet som beløp som angis i det nye lønningssystemet.</span><span class="sxs-lookup"><span data-stu-id="ad784-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="ad784-122">Følgende eksempel viser hvordan du kan angi startsaldoer for ansattes lønn, inkludert inntektskoder, fordeler/fradrag og avgifter.</span><span class="sxs-lookup"><span data-stu-id="ad784-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="ad784-123">I et eksempel fra virkeligheten vil du ha et linjeelement for hver inntektskode, fordelsfradrag, fordelsbidrag, ansattavgift og arbeidsgiveravgift med beløpet som er angitt som år-til-dato-beløpet.</span><span class="sxs-lookup"><span data-stu-id="ad784-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="ad784-124">Ved hjelp av den listen med koder og beløp, følger du trinnene for å opprette en manuell inntekts- og lønnsoppgave med regnskap deaktivert for å overføre startsaldoer til lønnsformål.</span><span class="sxs-lookup"><span data-stu-id="ad784-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="ad784-125">Du kan deaktivere regnskap fordi du ikke vil postere denne lønnsoppgavens startsaldo i Finans.</span><span class="sxs-lookup"><span data-stu-id="ad784-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="ad784-126">Som ble gjort i det gamle systemet og kommer til det nye systemet når du angir startsaldoer i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="ad784-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="ad784-127">A.</span><span class="sxs-lookup"><span data-stu-id="ad784-127">A.</span></span> <span data-ttu-id="ad784-128">Slik konfigurerer du inntektskoder som skal brukes på startsaldoer for lønn</span><span class="sxs-lookup"><span data-stu-id="ad784-128">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="ad784-129">Når du angir startssaldoer for lønn, må du kontrollere at inntektskodene som du vil bruke, er konfigurert med alternativet "Tillat redigering av inntektsoppgavesatser".</span><span class="sxs-lookup"><span data-stu-id="ad784-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="ad784-130">Dermed kan du taste beløpet fra det gamle systemet manuelt.</span><span class="sxs-lookup"><span data-stu-id="ad784-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="ad784-131">B.</span><span class="sxs-lookup"><span data-stu-id="ad784-131">B.</span></span> <span data-ttu-id="ad784-132">Opprette inntektsoppgaver for en ansatt med en startsaldo</span><span class="sxs-lookup"><span data-stu-id="ad784-132">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="ad784-133">Dette trinnet oppretter manuelt en inntektsoppgave for hver arbeider for den siste lønnsperioden av det gamle systemet, noe som oppretter inntektsoppgavelinjene i det nye lønnssystemet.</span><span class="sxs-lookup"><span data-stu-id="ad784-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="ad784-134">Angi én linje per inntektskode og år-til-dato-beløp og timer.</span><span class="sxs-lookup"><span data-stu-id="ad784-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="ad784-135">Eksempeltrinnene er som følger:</span><span class="sxs-lookup"><span data-stu-id="ad784-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="ad784-136">Åpne **Alle inntektsoppgaver**-siden og klikk **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ad784-136">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="ad784-137">Angi følgende:</span><span class="sxs-lookup"><span data-stu-id="ad784-137">Enter the following:</span></span> 

    | <span data-ttu-id="ad784-138">Felt</span><span class="sxs-lookup"><span data-stu-id="ad784-138">Field</span></span>      | <span data-ttu-id="ad784-139">Verdi</span><span class="sxs-lookup"><span data-stu-id="ad784-139">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="ad784-140">Arbeider</span><span class="sxs-lookup"><span data-stu-id="ad784-140">Worker</span></span>     | <span data-ttu-id="ad784-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="ad784-141">Michael Redmond</span></span>       |
    | <span data-ttu-id="ad784-142">Lønnssyklus</span><span class="sxs-lookup"><span data-stu-id="ad784-142">Pay cycle</span></span>  | <span data-ttu-id="ad784-143">sm</span><span class="sxs-lookup"><span data-stu-id="ad784-143">sm</span></span>                    |
    | <span data-ttu-id="ad784-144">Lønnsperiode</span><span class="sxs-lookup"><span data-stu-id="ad784-144">Pay period</span></span> | <span data-ttu-id="ad784-145">16/6/2017 – 30/06/2017</span><span class="sxs-lookup"><span data-stu-id="ad784-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="ad784-146">I kategorien **Linje i inntektsoppgave** skriver du inn følgende:</span><span class="sxs-lookup"><span data-stu-id="ad784-146">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="ad784-147">Linje 1: kategorien **Linje i inntektsoppgave**</span><span class="sxs-lookup"><span data-stu-id="ad784-147">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="ad784-148">Felt</span><span class="sxs-lookup"><span data-stu-id="ad784-148">Field</span></span>            | <span data-ttu-id="ad784-149">Verdi</span><span class="sxs-lookup"><span data-stu-id="ad784-149">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="ad784-150">Inntektskode</span><span class="sxs-lookup"><span data-stu-id="ad784-150">Earnings code</span></span>    | <span data-ttu-id="ad784-151">Vanlig lønn</span><span class="sxs-lookup"><span data-stu-id="ad784-151">Regular pay</span></span> |
    | <span data-ttu-id="ad784-152">Antall</span><span class="sxs-lookup"><span data-stu-id="ad784-152">Quantity</span></span>         | <span data-ttu-id="ad784-153">1,00</span><span class="sxs-lookup"><span data-stu-id="ad784-153">1.00</span></span>        |
    | <span data-ttu-id="ad784-154">Område</span><span class="sxs-lookup"><span data-stu-id="ad784-154">Rage</span></span>             | <span data-ttu-id="ad784-155">30 000</span><span class="sxs-lookup"><span data-stu-id="ad784-155">30,000</span></span>      |
    | <span data-ttu-id="ad784-156">Kategorien Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="ad784-156">Line details tab</span></span> |             |
    | <span data-ttu-id="ad784-157">Manuell</span><span class="sxs-lookup"><span data-stu-id="ad784-157">Manual</span></span>           | <span data-ttu-id="ad784-158">(merket)</span><span class="sxs-lookup"><span data-stu-id="ad784-158">(marked)</span></span>    |

    <span data-ttu-id="ad784-159">Linje 2: kategorien **Linje i inntektsoppgave**</span><span class="sxs-lookup"><span data-stu-id="ad784-159">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="ad784-160">Felt</span><span class="sxs-lookup"><span data-stu-id="ad784-160">Field</span></span>            | <span data-ttu-id="ad784-161">Verdi</span><span class="sxs-lookup"><span data-stu-id="ad784-161">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="ad784-162">Inntektskode</span><span class="sxs-lookup"><span data-stu-id="ad784-162">Earnings code</span></span>    | <span data-ttu-id="ad784-163">Bonus</span><span class="sxs-lookup"><span data-stu-id="ad784-163">Bonus</span></span>    |
    | <span data-ttu-id="ad784-164">Antall</span><span class="sxs-lookup"><span data-stu-id="ad784-164">Quantity</span></span>         | <span data-ttu-id="ad784-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="ad784-165">1.0000</span></span>   |
    | <span data-ttu-id="ad784-166">Sats</span><span class="sxs-lookup"><span data-stu-id="ad784-166">Rate</span></span>             | <span data-ttu-id="ad784-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="ad784-167">4250.00</span></span>  |
    | <span data-ttu-id="ad784-168">Kategorien Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="ad784-168">Line details tab</span></span> |          |
    | <span data-ttu-id="ad784-169">Manuell</span><span class="sxs-lookup"><span data-stu-id="ad784-169">Manual</span></span>           | <span data-ttu-id="ad784-170">(merket)</span><span class="sxs-lookup"><span data-stu-id="ad784-170">(marked)</span></span> |

    <span data-ttu-id="ad784-171">Linje 3: kategorien **Linje i inntektsoppgave**</span><span class="sxs-lookup"><span data-stu-id="ad784-171">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="ad784-172">Felt</span><span class="sxs-lookup"><span data-stu-id="ad784-172">Field</span></span>           | <span data-ttu-id="ad784-173">Verdi</span><span class="sxs-lookup"><span data-stu-id="ad784-173">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="ad784-174">Inntektskode</span><span class="sxs-lookup"><span data-stu-id="ad784-174">Earnings code</span></span>   | <span data-ttu-id="ad784-175">Provisjon</span><span class="sxs-lookup"><span data-stu-id="ad784-175">Commission</span></span> |
    | <span data-ttu-id="ad784-176">Antall</span><span class="sxs-lookup"><span data-stu-id="ad784-176">Quantity</span></span>        | <span data-ttu-id="ad784-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="ad784-177">1.0000</span></span>     |
    | <span data-ttu-id="ad784-178">Sats</span><span class="sxs-lookup"><span data-stu-id="ad784-178">Rate</span></span>            | <span data-ttu-id="ad784-179">!,299,00</span><span class="sxs-lookup"><span data-stu-id="ad784-179">!,299.00</span></span>   |
    | <span data-ttu-id="ad784-180">Sats</span><span class="sxs-lookup"><span data-stu-id="ad784-180">Rate</span></span>            | <span data-ttu-id="ad784-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="ad784-181">1,299.00</span></span>   |
    | <span data-ttu-id="ad784-182">Kategorien Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="ad784-182">Line detail tab</span></span> |            |
    | <span data-ttu-id="ad784-183">Manuell</span><span class="sxs-lookup"><span data-stu-id="ad784-183">Manual</span></span>          | <span data-ttu-id="ad784-184">(merket)</span><span class="sxs-lookup"><span data-stu-id="ad784-184">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="ad784-185">Å sette **Manuell**-glidebryteren til **Ja** i kategorien **Linjedetaljer** for hver inntektsoppgave er nøkkelen til å få angitt startsaldoer for lønn for hver arbeider.</span><span class="sxs-lookup"><span data-stu-id="ad784-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="ad784-186">På **Handling**-ruten klikker du **Frigi inntektsoppgave** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="ad784-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="ad784-187">På **Handling**-ruten klikker du **Lønnsoppgave** for å åpne siden **Generer lønnsoppgaver**, og angi følgende:</span><span class="sxs-lookup"><span data-stu-id="ad784-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="ad784-188">Felt</span><span class="sxs-lookup"><span data-stu-id="ad784-188">Field</span></span>              | <span data-ttu-id="ad784-189">Verdi</span><span class="sxs-lookup"><span data-stu-id="ad784-189">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="ad784-190">Betalingsdato</span><span class="sxs-lookup"><span data-stu-id="ad784-190">Payment date</span></span>       | <span data-ttu-id="ad784-191">30/6/2017</span><span class="sxs-lookup"><span data-stu-id="ad784-191">6/30/2017</span></span> |
    | <span data-ttu-id="ad784-192">Betalingskjøringstype</span><span class="sxs-lookup"><span data-stu-id="ad784-192">Payment run type</span></span>   | <span data-ttu-id="ad784-193">Manuell</span><span class="sxs-lookup"><span data-stu-id="ad784-193">Manual</span></span>    |
    | <span data-ttu-id="ad784-194">Deaktiver regnskap</span><span class="sxs-lookup"><span data-stu-id="ad784-194">Disable accounting</span></span> |   <span data-ttu-id="ad784-195">Ja</span><span class="sxs-lookup"><span data-stu-id="ad784-195">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="ad784-196">Dette er bare tilgjengelig når betalingens kjøretype er manuell, og når brukeren ønsker å deaktivere regnskap på betalingskjøringen.</span><span class="sxs-lookup"><span data-stu-id="ad784-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="ad784-197">Klikk **OK** og lukk **Infolog**.</span><span class="sxs-lookup"><span data-stu-id="ad784-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="ad784-198">Hvorfor må glidebryteren Deaktiver regnskap være satt til Ja ved generering av lønnsoppgaver?</span><span class="sxs-lookup"><span data-stu-id="ad784-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="ad784-199">Hvis du setter du glidebryteren til **Ja**, forhindres linjene i lønnsoppgaven fra å distribueres til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="ad784-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="ad784-200">Beløpene i økonomimodulen ble oppdatert tidligere da kontosaldoer fra det gamle systemet ble angitt.</span><span class="sxs-lookup"><span data-stu-id="ad784-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="ad784-201">Ved å angi startsaldoer for lønn kan du generere rapporter som inkluderer informasjon fra foregående år, i tillegg til for å identifisere grenser for fordeler og skatteformål.</span><span class="sxs-lookup"><span data-stu-id="ad784-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="ad784-202">C.</span><span class="sxs-lookup"><span data-stu-id="ad784-202">C.</span></span> <span data-ttu-id="ad784-203">Opprette lønnsoppgaver for ansatte</span><span class="sxs-lookup"><span data-stu-id="ad784-203">Create pay statements for employees</span></span>

<span data-ttu-id="ad784-204">Når du har generert lønnsoppgaver med startsaldoer, må du kontrollere at lønnsoppgavene gjenspeile lønnsdataene riktig.</span><span class="sxs-lookup"><span data-stu-id="ad784-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="ad784-205">Du må også oppdatere informasjon om fordeler og avgifter manuelt for å samsvare med verdiene i det forrige lønningssystemet.</span><span class="sxs-lookup"><span data-stu-id="ad784-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="ad784-206">Når du har bekreftet at beløpene fra forrige lønningssystem svarer til beløpene på de gjeldende lønnsoppgavene, må du fullføre lønnsoppgavene.</span><span class="sxs-lookup"><span data-stu-id="ad784-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="ad784-207">Åpne siden **Alle lønnsoppgaver**.</span><span class="sxs-lookup"><span data-stu-id="ad784-207">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="ad784-208">Merk den sist genererte lønnsoppgaven for Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="ad784-208">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="ad784-209">Klikk **Rediger** for å åpne **Lønnsoppgave**-siden.</span><span class="sxs-lookup"><span data-stu-id="ad784-209">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="ad784-210">Åpne kategorien **Fordelsfradrag** og angi følgende:</span><span class="sxs-lookup"><span data-stu-id="ad784-210">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="ad784-211">Felt</span><span class="sxs-lookup"><span data-stu-id="ad784-211">Field</span></span>             | <span data-ttu-id="ad784-212">Verdi</span><span class="sxs-lookup"><span data-stu-id="ad784-212">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="ad784-213">Fordel</span><span class="sxs-lookup"><span data-stu-id="ad784-213">Benefit</span></span>           | <span data-ttu-id="ad784-214">Fradragsbeløp</span><span class="sxs-lookup"><span data-stu-id="ad784-214">Deduction amount</span></span> |
    | <span data-ttu-id="ad784-215">401K</span><span class="sxs-lookup"><span data-stu-id="ad784-215">401K</span></span>              | <span data-ttu-id="ad784-216">Delta</span><span class="sxs-lookup"><span data-stu-id="ad784-216">Participate</span></span>      |
    | <span data-ttu-id="ad784-217">Tannforsikring</span><span class="sxs-lookup"><span data-stu-id="ad784-217">Dental</span></span>            | <span data-ttu-id="ad784-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="ad784-218">SubSp</span></span>            |
    | <span data-ttu-id="ad784-219">Utgifter til pass og stell av barn</span><span class="sxs-lookup"><span data-stu-id="ad784-219">Dep care spending</span></span> | <span data-ttu-id="ad784-220">Delta</span><span class="sxs-lookup"><span data-stu-id="ad784-220">Participate</span></span>      |
    | <span data-ttu-id="ad784-221">Syn</span><span class="sxs-lookup"><span data-stu-id="ad784-221">Vision</span></span>            | <span data-ttu-id="ad784-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="ad784-222">SupSp</span></span>            |

5. <span data-ttu-id="ad784-223">I kategorien **Fordelsbidrag** angir du følgende:</span><span class="sxs-lookup"><span data-stu-id="ad784-223">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="ad784-224">Felt</span><span class="sxs-lookup"><span data-stu-id="ad784-224">Field</span></span>   | <span data-ttu-id="ad784-225">Verdi</span><span class="sxs-lookup"><span data-stu-id="ad784-225">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="ad784-226">Fordel</span><span class="sxs-lookup"><span data-stu-id="ad784-226">Benefit</span></span> | <span data-ttu-id="ad784-227">Bidragsbeløp</span><span class="sxs-lookup"><span data-stu-id="ad784-227">Contribution amount</span></span> |
    | <span data-ttu-id="ad784-228">401K</span><span class="sxs-lookup"><span data-stu-id="ad784-228">401K</span></span>    | <span data-ttu-id="ad784-229">Delta</span><span class="sxs-lookup"><span data-stu-id="ad784-229">Participate</span></span>         |
    | <span data-ttu-id="ad784-230">Tannforsikring</span><span class="sxs-lookup"><span data-stu-id="ad784-230">Dental</span></span>  | <span data-ttu-id="ad784-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="ad784-231">SubSp</span></span>               |
    | <span data-ttu-id="ad784-232">Syn</span><span class="sxs-lookup"><span data-stu-id="ad784-232">Vision</span></span>  | <span data-ttu-id="ad784-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="ad784-233">SubSp</span></span>               |

6. <span data-ttu-id="ad784-234">Angi følgende informasjon i kategorien **Avgiftsfradrag**:</span><span class="sxs-lookup"><span data-stu-id="ad784-234">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="ad784-235">Felt</span><span class="sxs-lookup"><span data-stu-id="ad784-235">Field</span></span>           | <span data-ttu-id="ad784-236">Verdi</span><span class="sxs-lookup"><span data-stu-id="ad784-236">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="ad784-237">Mva-kode</span><span class="sxs-lookup"><span data-stu-id="ad784-237">Tax code</span></span>        | <span data-ttu-id="ad784-238">Fradragsbeløp</span><span class="sxs-lookup"><span data-stu-id="ad784-238">Deduction amount</span></span> |
    | <span data-ttu-id="ad784-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="ad784-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="ad784-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="ad784-240">1600.00</span></span>          |
    | <span data-ttu-id="ad784-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="ad784-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="ad784-242">825.75</span><span class="sxs-lookup"><span data-stu-id="ad784-242">825.75</span></span>           |

7. <span data-ttu-id="ad784-243">Angi følgende informasjon i kategorien **Avgiftsbidrag**:</span><span class="sxs-lookup"><span data-stu-id="ad784-243">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="ad784-244">Klikk **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="ad784-244">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="ad784-245">Valider totalene i lønnsoppgaven for at de samsvarer med år-til-dato arbeiderens gamle system.</span><span class="sxs-lookup"><span data-stu-id="ad784-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="ad784-246">Det kan hende du vil vente med å sluttføre i det neste trinnet for å gjøre en generel validering av alle lønnsoppgaver samlet.</span><span class="sxs-lookup"><span data-stu-id="ad784-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="ad784-247">Etter validering kjører du gjennom alle lønnsoppgaver og sluttfører dem.</span><span class="sxs-lookup"><span data-stu-id="ad784-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="ad784-248">Den samme prosessen kan utføres kvartalsvis om nødvendig for alle tidligere kvartaler i hvert år.</span><span class="sxs-lookup"><span data-stu-id="ad784-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="ad784-249">Dette er bare nødvendig hvis kunden skal vise dataene kvartalsvis uten å gå tilbake til det gamle systemet.</span><span class="sxs-lookup"><span data-stu-id="ad784-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="ad784-250">Hvis du gjør en feil når du angir startsaldoer for en ansatt</span><span class="sxs-lookup"><span data-stu-id="ad784-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="ad784-251">Det er mulig å tilbakeføre, og skrive inn transaksjoner på nytt.</span><span class="sxs-lookup"><span data-stu-id="ad784-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="ad784-252">Hvis du vil tilbakeføre transaksjonen, trenger du bare å fullføre følgende trinn på siden **Alle lønnsoppgaver**.</span><span class="sxs-lookup"><span data-stu-id="ad784-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="ad784-253">Klikk **Tilbakefør**.</span><span class="sxs-lookup"><span data-stu-id="ad784-253">Click **Reverse**.</span></span>
2. <span data-ttu-id="ad784-254">Klikk **Ja** når meldingen «Når du tilbakefører denne lønnsoppgaven, opprettes en lønnsoppgave for tilbakeføring for å motregne denne lønnsoppgaven.</span><span class="sxs-lookup"><span data-stu-id="ad784-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="ad784-255">Ingen lønnsoppgave kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="ad784-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="ad784-256">Du vil tilbakeføre denne lønnsoppgaven?"</span><span class="sxs-lookup"><span data-stu-id="ad784-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="ad784-257">vises.</span><span class="sxs-lookup"><span data-stu-id="ad784-257">displays.</span></span> 

<span data-ttu-id="ad784-258">Når du tilbakefører lønnsoppgaven, kan du generere en ny lønnsoppgave for arbeideren fra inntektsoppgaven som du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="ad784-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="ad784-259">Husk å rette opp eventuelle ukorrekte linjer på inntekstoppgaven før du genererer den nye lønnsoppgaven, og deretter generere nye lønnsoppgaver med riktig beløp.</span><span class="sxs-lookup"><span data-stu-id="ad784-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 

