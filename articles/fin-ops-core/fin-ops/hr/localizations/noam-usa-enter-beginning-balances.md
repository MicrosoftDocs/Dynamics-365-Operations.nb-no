---
title: Angi startsaldoer for lønn
description: Emnet beskriver fremgangsmåten for å angi startsaldoer for inntektskoder, fradrag, fordeler og avgifter.
author: andreabichsel
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9272828fe5d6e0bf131ea66353a0d5c3c7b1c4bd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752156"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="1340c-103">Angi startsaldoer for lønn</span><span class="sxs-lookup"><span data-stu-id="1340c-103">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1340c-104">Emnet beskriver fremgangsmåten for å angi startsaldoer for inntektskoder, fradrag, fordeler og avgifter.</span><span class="sxs-lookup"><span data-stu-id="1340c-104">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="1340c-105">Denne informasjonen er nyttig for partnere som overfører eller overfører data til en ny lønnsimplementering fra et annet system.</span><span class="sxs-lookup"><span data-stu-id="1340c-105">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="1340c-106">Ved klargjøring for å angi startsaldoer for lønn, kontrollerer vi følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="1340c-106">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="1340c-107">Ansattposter er angitt og tilgjengelige i systemet</span><span class="sxs-lookup"><span data-stu-id="1340c-107">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="1340c-108">Følgende data blir definert og tilordnet til ansatte:</span><span class="sxs-lookup"><span data-stu-id="1340c-108">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="1340c-109">Lønnssykluser og lønnsperioder</span><span class="sxs-lookup"><span data-stu-id="1340c-109">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="1340c-110">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="1340c-110">Earning codes</span></span>
    - <span data-ttu-id="1340c-111">Avgifter</span><span class="sxs-lookup"><span data-stu-id="1340c-111">Taxes</span></span>
    - <span data-ttu-id="1340c-112">Fordeler og fradrag</span><span class="sxs-lookup"><span data-stu-id="1340c-112">Benefits and deductions</span></span>

- <span data-ttu-id="1340c-113">Firmaet skal har valgt en dato der startsaldoer for lønn kan angis.</span><span class="sxs-lookup"><span data-stu-id="1340c-113">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="1340c-114">Informasjonen ble samlet om alle inntekter, fordeler/fradrag, fordelsbidrag, avgifter for ansatte, og arbeidstakeravgifter og arbeidsgiveravgifter deres og år til dato-beløp fra det gamle systemet.</span><span class="sxs-lookup"><span data-stu-id="1340c-114">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="1340c-115">Når du planlegger å skrive inn startsaldoer, bør du vurdere hvor detaljert dataene skal være.</span><span class="sxs-lookup"><span data-stu-id="1340c-115">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="1340c-116">De fleste bedrifter angir et enkelt, konsolidert år til dato-beløp.</span><span class="sxs-lookup"><span data-stu-id="1340c-116">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="1340c-117">Hvis du trenger mer informasjon, kan du imidlertid angi saldoer kvartalsvis.</span><span class="sxs-lookup"><span data-stu-id="1340c-117">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="1340c-118">Når nødvendig detaljnivå bestemmes, bestemmes også hvor mange manuelle lønnsoppgaver som må opprettes for hver arbeider.</span><span class="sxs-lookup"><span data-stu-id="1340c-118">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="1340c-119">For ett enkelt år til dato-beløp trengs det bare ett manuelt utdrag for hver ansatt.</span><span class="sxs-lookup"><span data-stu-id="1340c-119">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="1340c-120">Hvis du vil gjøre dette, bruker du år-til-dato-beløp fra den siste lønnsoppgaven fra det forrige systemet som beløp som angis i det nye lønningssystemet.</span><span class="sxs-lookup"><span data-stu-id="1340c-120">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="1340c-121">Følgende eksempel viser hvordan du kan angi startsaldoer for ansattes lønn, inkludert inntektskoder, fordeler/fradrag og avgifter.</span><span class="sxs-lookup"><span data-stu-id="1340c-121">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="1340c-122">I et eksempel fra virkeligheten vil du ha et linjeelement for hver inntektskode, fordelsfradrag, fordelsbidrag, ansattavgift og arbeidsgiveravgift med beløpet som er angitt som år-til-dato-beløpet.</span><span class="sxs-lookup"><span data-stu-id="1340c-122">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="1340c-123">Ved hjelp av den listen med koder og beløp, følger du trinnene for å opprette en manuell inntekts- og lønnsoppgave med regnskap deaktivert for å overføre startsaldoer til lønnsformål.</span><span class="sxs-lookup"><span data-stu-id="1340c-123">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="1340c-124">Du kan deaktivere regnskap fordi du ikke vil postere denne lønnsoppgavens startsaldo i Finans.</span><span class="sxs-lookup"><span data-stu-id="1340c-124">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="1340c-125">Som ble gjort i det gamle systemet og kommer til det nye systemet når du angir startsaldoer i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="1340c-125">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="1340c-126">A.</span><span class="sxs-lookup"><span data-stu-id="1340c-126">A.</span></span> <span data-ttu-id="1340c-127">Slik konfigurerer du inntektskoder som skal brukes på startsaldoer for lønn</span><span class="sxs-lookup"><span data-stu-id="1340c-127">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="1340c-128">Når du angir startssaldoer for lønn, må du kontrollere at inntektskodene som du vil bruke, er konfigurert med alternativet "Tillat redigering av inntektsoppgavesatser".</span><span class="sxs-lookup"><span data-stu-id="1340c-128">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="1340c-129">Dermed kan du taste beløpet fra det gamle systemet manuelt.</span><span class="sxs-lookup"><span data-stu-id="1340c-129">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="1340c-130">B.</span><span class="sxs-lookup"><span data-stu-id="1340c-130">B.</span></span> <span data-ttu-id="1340c-131">Opprette inntektsoppgaver for en ansatt med en startsaldo</span><span class="sxs-lookup"><span data-stu-id="1340c-131">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="1340c-132">Dette trinnet oppretter manuelt en inntektsoppgave for hver arbeider for den siste lønnsperioden av det gamle systemet, noe som oppretter inntektsoppgavelinjene i det nye lønnssystemet.</span><span class="sxs-lookup"><span data-stu-id="1340c-132">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="1340c-133">Angi én linje per inntektskode og år-til-dato-beløp og timer.</span><span class="sxs-lookup"><span data-stu-id="1340c-133">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="1340c-134">Eksempeltrinnene er som følger:</span><span class="sxs-lookup"><span data-stu-id="1340c-134">The sample steps are as follows:</span></span>

1. <span data-ttu-id="1340c-135">Åpne **Alle inntektsoppgaver**-siden og klikk **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1340c-135">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="1340c-136">Angi følgende:</span><span class="sxs-lookup"><span data-stu-id="1340c-136">Enter the following:</span></span> 

    | <span data-ttu-id="1340c-137">Felt</span><span class="sxs-lookup"><span data-stu-id="1340c-137">Field</span></span>      | <span data-ttu-id="1340c-138">Verdi</span><span class="sxs-lookup"><span data-stu-id="1340c-138">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="1340c-139">Arbeider</span><span class="sxs-lookup"><span data-stu-id="1340c-139">Worker</span></span>     | <span data-ttu-id="1340c-140">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="1340c-140">Michael Redmond</span></span>       |
    | <span data-ttu-id="1340c-141">Lønnssyklus</span><span class="sxs-lookup"><span data-stu-id="1340c-141">Pay cycle</span></span>  | <span data-ttu-id="1340c-142">sm</span><span class="sxs-lookup"><span data-stu-id="1340c-142">sm</span></span>                    |
    | <span data-ttu-id="1340c-143">Lønnsperiode</span><span class="sxs-lookup"><span data-stu-id="1340c-143">Pay period</span></span> | <span data-ttu-id="1340c-144">16/6/2017 – 30/06/2017</span><span class="sxs-lookup"><span data-stu-id="1340c-144">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="1340c-145">I fanen **Linje i inntektsoppgave** skriver du inn følgende:</span><span class="sxs-lookup"><span data-stu-id="1340c-145">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="1340c-146">Linje 1: fanen **Linje i inntektsoppgave**</span><span class="sxs-lookup"><span data-stu-id="1340c-146">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="1340c-147">Felt</span><span class="sxs-lookup"><span data-stu-id="1340c-147">Field</span></span>            | <span data-ttu-id="1340c-148">Verdi</span><span class="sxs-lookup"><span data-stu-id="1340c-148">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="1340c-149">Inntektskode</span><span class="sxs-lookup"><span data-stu-id="1340c-149">Earnings code</span></span>    | <span data-ttu-id="1340c-150">Vanlig lønn</span><span class="sxs-lookup"><span data-stu-id="1340c-150">Regular pay</span></span> |
    | <span data-ttu-id="1340c-151">Antall</span><span class="sxs-lookup"><span data-stu-id="1340c-151">Quantity</span></span>         | <span data-ttu-id="1340c-152">1.00</span><span class="sxs-lookup"><span data-stu-id="1340c-152">1.00</span></span>        |
    | <span data-ttu-id="1340c-153">Sats</span><span class="sxs-lookup"><span data-stu-id="1340c-153">Rate</span></span>             | <span data-ttu-id="1340c-154">30,000</span><span class="sxs-lookup"><span data-stu-id="1340c-154">30,000</span></span>      |
    | <span data-ttu-id="1340c-155">fanen Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="1340c-155">Line details tab</span></span> |             |
    | <span data-ttu-id="1340c-156">Manuell</span><span class="sxs-lookup"><span data-stu-id="1340c-156">Manual</span></span>           | <span data-ttu-id="1340c-157">(merket)</span><span class="sxs-lookup"><span data-stu-id="1340c-157">(marked)</span></span>    |

    <span data-ttu-id="1340c-158">Linje 2: fanen **Linje i inntektsoppgave**</span><span class="sxs-lookup"><span data-stu-id="1340c-158">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="1340c-159">Felt</span><span class="sxs-lookup"><span data-stu-id="1340c-159">Field</span></span>            | <span data-ttu-id="1340c-160">Verdi</span><span class="sxs-lookup"><span data-stu-id="1340c-160">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="1340c-161">Inntektskode</span><span class="sxs-lookup"><span data-stu-id="1340c-161">Earnings code</span></span>    | <span data-ttu-id="1340c-162">Bonus</span><span class="sxs-lookup"><span data-stu-id="1340c-162">Bonus</span></span>    |
    | <span data-ttu-id="1340c-163">Antall</span><span class="sxs-lookup"><span data-stu-id="1340c-163">Quantity</span></span>         | <span data-ttu-id="1340c-164">1.0000</span><span class="sxs-lookup"><span data-stu-id="1340c-164">1.0000</span></span>   |
    | <span data-ttu-id="1340c-165">Sats</span><span class="sxs-lookup"><span data-stu-id="1340c-165">Rate</span></span>             | <span data-ttu-id="1340c-166">4250.00</span><span class="sxs-lookup"><span data-stu-id="1340c-166">4250.00</span></span>  |
    | <span data-ttu-id="1340c-167">fanen Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="1340c-167">Line details tab</span></span> |          |
    | <span data-ttu-id="1340c-168">Manuell</span><span class="sxs-lookup"><span data-stu-id="1340c-168">Manual</span></span>           | <span data-ttu-id="1340c-169">(merket)</span><span class="sxs-lookup"><span data-stu-id="1340c-169">(marked)</span></span> |

    <span data-ttu-id="1340c-170">Linje 3: fanen **Linje i inntektsoppgave**</span><span class="sxs-lookup"><span data-stu-id="1340c-170">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="1340c-171">Felt</span><span class="sxs-lookup"><span data-stu-id="1340c-171">Field</span></span>           | <span data-ttu-id="1340c-172">Verdi</span><span class="sxs-lookup"><span data-stu-id="1340c-172">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="1340c-173">Inntektskode</span><span class="sxs-lookup"><span data-stu-id="1340c-173">Earnings code</span></span>   | <span data-ttu-id="1340c-174">Provisjon</span><span class="sxs-lookup"><span data-stu-id="1340c-174">Commission</span></span> |
    | <span data-ttu-id="1340c-175">Antall</span><span class="sxs-lookup"><span data-stu-id="1340c-175">Quantity</span></span>        | <span data-ttu-id="1340c-176">1.0000</span><span class="sxs-lookup"><span data-stu-id="1340c-176">1.0000</span></span>     |
    | <span data-ttu-id="1340c-177">Sats</span><span class="sxs-lookup"><span data-stu-id="1340c-177">Rate</span></span>            | <span data-ttu-id="1340c-178">!,299,00</span><span class="sxs-lookup"><span data-stu-id="1340c-178">!,299.00</span></span>   |
    | <span data-ttu-id="1340c-179">Sats</span><span class="sxs-lookup"><span data-stu-id="1340c-179">Rate</span></span>            | <span data-ttu-id="1340c-180">1,299.00</span><span class="sxs-lookup"><span data-stu-id="1340c-180">1,299.00</span></span>   |
    | <span data-ttu-id="1340c-181">fanen Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="1340c-181">Line detail tab</span></span> |            |
    | <span data-ttu-id="1340c-182">Manuell</span><span class="sxs-lookup"><span data-stu-id="1340c-182">Manual</span></span>          | <span data-ttu-id="1340c-183">(merket)</span><span class="sxs-lookup"><span data-stu-id="1340c-183">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="1340c-184">Å sette **Manuell**-glidebryteren til **Ja** i fanen **Linjedetaljer** for hver inntektsoppgave er nøkkelen til å få angitt startsaldoer for lønn for hver arbeider.</span><span class="sxs-lookup"><span data-stu-id="1340c-184">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="1340c-185">På **Handling**-ruten klikker du **Frigi inntektsoppgave** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="1340c-185">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="1340c-186">På **Handling**-ruten klikker du **Lønnsoppgave** for å åpne siden **Generer lønnsoppgaver**, og angi følgende:</span><span class="sxs-lookup"><span data-stu-id="1340c-186">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="1340c-187">Felt</span><span class="sxs-lookup"><span data-stu-id="1340c-187">Field</span></span>              | <span data-ttu-id="1340c-188">Verdi</span><span class="sxs-lookup"><span data-stu-id="1340c-188">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="1340c-189">Betalingsdato</span><span class="sxs-lookup"><span data-stu-id="1340c-189">Payment date</span></span>       | <span data-ttu-id="1340c-190">30/6/2017</span><span class="sxs-lookup"><span data-stu-id="1340c-190">6/30/2017</span></span> |
    | <span data-ttu-id="1340c-191">Betalingskjøringstype</span><span class="sxs-lookup"><span data-stu-id="1340c-191">Payment run type</span></span>   | <span data-ttu-id="1340c-192">Manuell</span><span class="sxs-lookup"><span data-stu-id="1340c-192">Manual</span></span>    |
    | <span data-ttu-id="1340c-193">Deaktiver regnskap</span><span class="sxs-lookup"><span data-stu-id="1340c-193">Disable accounting</span></span> |   <span data-ttu-id="1340c-194">Ja</span><span class="sxs-lookup"><span data-stu-id="1340c-194">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="1340c-195">Dette er bare tilgjengelig når betalingens kjøretype er manuell, og når brukeren ønsker å deaktivere regnskap på betalingskjøringen.</span><span class="sxs-lookup"><span data-stu-id="1340c-195">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="1340c-196">Klikk på **OK** og lukk **Infolog**.</span><span class="sxs-lookup"><span data-stu-id="1340c-196">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="1340c-197">Hvorfor må glidebryteren Deaktiver regnskap være satt til Ja ved generering av lønnsoppgaver?</span><span class="sxs-lookup"><span data-stu-id="1340c-197">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="1340c-198">Hvis du setter du glidebryteren til **Ja**, forhindres linjene i lønnsoppgaven fra å distribueres til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="1340c-198">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="1340c-199">Beløpene i økonomimodulen ble oppdatert tidligere da kontosaldoer fra det gamle systemet ble angitt.</span><span class="sxs-lookup"><span data-stu-id="1340c-199">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="1340c-200">Ved å angi startsaldoer for lønn kan du generere rapporter som inkluderer informasjon fra foregående år, i tillegg til for å identifisere grenser for fordeler og skatteformål.</span><span class="sxs-lookup"><span data-stu-id="1340c-200">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="1340c-201">C.</span><span class="sxs-lookup"><span data-stu-id="1340c-201">C.</span></span> <span data-ttu-id="1340c-202">Opprette lønnsoppgaver for ansatte</span><span class="sxs-lookup"><span data-stu-id="1340c-202">Create pay statements for employees</span></span>

<span data-ttu-id="1340c-203">Når du har generert lønnsoppgaver med startsaldoer, må du kontrollere at lønnsoppgavene gjenspeile lønnsdataene riktig.</span><span class="sxs-lookup"><span data-stu-id="1340c-203">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="1340c-204">Du må også oppdatere informasjon om fordeler og avgifter manuelt for å samsvare med verdiene i det forrige lønningssystemet.</span><span class="sxs-lookup"><span data-stu-id="1340c-204">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="1340c-205">Når du har bekreftet at beløpene fra forrige lønningssystem svarer til beløpene på de gjeldende lønnsoppgavene, må du fullføre lønnsoppgavene.</span><span class="sxs-lookup"><span data-stu-id="1340c-205">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="1340c-206">Åpne siden **Alle lønnsoppgaver**.</span><span class="sxs-lookup"><span data-stu-id="1340c-206">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="1340c-207">Merk den sist genererte lønnsoppgaven for Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="1340c-207">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="1340c-208">Klikk på **Rediger** for å åpne **Lønnsoppgave**-siden.</span><span class="sxs-lookup"><span data-stu-id="1340c-208">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="1340c-209">Åpne fanen **Fordelsfradrag** og angi følgende:</span><span class="sxs-lookup"><span data-stu-id="1340c-209">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="1340c-210">Felt</span><span class="sxs-lookup"><span data-stu-id="1340c-210">Field</span></span>             | <span data-ttu-id="1340c-211">Verdi</span><span class="sxs-lookup"><span data-stu-id="1340c-211">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="1340c-212">Fordel</span><span class="sxs-lookup"><span data-stu-id="1340c-212">Benefit</span></span>           | <span data-ttu-id="1340c-213">Fradragsbeløp</span><span class="sxs-lookup"><span data-stu-id="1340c-213">Deduction amount</span></span> |
    | <span data-ttu-id="1340c-214">401K</span><span class="sxs-lookup"><span data-stu-id="1340c-214">401K</span></span>              | <span data-ttu-id="1340c-215">Delta</span><span class="sxs-lookup"><span data-stu-id="1340c-215">Participate</span></span>      |
    | <span data-ttu-id="1340c-216">Tannforsikring</span><span class="sxs-lookup"><span data-stu-id="1340c-216">Dental</span></span>            | <span data-ttu-id="1340c-217">SubSp</span><span class="sxs-lookup"><span data-stu-id="1340c-217">SubSp</span></span>            |
    | <span data-ttu-id="1340c-218">Utgifter til pass og stell av barn</span><span class="sxs-lookup"><span data-stu-id="1340c-218">Dep care spending</span></span> | <span data-ttu-id="1340c-219">Delta</span><span class="sxs-lookup"><span data-stu-id="1340c-219">Participate</span></span>      |
    | <span data-ttu-id="1340c-220">Syn</span><span class="sxs-lookup"><span data-stu-id="1340c-220">Vision</span></span>            | <span data-ttu-id="1340c-221">SupSp</span><span class="sxs-lookup"><span data-stu-id="1340c-221">SupSp</span></span>            |

5. <span data-ttu-id="1340c-222">I fanen **Fordelsbidrag** angir du følgende:</span><span class="sxs-lookup"><span data-stu-id="1340c-222">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="1340c-223">Felt</span><span class="sxs-lookup"><span data-stu-id="1340c-223">Field</span></span>   | <span data-ttu-id="1340c-224">Verdi</span><span class="sxs-lookup"><span data-stu-id="1340c-224">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="1340c-225">Fordel</span><span class="sxs-lookup"><span data-stu-id="1340c-225">Benefit</span></span> | <span data-ttu-id="1340c-226">Bidragsbeløp</span><span class="sxs-lookup"><span data-stu-id="1340c-226">Contribution amount</span></span> |
    | <span data-ttu-id="1340c-227">401K</span><span class="sxs-lookup"><span data-stu-id="1340c-227">401K</span></span>    | <span data-ttu-id="1340c-228">Delta</span><span class="sxs-lookup"><span data-stu-id="1340c-228">Participate</span></span>         |
    | <span data-ttu-id="1340c-229">Tannforsikring</span><span class="sxs-lookup"><span data-stu-id="1340c-229">Dental</span></span>  | <span data-ttu-id="1340c-230">SubSp</span><span class="sxs-lookup"><span data-stu-id="1340c-230">SubSp</span></span>               |
    | <span data-ttu-id="1340c-231">Syn</span><span class="sxs-lookup"><span data-stu-id="1340c-231">Vision</span></span>  | <span data-ttu-id="1340c-232">SubSp</span><span class="sxs-lookup"><span data-stu-id="1340c-232">SubSp</span></span>               |

6. <span data-ttu-id="1340c-233">Angi følgende informasjon i fanen **Avgiftsfradrag**:</span><span class="sxs-lookup"><span data-stu-id="1340c-233">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="1340c-234">Felt</span><span class="sxs-lookup"><span data-stu-id="1340c-234">Field</span></span>           | <span data-ttu-id="1340c-235">Verdi</span><span class="sxs-lookup"><span data-stu-id="1340c-235">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="1340c-236">Mva-kode</span><span class="sxs-lookup"><span data-stu-id="1340c-236">Tax code</span></span>        | <span data-ttu-id="1340c-237">Fradragsbeløp</span><span class="sxs-lookup"><span data-stu-id="1340c-237">Deduction amount</span></span> |
    | <span data-ttu-id="1340c-238">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="1340c-238">USA-FED-ER-FICA</span></span> | <span data-ttu-id="1340c-239">1600.00</span><span class="sxs-lookup"><span data-stu-id="1340c-239">1600.00</span></span>          |
    | <span data-ttu-id="1340c-240">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="1340c-240">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="1340c-241">825.75</span><span class="sxs-lookup"><span data-stu-id="1340c-241">825.75</span></span>           |

7. <span data-ttu-id="1340c-242">Angi følgende informasjon i fanen **Avgiftsbidrag**:</span><span class="sxs-lookup"><span data-stu-id="1340c-242">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="1340c-243">Klikk på **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="1340c-243">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="1340c-244">Valider totalene i lønnsoppgaven for at de samsvarer med år-til-dato arbeiderens gamle system.</span><span class="sxs-lookup"><span data-stu-id="1340c-244">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="1340c-245">Det kan hende du vil vente med å sluttføre i det neste trinnet for å gjøre en generel validering av alle lønnsoppgaver samlet.</span><span class="sxs-lookup"><span data-stu-id="1340c-245">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="1340c-246">Etter validering kjører du gjennom alle lønnsoppgaver og sluttfører dem.</span><span class="sxs-lookup"><span data-stu-id="1340c-246">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="1340c-247">Den samme prosessen kan utføres kvartalsvis om nødvendig for alle tidligere kvartaler i hvert år.</span><span class="sxs-lookup"><span data-stu-id="1340c-247">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="1340c-248">Dette er bare nødvendig hvis kunden skal vise dataene kvartalsvis uten å gå tilbake til det gamle systemet.</span><span class="sxs-lookup"><span data-stu-id="1340c-248">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="1340c-249">Hvis du gjør en feil når du angir startsaldoer for en ansatt</span><span class="sxs-lookup"><span data-stu-id="1340c-249">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="1340c-250">Det er mulig å tilbakeføre, og skrive inn transaksjoner på nytt.</span><span class="sxs-lookup"><span data-stu-id="1340c-250">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="1340c-251">Hvis du vil tilbakeføre transaksjonen, trenger du bare å fullføre følgende trinn på siden **Alle lønnsoppgaver**.</span><span class="sxs-lookup"><span data-stu-id="1340c-251">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="1340c-252">Klikk på **Tilbakefør**.</span><span class="sxs-lookup"><span data-stu-id="1340c-252">Click **Reverse**.</span></span>
2. <span data-ttu-id="1340c-253">Klikk på **Ja** når meldingen «Når du tilbakefører denne lønnsoppgaven, opprettes en lønnsoppgave for tilbakeføring for å motregne denne lønnsoppgaven.</span><span class="sxs-lookup"><span data-stu-id="1340c-253">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="1340c-254">Ingen lønnsoppgave kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="1340c-254">Neither pay statement can be edited.</span></span> <span data-ttu-id="1340c-255">Du vil tilbakeføre denne lønnsoppgaven?"</span><span class="sxs-lookup"><span data-stu-id="1340c-255">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="1340c-256">vises.</span><span class="sxs-lookup"><span data-stu-id="1340c-256">displays.</span></span> 

<span data-ttu-id="1340c-257">Når du tilbakefører lønnsoppgaven, kan du generere en ny lønnsoppgave for arbeideren fra inntektsoppgaven som du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="1340c-257">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="1340c-258">Husk å rette opp eventuelle ukorrekte linjer på inntekstoppgaven før du genererer den nye lønnsoppgaven, og deretter generere nye lønnsoppgaver med riktig beløp.</span><span class="sxs-lookup"><span data-stu-id="1340c-258">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]