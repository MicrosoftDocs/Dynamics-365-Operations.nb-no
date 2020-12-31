---
title: Angi startsaldoer for lønn
description: Emnet beskriver fremgangsmåten for å angi startsaldoer for inntektskoder, fradrag, fordeler og avgifter. Denne informasjonen er nyttig for partnere for å overføre eller overføre data til en ny lønnsimplementering fra et annet system.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4411a6b72dbb7e6f5b1a72df8dbcbd54e265164c
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693408"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="35c0b-104">Angi startsaldoer for lønn</span><span class="sxs-lookup"><span data-stu-id="35c0b-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="35c0b-105">Emnet beskriver fremgangsmåten for å angi startsaldoer for inntektskoder, fradrag, fordeler og avgifter.</span><span class="sxs-lookup"><span data-stu-id="35c0b-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="35c0b-106">Denne informasjonen er nyttig for partnere som overfører eller overfører data til en ny lønnsimplementering fra et annet system.</span><span class="sxs-lookup"><span data-stu-id="35c0b-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="35c0b-107">Ved klargjøring for å angi startsaldoer for lønn, kontrollerer vi følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="35c0b-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="35c0b-108">Ansattposter er angitt og tilgjengelige i systemet</span><span class="sxs-lookup"><span data-stu-id="35c0b-108">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="35c0b-109">Følgende data blir definert og tilordnet til ansatte:</span><span class="sxs-lookup"><span data-stu-id="35c0b-109">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="35c0b-110">Lønnssykluser og lønnsperioder</span><span class="sxs-lookup"><span data-stu-id="35c0b-110">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="35c0b-111">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="35c0b-111">Earning codes</span></span>
    - <span data-ttu-id="35c0b-112">Avgifter</span><span class="sxs-lookup"><span data-stu-id="35c0b-112">Taxes</span></span>
    - <span data-ttu-id="35c0b-113">Fordeler og fradrag</span><span class="sxs-lookup"><span data-stu-id="35c0b-113">Benefits and deductions</span></span>

- <span data-ttu-id="35c0b-114">Firmaet skal har valgt en dato der startsaldoer for lønn kan angis.</span><span class="sxs-lookup"><span data-stu-id="35c0b-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="35c0b-115">Informasjonen ble samlet om alle inntekter, fordeler/fradrag, fordelsbidrag, avgifter for ansatte, og arbeidstakeravgifter og arbeidsgiveravgifter deres og år til dato-beløp fra det gamle systemet.</span><span class="sxs-lookup"><span data-stu-id="35c0b-115">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="35c0b-116">Når du planlegger å skrive inn startsaldoer, bør du vurdere hvor detaljert dataene skal være.</span><span class="sxs-lookup"><span data-stu-id="35c0b-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="35c0b-117">De fleste bedrifter angir et enkelt, konsolidert år til dato-beløp.</span><span class="sxs-lookup"><span data-stu-id="35c0b-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="35c0b-118">Hvis du trenger mer informasjon, kan du imidlertid angi saldoer kvartalsvis.</span><span class="sxs-lookup"><span data-stu-id="35c0b-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="35c0b-119">Når nødvendig detaljnivå bestemmes, bestemmes også hvor mange manuelle lønnsoppgaver som må opprettes for hver arbeider.</span><span class="sxs-lookup"><span data-stu-id="35c0b-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="35c0b-120">For ett enkelt år til dato-beløp trengs det bare ett manuelt utdrag for hver ansatt.</span><span class="sxs-lookup"><span data-stu-id="35c0b-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="35c0b-121">Hvis du vil gjøre dette, bruker du år-til-dato-beløp fra den siste lønnsoppgaven fra det forrige systemet som beløp som angis i det nye lønningssystemet.</span><span class="sxs-lookup"><span data-stu-id="35c0b-121">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="35c0b-122">Følgende eksempel viser hvordan du kan angi startsaldoer for ansattes lønn, inkludert inntektskoder, fordeler/fradrag og avgifter.</span><span class="sxs-lookup"><span data-stu-id="35c0b-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="35c0b-123">I et eksempel fra virkeligheten vil du ha et linjeelement for hver inntektskode, fordelsfradrag, fordelsbidrag, ansattavgift og arbeidsgiveravgift med beløpet som er angitt som år-til-dato-beløpet.</span><span class="sxs-lookup"><span data-stu-id="35c0b-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="35c0b-124">Ved hjelp av den listen med koder og beløp, følger du trinnene for å opprette en manuell inntekts- og lønnsoppgave med regnskap deaktivert for å overføre startsaldoer til lønnsformål.</span><span class="sxs-lookup"><span data-stu-id="35c0b-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="35c0b-125">Du kan deaktivere regnskap fordi du ikke vil postere denne lønnsoppgavens startsaldo i Finans.</span><span class="sxs-lookup"><span data-stu-id="35c0b-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="35c0b-126">Som ble gjort i det gamle systemet og kommer til det nye systemet når du angir startsaldoer i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="35c0b-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="35c0b-127">A.</span><span class="sxs-lookup"><span data-stu-id="35c0b-127">A.</span></span> <span data-ttu-id="35c0b-128">Slik konfigurerer du inntektskoder som skal brukes på startsaldoer for lønn</span><span class="sxs-lookup"><span data-stu-id="35c0b-128">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="35c0b-129">Når du angir startssaldoer for lønn, må du kontrollere at inntektskodene som du vil bruke, er konfigurert med alternativet "Tillat redigering av inntektsoppgavesatser".</span><span class="sxs-lookup"><span data-stu-id="35c0b-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="35c0b-130">Dermed kan du taste beløpet fra det gamle systemet manuelt.</span><span class="sxs-lookup"><span data-stu-id="35c0b-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="35c0b-131">B.</span><span class="sxs-lookup"><span data-stu-id="35c0b-131">B.</span></span> <span data-ttu-id="35c0b-132">Opprette inntektsoppgaver for en ansatt med en startsaldo</span><span class="sxs-lookup"><span data-stu-id="35c0b-132">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="35c0b-133">Dette trinnet oppretter manuelt en inntektsoppgave for hver arbeider for den siste lønnsperioden av det gamle systemet, noe som oppretter inntektsoppgavelinjene i det nye lønnssystemet.</span><span class="sxs-lookup"><span data-stu-id="35c0b-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="35c0b-134">Angi én linje per inntektskode og år-til-dato-beløp og timer.</span><span class="sxs-lookup"><span data-stu-id="35c0b-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="35c0b-135">Eksempeltrinnene er som følger:</span><span class="sxs-lookup"><span data-stu-id="35c0b-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="35c0b-136">Åpne **Alle inntektsoppgaver**-siden og klikk **Ny**.</span><span class="sxs-lookup"><span data-stu-id="35c0b-136">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="35c0b-137">Angi følgende:</span><span class="sxs-lookup"><span data-stu-id="35c0b-137">Enter the following:</span></span> 

    | <span data-ttu-id="35c0b-138">Felt</span><span class="sxs-lookup"><span data-stu-id="35c0b-138">Field</span></span>      | <span data-ttu-id="35c0b-139">Verdi</span><span class="sxs-lookup"><span data-stu-id="35c0b-139">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="35c0b-140">Arbeider</span><span class="sxs-lookup"><span data-stu-id="35c0b-140">Worker</span></span>     | <span data-ttu-id="35c0b-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="35c0b-141">Michael Redmond</span></span>       |
    | <span data-ttu-id="35c0b-142">Lønnssyklus</span><span class="sxs-lookup"><span data-stu-id="35c0b-142">Pay cycle</span></span>  | <span data-ttu-id="35c0b-143">sm</span><span class="sxs-lookup"><span data-stu-id="35c0b-143">sm</span></span>                    |
    | <span data-ttu-id="35c0b-144">Lønnsperiode</span><span class="sxs-lookup"><span data-stu-id="35c0b-144">Pay period</span></span> | <span data-ttu-id="35c0b-145">16/6/2017 – 30/06/2017</span><span class="sxs-lookup"><span data-stu-id="35c0b-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="35c0b-146">I kategorien **Linje i inntektsoppgave** skriver du inn følgende:</span><span class="sxs-lookup"><span data-stu-id="35c0b-146">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="35c0b-147">Linje 1: kategorien **Linje i inntektsoppgave**</span><span class="sxs-lookup"><span data-stu-id="35c0b-147">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="35c0b-148">Felt</span><span class="sxs-lookup"><span data-stu-id="35c0b-148">Field</span></span>            | <span data-ttu-id="35c0b-149">Verdi</span><span class="sxs-lookup"><span data-stu-id="35c0b-149">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="35c0b-150">Inntektskode</span><span class="sxs-lookup"><span data-stu-id="35c0b-150">Earnings code</span></span>    | <span data-ttu-id="35c0b-151">Vanlig lønn</span><span class="sxs-lookup"><span data-stu-id="35c0b-151">Regular pay</span></span> |
    | <span data-ttu-id="35c0b-152">Antall</span><span class="sxs-lookup"><span data-stu-id="35c0b-152">Quantity</span></span>         | <span data-ttu-id="35c0b-153">1.00</span><span class="sxs-lookup"><span data-stu-id="35c0b-153">1.00</span></span>        |
    | <span data-ttu-id="35c0b-154">Sats</span><span class="sxs-lookup"><span data-stu-id="35c0b-154">Rate</span></span>             | <span data-ttu-id="35c0b-155">30,000</span><span class="sxs-lookup"><span data-stu-id="35c0b-155">30,000</span></span>      |
    | <span data-ttu-id="35c0b-156">Kategorien Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="35c0b-156">Line details tab</span></span> |             |
    | <span data-ttu-id="35c0b-157">Manuell</span><span class="sxs-lookup"><span data-stu-id="35c0b-157">Manual</span></span>           | <span data-ttu-id="35c0b-158">(merket)</span><span class="sxs-lookup"><span data-stu-id="35c0b-158">(marked)</span></span>    |

    <span data-ttu-id="35c0b-159">Linje 2: kategorien **Linje i inntektsoppgave**</span><span class="sxs-lookup"><span data-stu-id="35c0b-159">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="35c0b-160">Felt</span><span class="sxs-lookup"><span data-stu-id="35c0b-160">Field</span></span>            | <span data-ttu-id="35c0b-161">Verdi</span><span class="sxs-lookup"><span data-stu-id="35c0b-161">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="35c0b-162">Inntektskode</span><span class="sxs-lookup"><span data-stu-id="35c0b-162">Earnings code</span></span>    | <span data-ttu-id="35c0b-163">Bonus</span><span class="sxs-lookup"><span data-stu-id="35c0b-163">Bonus</span></span>    |
    | <span data-ttu-id="35c0b-164">Antall</span><span class="sxs-lookup"><span data-stu-id="35c0b-164">Quantity</span></span>         | <span data-ttu-id="35c0b-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="35c0b-165">1.0000</span></span>   |
    | <span data-ttu-id="35c0b-166">Sats</span><span class="sxs-lookup"><span data-stu-id="35c0b-166">Rate</span></span>             | <span data-ttu-id="35c0b-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="35c0b-167">4250.00</span></span>  |
    | <span data-ttu-id="35c0b-168">Kategorien Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="35c0b-168">Line details tab</span></span> |          |
    | <span data-ttu-id="35c0b-169">Manuell</span><span class="sxs-lookup"><span data-stu-id="35c0b-169">Manual</span></span>           | <span data-ttu-id="35c0b-170">(merket)</span><span class="sxs-lookup"><span data-stu-id="35c0b-170">(marked)</span></span> |

    <span data-ttu-id="35c0b-171">Linje 3: kategorien **Linje i inntektsoppgave**</span><span class="sxs-lookup"><span data-stu-id="35c0b-171">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="35c0b-172">Felt</span><span class="sxs-lookup"><span data-stu-id="35c0b-172">Field</span></span>           | <span data-ttu-id="35c0b-173">Verdi</span><span class="sxs-lookup"><span data-stu-id="35c0b-173">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="35c0b-174">Inntektskode</span><span class="sxs-lookup"><span data-stu-id="35c0b-174">Earnings code</span></span>   | <span data-ttu-id="35c0b-175">Provisjon</span><span class="sxs-lookup"><span data-stu-id="35c0b-175">Commission</span></span> |
    | <span data-ttu-id="35c0b-176">Antall</span><span class="sxs-lookup"><span data-stu-id="35c0b-176">Quantity</span></span>        | <span data-ttu-id="35c0b-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="35c0b-177">1.0000</span></span>     |
    | <span data-ttu-id="35c0b-178">Sats</span><span class="sxs-lookup"><span data-stu-id="35c0b-178">Rate</span></span>            | <span data-ttu-id="35c0b-179">!,299,00</span><span class="sxs-lookup"><span data-stu-id="35c0b-179">!,299.00</span></span>   |
    | <span data-ttu-id="35c0b-180">Sats</span><span class="sxs-lookup"><span data-stu-id="35c0b-180">Rate</span></span>            | <span data-ttu-id="35c0b-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="35c0b-181">1,299.00</span></span>   |
    | <span data-ttu-id="35c0b-182">Kategorien Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="35c0b-182">Line detail tab</span></span> |            |
    | <span data-ttu-id="35c0b-183">Manuell</span><span class="sxs-lookup"><span data-stu-id="35c0b-183">Manual</span></span>          | <span data-ttu-id="35c0b-184">(merket)</span><span class="sxs-lookup"><span data-stu-id="35c0b-184">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="35c0b-185">Å sette **Manuell**-glidebryteren til **Ja** i kategorien **Linjedetaljer** for hver inntektsoppgave er nøkkelen til å få angitt startsaldoer for lønn for hver arbeider.</span><span class="sxs-lookup"><span data-stu-id="35c0b-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="35c0b-186">På **Handling**-ruten klikker du **Frigi inntektsoppgave** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="35c0b-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="35c0b-187">På **Handling**-ruten klikker du **Lønnsoppgave** for å åpne siden **Generer lønnsoppgaver**, og angi følgende:</span><span class="sxs-lookup"><span data-stu-id="35c0b-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="35c0b-188">Felt</span><span class="sxs-lookup"><span data-stu-id="35c0b-188">Field</span></span>              | <span data-ttu-id="35c0b-189">Verdi</span><span class="sxs-lookup"><span data-stu-id="35c0b-189">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="35c0b-190">Betalingsdato</span><span class="sxs-lookup"><span data-stu-id="35c0b-190">Payment date</span></span>       | <span data-ttu-id="35c0b-191">30/6/2017</span><span class="sxs-lookup"><span data-stu-id="35c0b-191">6/30/2017</span></span> |
    | <span data-ttu-id="35c0b-192">Betalingskjøringstype</span><span class="sxs-lookup"><span data-stu-id="35c0b-192">Payment run type</span></span>   | <span data-ttu-id="35c0b-193">Manuell</span><span class="sxs-lookup"><span data-stu-id="35c0b-193">Manual</span></span>    |
    | <span data-ttu-id="35c0b-194">Deaktiver regnskap</span><span class="sxs-lookup"><span data-stu-id="35c0b-194">Disable accounting</span></span> |   <span data-ttu-id="35c0b-195">Ja</span><span class="sxs-lookup"><span data-stu-id="35c0b-195">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="35c0b-196">Dette er bare tilgjengelig når betalingens kjøretype er manuell, og når brukeren ønsker å deaktivere regnskap på betalingskjøringen.</span><span class="sxs-lookup"><span data-stu-id="35c0b-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="35c0b-197">Klikk **OK** og lukk **Infolog**.</span><span class="sxs-lookup"><span data-stu-id="35c0b-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="35c0b-198">Hvorfor må glidebryteren Deaktiver regnskap være satt til Ja ved generering av lønnsoppgaver?</span><span class="sxs-lookup"><span data-stu-id="35c0b-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="35c0b-199">Hvis du setter du glidebryteren til **Ja**, forhindres linjene i lønnsoppgaven fra å distribueres til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="35c0b-199">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="35c0b-200">Beløpene i økonomimodulen ble oppdatert tidligere da kontosaldoer fra det gamle systemet ble angitt.</span><span class="sxs-lookup"><span data-stu-id="35c0b-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="35c0b-201">Ved å angi startsaldoer for lønn kan du generere rapporter som inkluderer informasjon fra foregående år, i tillegg til for å identifisere grenser for fordeler og skatteformål.</span><span class="sxs-lookup"><span data-stu-id="35c0b-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="35c0b-202">C.</span><span class="sxs-lookup"><span data-stu-id="35c0b-202">C.</span></span> <span data-ttu-id="35c0b-203">Opprette lønnsoppgaver for ansatte</span><span class="sxs-lookup"><span data-stu-id="35c0b-203">Create pay statements for employees</span></span>

<span data-ttu-id="35c0b-204">Når du har generert lønnsoppgaver med startsaldoer, må du kontrollere at lønnsoppgavene gjenspeile lønnsdataene riktig.</span><span class="sxs-lookup"><span data-stu-id="35c0b-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="35c0b-205">Du må også oppdatere informasjon om fordeler og avgifter manuelt for å samsvare med verdiene i det forrige lønningssystemet.</span><span class="sxs-lookup"><span data-stu-id="35c0b-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="35c0b-206">Når du har bekreftet at beløpene fra forrige lønningssystem svarer til beløpene på de gjeldende lønnsoppgavene, må du fullføre lønnsoppgavene.</span><span class="sxs-lookup"><span data-stu-id="35c0b-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="35c0b-207">Åpne siden **Alle lønnsoppgaver**.</span><span class="sxs-lookup"><span data-stu-id="35c0b-207">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="35c0b-208">Merk den sist genererte lønnsoppgaven for Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="35c0b-208">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="35c0b-209">Klikk **Rediger** for å åpne **Lønnsoppgave**-siden.</span><span class="sxs-lookup"><span data-stu-id="35c0b-209">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="35c0b-210">Åpne kategorien **Fordelsfradrag** og angi følgende:</span><span class="sxs-lookup"><span data-stu-id="35c0b-210">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="35c0b-211">Felt</span><span class="sxs-lookup"><span data-stu-id="35c0b-211">Field</span></span>             | <span data-ttu-id="35c0b-212">Verdi</span><span class="sxs-lookup"><span data-stu-id="35c0b-212">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="35c0b-213">Fordel</span><span class="sxs-lookup"><span data-stu-id="35c0b-213">Benefit</span></span>           | <span data-ttu-id="35c0b-214">Fradragsbeløp</span><span class="sxs-lookup"><span data-stu-id="35c0b-214">Deduction amount</span></span> |
    | <span data-ttu-id="35c0b-215">401K</span><span class="sxs-lookup"><span data-stu-id="35c0b-215">401K</span></span>              | <span data-ttu-id="35c0b-216">Delta</span><span class="sxs-lookup"><span data-stu-id="35c0b-216">Participate</span></span>      |
    | <span data-ttu-id="35c0b-217">Tannforsikring</span><span class="sxs-lookup"><span data-stu-id="35c0b-217">Dental</span></span>            | <span data-ttu-id="35c0b-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="35c0b-218">SubSp</span></span>            |
    | <span data-ttu-id="35c0b-219">Utgifter til pass og stell av barn</span><span class="sxs-lookup"><span data-stu-id="35c0b-219">Dep care spending</span></span> | <span data-ttu-id="35c0b-220">Delta</span><span class="sxs-lookup"><span data-stu-id="35c0b-220">Participate</span></span>      |
    | <span data-ttu-id="35c0b-221">Syn</span><span class="sxs-lookup"><span data-stu-id="35c0b-221">Vision</span></span>            | <span data-ttu-id="35c0b-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="35c0b-222">SupSp</span></span>            |

5. <span data-ttu-id="35c0b-223">I kategorien **Fordelsbidrag** angir du følgende:</span><span class="sxs-lookup"><span data-stu-id="35c0b-223">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="35c0b-224">Felt</span><span class="sxs-lookup"><span data-stu-id="35c0b-224">Field</span></span>   | <span data-ttu-id="35c0b-225">Verdi</span><span class="sxs-lookup"><span data-stu-id="35c0b-225">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="35c0b-226">Fordel</span><span class="sxs-lookup"><span data-stu-id="35c0b-226">Benefit</span></span> | <span data-ttu-id="35c0b-227">Bidragsbeløp</span><span class="sxs-lookup"><span data-stu-id="35c0b-227">Contribution amount</span></span> |
    | <span data-ttu-id="35c0b-228">401K</span><span class="sxs-lookup"><span data-stu-id="35c0b-228">401K</span></span>    | <span data-ttu-id="35c0b-229">Delta</span><span class="sxs-lookup"><span data-stu-id="35c0b-229">Participate</span></span>         |
    | <span data-ttu-id="35c0b-230">Tannforsikring</span><span class="sxs-lookup"><span data-stu-id="35c0b-230">Dental</span></span>  | <span data-ttu-id="35c0b-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="35c0b-231">SubSp</span></span>               |
    | <span data-ttu-id="35c0b-232">Syn</span><span class="sxs-lookup"><span data-stu-id="35c0b-232">Vision</span></span>  | <span data-ttu-id="35c0b-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="35c0b-233">SubSp</span></span>               |

6. <span data-ttu-id="35c0b-234">Angi følgende informasjon i kategorien **Avgiftsfradrag**:</span><span class="sxs-lookup"><span data-stu-id="35c0b-234">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="35c0b-235">Felt</span><span class="sxs-lookup"><span data-stu-id="35c0b-235">Field</span></span>           | <span data-ttu-id="35c0b-236">Verdi</span><span class="sxs-lookup"><span data-stu-id="35c0b-236">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="35c0b-237">Mva-kode</span><span class="sxs-lookup"><span data-stu-id="35c0b-237">Tax code</span></span>        | <span data-ttu-id="35c0b-238">Fradragsbeløp</span><span class="sxs-lookup"><span data-stu-id="35c0b-238">Deduction amount</span></span> |
    | <span data-ttu-id="35c0b-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="35c0b-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="35c0b-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="35c0b-240">1600.00</span></span>          |
    | <span data-ttu-id="35c0b-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="35c0b-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="35c0b-242">825.75</span><span class="sxs-lookup"><span data-stu-id="35c0b-242">825.75</span></span>           |

7. <span data-ttu-id="35c0b-243">Angi følgende informasjon i kategorien **Avgiftsbidrag**:</span><span class="sxs-lookup"><span data-stu-id="35c0b-243">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="35c0b-244">Klikk **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="35c0b-244">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="35c0b-245">Valider totalene i lønnsoppgaven for at de samsvarer med år-til-dato arbeiderens gamle system.</span><span class="sxs-lookup"><span data-stu-id="35c0b-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="35c0b-246">Det kan hende du vil vente med å sluttføre i det neste trinnet for å gjøre en generel validering av alle lønnsoppgaver samlet.</span><span class="sxs-lookup"><span data-stu-id="35c0b-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="35c0b-247">Etter validering kjører du gjennom alle lønnsoppgaver og sluttfører dem.</span><span class="sxs-lookup"><span data-stu-id="35c0b-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="35c0b-248">Den samme prosessen kan utføres kvartalsvis om nødvendig for alle tidligere kvartaler i hvert år.</span><span class="sxs-lookup"><span data-stu-id="35c0b-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="35c0b-249">Dette er bare nødvendig hvis kunden skal vise dataene kvartalsvis uten å gå tilbake til det gamle systemet.</span><span class="sxs-lookup"><span data-stu-id="35c0b-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="35c0b-250">Hvis du gjør en feil når du angir startsaldoer for en ansatt</span><span class="sxs-lookup"><span data-stu-id="35c0b-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="35c0b-251">Det er mulig å tilbakeføre, og skrive inn transaksjoner på nytt.</span><span class="sxs-lookup"><span data-stu-id="35c0b-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="35c0b-252">Hvis du vil tilbakeføre transaksjonen, trenger du bare å fullføre følgende trinn på siden **Alle lønnsoppgaver**.</span><span class="sxs-lookup"><span data-stu-id="35c0b-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="35c0b-253">Klikk **Tilbakefør**.</span><span class="sxs-lookup"><span data-stu-id="35c0b-253">Click **Reverse**.</span></span>
2. <span data-ttu-id="35c0b-254">Klikk **Ja** når meldingen «Når du tilbakefører denne lønnsoppgaven, opprettes en lønnsoppgave for tilbakeføring for å motregne denne lønnsoppgaven.</span><span class="sxs-lookup"><span data-stu-id="35c0b-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="35c0b-255">Ingen lønnsoppgave kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="35c0b-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="35c0b-256">Du vil tilbakeføre denne lønnsoppgaven?"</span><span class="sxs-lookup"><span data-stu-id="35c0b-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="35c0b-257">vises.</span><span class="sxs-lookup"><span data-stu-id="35c0b-257">displays.</span></span> 

<span data-ttu-id="35c0b-258">Når du tilbakefører lønnsoppgaven, kan du generere en ny lønnsoppgave for arbeideren fra inntektsoppgaven som du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="35c0b-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="35c0b-259">Husk å rette opp eventuelle ukorrekte linjer på inntekstoppgaven før du genererer den nye lønnsoppgaven, og deretter generere nye lønnsoppgaver med riktig beløp.</span><span class="sxs-lookup"><span data-stu-id="35c0b-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 
