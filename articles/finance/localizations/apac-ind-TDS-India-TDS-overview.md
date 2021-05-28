---
title: Oversikt over indisk TDS (Tax Deducted at Source)
description: Dette emnet inneholder detaljert informasjon om indisk TDS (Tax Deducted at Source). TDS-dokumentasjonen omhandler funksjonaliteten til denne funksjonen.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023491"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="bcc44-104">Oversikt over indisk TDS (Tax Deducted at Source)</span><span class="sxs-lookup"><span data-stu-id="bcc44-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcc44-105">Dette emnet inneholder detaljert informasjon om indisk TDS (Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="bcc44-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="bcc44-106">TDS-dokumentasjonen omhandler funksjonaliteten til denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="bcc44-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="bcc44-107">Den forklarer også hvordan du foretar den grunnleggende konfigurasjonen for TDS, beregner TDS for transaksjoner, fullfører TDS-utligningsprosessen, registrerer TDS-sertifikatnumre og genererer TDS-forespørsler, TDS-oppgaver og TDS-sertifikater.</span><span class="sxs-lookup"><span data-stu-id="bcc44-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="bcc44-108">Dokumentasjonen inneholder følgende emner:</span><span class="sxs-lookup"><span data-stu-id="bcc44-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="bcc44-109">Grunnleggende konfigurasjon for TDS</span><span class="sxs-lookup"><span data-stu-id="bcc44-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="bcc44-110">Formeldesigner og terskelgrensefunksjonalitet som brukes til TDS-beregning</span><span class="sxs-lookup"><span data-stu-id="bcc44-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="bcc44-111">Beregning av TDS for fakturaer, betalinger, egenveksler og konserninterne transaksjoner</span><span class="sxs-lookup"><span data-stu-id="bcc44-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="bcc44-112">Periodisk TDS-utligningsprosess og utligning av TDS-beløp mot TDS-myndighetsleverandører</span><span class="sxs-lookup"><span data-stu-id="bcc44-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="bcc44-113">Registrere og oppdatere TDS-sertifikatnumre og -datoer</span><span class="sxs-lookup"><span data-stu-id="bcc44-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="bcc44-114">Innføring i TDS</span><span class="sxs-lookup"><span data-stu-id="bcc44-114">Introduction to TDS</span></span>

<span data-ttu-id="bcc44-115">I henhold til loven om avskriving per inntektsskatt fra 1961 blir inntektsskatt trukket fra ved kilden av mottakeren av tjenesten på tidspunktet for forskuddsbetaling eller regnskapsføring av kredit, avhengig av hva som kommer først.</span><span class="sxs-lookup"><span data-stu-id="bcc44-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="bcc44-116">Personen som foretar betalingen, må trekke fra avgiftsbeløpet og bare betale nettosaldoen til leverandøren av tjenesten.</span><span class="sxs-lookup"><span data-stu-id="bcc44-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="bcc44-117">TDS brukes på tjenester angitt av myndighetene, og avgiften trekkes fra ved hjelp av satsene som myndighetene angir for en periode.</span><span class="sxs-lookup"><span data-stu-id="bcc44-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="bcc44-118">Fradragssatsen er basert på statusen for enheten som mottar betalingen, eller som tilbyr tjenesten.</span><span class="sxs-lookup"><span data-stu-id="bcc44-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="bcc44-119">Statuser omfatter **Enkeltperson**, **HUF** (**Hindu Undivided Family**), **Selskap**, **Firma**, **AOP** (**Association of Persons**), **BOI** (**Body of Individuals**) og **Lokale myndigheter**.</span><span class="sxs-lookup"><span data-stu-id="bcc44-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="bcc44-120">Følgende deler viser tjenestene som TDS brukes på, som angitt av myndighetene i India.</span><span class="sxs-lookup"><span data-stu-id="bcc44-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="bcc44-121">**Beboere**</span><span class="sxs-lookup"><span data-stu-id="bcc44-121">**Residents**</span></span>

- <span data-ttu-id="bcc44-122">Inntekt fra lønn (i paragraf 192)</span><span class="sxs-lookup"><span data-stu-id="bcc44-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="bcc44-123">Inntekter fra rente på verdipapirer (i paragraf 193)</span><span class="sxs-lookup"><span data-stu-id="bcc44-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="bcc44-124">Inntekt fra aksjeutbytte (i paragraf 194)</span><span class="sxs-lookup"><span data-stu-id="bcc44-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="bcc44-125">Inntekt fra rente (i paragraf 194A)</span><span class="sxs-lookup"><span data-stu-id="bcc44-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="bcc44-126">Inntekt fra lotterier eller spill (i paragraf 194B)</span><span class="sxs-lookup"><span data-stu-id="bcc44-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="bcc44-127">Gevinst fra hesteveddeløp og så videre (i paragraf 194BB)</span><span class="sxs-lookup"><span data-stu-id="bcc44-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="bcc44-128">Oppdragstakere og underleverandører (i paragraf 194C)</span><span class="sxs-lookup"><span data-stu-id="bcc44-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="bcc44-129">Forsikringsprovisjon (i paragraf 194D)</span><span class="sxs-lookup"><span data-stu-id="bcc44-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="bcc44-130">Inntekt fra innbetaling i samsvar med nasjonal spareordning (i paragraf 194EE)</span><span class="sxs-lookup"><span data-stu-id="bcc44-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="bcc44-131">Inntekt fra aksjefond eller UTI (i paragraf 194F)</span><span class="sxs-lookup"><span data-stu-id="bcc44-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="bcc44-132">Provisjon, godtgjørelse, pris og så videre for salg eller lotteri (i paragraf 194G)</span><span class="sxs-lookup"><span data-stu-id="bcc44-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="bcc44-133">Betaling av provisjon eller meglerprovisjon (i paragraf 194H)</span><span class="sxs-lookup"><span data-stu-id="bcc44-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="bcc44-134">Leie (i paragraf 194I)</span><span class="sxs-lookup"><span data-stu-id="bcc44-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="bcc44-135">Profesjonell tjeneste (i paragraf 194J)</span><span class="sxs-lookup"><span data-stu-id="bcc44-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="bcc44-136">Inntekt fra aksjefondsenheter (i paragraf 194K)</span><span class="sxs-lookup"><span data-stu-id="bcc44-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="bcc44-137">Betaling av kompensasjon ved anskaffelse av visse faste eiendommer (i paragraf 194LA)</span><span class="sxs-lookup"><span data-stu-id="bcc44-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="bcc44-138">**Utlending**</span><span class="sxs-lookup"><span data-stu-id="bcc44-138">**Non-residents**</span></span>

- <span data-ttu-id="bcc44-139">Betalinger til utenlandske idrettsutøvere eller idrettslag (i paragraf 194E)</span><span class="sxs-lookup"><span data-stu-id="bcc44-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="bcc44-140">Andre summer (i paragraf 195)</span><span class="sxs-lookup"><span data-stu-id="bcc44-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="bcc44-141">Inntekt med hensyn til enheter av utlendinger (i paragraf 196A)</span><span class="sxs-lookup"><span data-stu-id="bcc44-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="bcc44-142">Inntekt fra utenlandske valutaobligasjoner eller aksjer i indisk selskap (i paragraf 196C)</span><span class="sxs-lookup"><span data-stu-id="bcc44-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="bcc44-143">Inntekter til utenlandske investorinstitusjoner fra verdipapirer (i paragraf 196D)</span><span class="sxs-lookup"><span data-stu-id="bcc44-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="bcc44-144">Lønn og alle andre positive inntekter under enhver inntektskilde (paragraf 192)</span><span class="sxs-lookup"><span data-stu-id="bcc44-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="bcc44-145">Renter på verdipapirer (paragraf 193)</span><span class="sxs-lookup"><span data-stu-id="bcc44-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="bcc44-146">Andre renter enn rente på verdipapirer (paragraf 194A)</span><span class="sxs-lookup"><span data-stu-id="bcc44-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="bcc44-147">Betalinger til oppdragstakere og underleverandører (paragraf 194C)</span><span class="sxs-lookup"><span data-stu-id="bcc44-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="bcc44-148">Gevinster fra lotteri eller kryssord (paragraf 194B)</span><span class="sxs-lookup"><span data-stu-id="bcc44-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="bcc44-149">Gevinster fra hesteveddeløp (paragraf 194BB)</span><span class="sxs-lookup"><span data-stu-id="bcc44-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="bcc44-150">Forsikringsprovisjon som dekker alle betalinger for anskaffelse av forsikringsvirksomhet (paragraf 194D)</span><span class="sxs-lookup"><span data-stu-id="bcc44-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="bcc44-151">Andre renter enn rente på verdipapirer som skal utstedes til utlendinger som ikke er et selskap, eller til et utenlandsk selskap (paragraf 195)</span><span class="sxs-lookup"><span data-stu-id="bcc44-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="bcc44-152">Betaling til utenlandsk idrettsutøver, inkludert idrettslag eller -institusjon.</span><span class="sxs-lookup"><span data-stu-id="bcc44-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="bcc44-153">Når det gjelder utenlandsk idrettsutøver, er betalinger med hensyn til annonser og artikler om alle kamper/idretter i India i aviser, tidsskrifter og så videre.</span><span class="sxs-lookup"><span data-stu-id="bcc44-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="bcc44-154">inkludert (paragraf 194E)</span><span class="sxs-lookup"><span data-stu-id="bcc44-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="bcc44-155">Betaling med hensyn til innbetalinger i samsvar med NSS \[National Savings Scheme\] (paragraf 194EE)</span><span class="sxs-lookup"><span data-stu-id="bcc44-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="bcc44-156">Betaling på grunn av tilbakekjøp av enheter ved aksjefond eller UTI (paragraf 194F)</span><span class="sxs-lookup"><span data-stu-id="bcc44-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="bcc44-157">Betaling for provisjon eller meglerprovisjon (paragraf 194H)</span><span class="sxs-lookup"><span data-stu-id="bcc44-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="bcc44-158">Betaling av leie (paragraf 194I)</span><span class="sxs-lookup"><span data-stu-id="bcc44-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="bcc44-159">Betaling av gebyrer for profesjonelle eller tekniske tjenester (paragraf 194J)</span><span class="sxs-lookup"><span data-stu-id="bcc44-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="bcc44-160">Provisjon til forhandlere, distributører, kjøpere og selgere av loddsedler, inkludert godtgjørelse eller pris på slike sedler (paragraf 194G)</span><span class="sxs-lookup"><span data-stu-id="bcc44-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="bcc44-161">Inntekt fra enheter som er kjøpt i utenlandsk valuta, eller langsiktig kapitalgevinst som skyldes overføring av slike enheter kjøpt i utenlandsk valuta (paragraf 196B)</span><span class="sxs-lookup"><span data-stu-id="bcc44-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="bcc44-162">Betaling av inntekter til utlendinger med hensyn til rente eller utbytte på verdipapirer og aksjer (paragraf 196C)</span><span class="sxs-lookup"><span data-stu-id="bcc44-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="bcc44-163">TDS beregnes for innkjøp, salg, salgsreturer, kreditnotaer, anleggsmiddelanskaffelser, forskuddsbetalinger, egenveksler, verksskatt og konserninterne transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="bcc44-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="bcc44-164">I det gjeldende indiske skattescenarioet beregnes ikke TDS på salgstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="bcc44-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="bcc44-165">Systemet omfatter imidlertid et tiltak for å beregne TDS som kan tilbakebetales på salgstransaksjoner, spesielt for konserninterne transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="bcc44-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="bcc44-166">Beregningen av TDS tar alltid hensyn til terskelen og unntaksterskelen som er definert for TDS-komponenten.</span><span class="sxs-lookup"><span data-stu-id="bcc44-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="bcc44-167">Den periodiske TDS-utligningsprosessen må kjøres, og TDS-betalingene må utlignes mot TDS-myndighetsleverandører.</span><span class="sxs-lookup"><span data-stu-id="bcc44-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="bcc44-168">Sertifikatnumrene og -datoene for TDS-sertifikater som mottas fra leverandører eller kunder, kan registreres og oppdateres.</span><span class="sxs-lookup"><span data-stu-id="bcc44-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="bcc44-169">De kvartalsvise oppgavene Form 26Q og Form 27Q samt sertifikatet Form 16A for TDS kan genereres i Finance.</span><span class="sxs-lookup"><span data-stu-id="bcc44-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="bcc44-170">Konfigurere og arbeide med TDS</span><span class="sxs-lookup"><span data-stu-id="bcc44-170">Setting up and working with TDS</span></span>

<span data-ttu-id="bcc44-171">Her er en oversikt over fremgangsmåten for å konfigurere og arbeide med TDS:</span><span class="sxs-lookup"><span data-stu-id="bcc44-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="bcc44-172">**TDS-konfigurasjon:**</span><span class="sxs-lookup"><span data-stu-id="bcc44-172">**TDS setup:**</span></span>

    - <span data-ttu-id="bcc44-173">Parameterkonfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="bcc44-173">Parameter setup:</span></span>

        - <span data-ttu-id="bcc44-174">Aktiver parametere som er knyttet til TDS, i Parametere for økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="bcc44-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="bcc44-175">Konfigurer nummerserien for kildeskattbetalinger i Parametere for økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="bcc44-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="bcc44-176">Konfigurer parametere i Leverandører og Kunder.</span><span class="sxs-lookup"><span data-stu-id="bcc44-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="bcc44-177">Grunnleggende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="bcc44-177">Basic setup:</span></span>

        - <span data-ttu-id="bcc44-178">Konfigurer TDS-registreringsnumre for et selskap, kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="bcc44-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="bcc44-179">Konfigurer TDS-komponentgrupper.</span><span class="sxs-lookup"><span data-stu-id="bcc44-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="bcc44-180">Konfigurer TDS-komponenter, knytt TDS-komponentgrupper til dem, og definer terskelen og unntaksterskelen for dem.</span><span class="sxs-lookup"><span data-stu-id="bcc44-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="bcc44-181">Konfigurer TDS-myndigheter.</span><span class="sxs-lookup"><span data-stu-id="bcc44-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="bcc44-182">Konfigurer TDS-utligningsperioder.</span><span class="sxs-lookup"><span data-stu-id="bcc44-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="bcc44-183">Konfigurer TDS-avgiftskoder, og knytt TDS-komponenter til dem.</span><span class="sxs-lookup"><span data-stu-id="bcc44-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="bcc44-184">Konfigurer TDS-avgiftsgrupper, og knytt TDS-avgiftskoder til dem.</span><span class="sxs-lookup"><span data-stu-id="bcc44-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="bcc44-185">I formeldesigneren definerer du en formel for å beregne TDS for en TDS-gruppe.</span><span class="sxs-lookup"><span data-stu-id="bcc44-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="bcc44-186">Registrer TDS-konsesjonssertifikatnumre.</span><span class="sxs-lookup"><span data-stu-id="bcc44-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="bcc44-187">Finanskontoer og selskapskonfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="bcc44-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="bcc44-188">Konfigurer leverandør- og kundefinanskontoer for TDS.</span><span class="sxs-lookup"><span data-stu-id="bcc44-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="bcc44-189">Konfigurer et kontonummer for avgiftsfradrag og -innkreving (TAN) og en kategori av typen deductor for selskapet.</span><span class="sxs-lookup"><span data-stu-id="bcc44-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="bcc44-190">Annen konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="bcc44-190">Other setup:</span></span>

        - <span data-ttu-id="bcc44-191">Konfigurer en betalingsplan som omfatter TDS-tildeling.</span><span class="sxs-lookup"><span data-stu-id="bcc44-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="bcc44-192">Konfigurer en betalingsgebyrtype for betalinger til TCS-myndigheten.</span><span class="sxs-lookup"><span data-stu-id="bcc44-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="bcc44-193">Konfigurer informasjon om TDS-grupper, permanente kontonumre (PAN) og TAN-numre for leverandører og kunder.</span><span class="sxs-lookup"><span data-stu-id="bcc44-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="bcc44-194">**Beregning av TDS i transaksjoner:**</span><span class="sxs-lookup"><span data-stu-id="bcc44-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="bcc44-195">Fakturaer og betalinger</span><span class="sxs-lookup"><span data-stu-id="bcc44-195">Invoices and payments</span></span>
    - <span data-ttu-id="bcc44-196">Egenveksler</span><span class="sxs-lookup"><span data-stu-id="bcc44-196">Promissory notes</span></span>
    - <span data-ttu-id="bcc44-197">Forskuddsbetalinger</span><span class="sxs-lookup"><span data-stu-id="bcc44-197">Advance payments</span></span>
    - <span data-ttu-id="bcc44-198">Forskuddsbetalinger</span><span class="sxs-lookup"><span data-stu-id="bcc44-198">Prepayments</span></span>

3. <span data-ttu-id="bcc44-199">**TDS-utligning:**</span><span class="sxs-lookup"><span data-stu-id="bcc44-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="bcc44-200">Periodisk TDS-utligningsprosess</span><span class="sxs-lookup"><span data-stu-id="bcc44-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="bcc44-201">Utligning av TDS-betalinger mot TDS-myndighetsleverandører og generering av TDS-challan</span><span class="sxs-lookup"><span data-stu-id="bcc44-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="bcc44-202">**TDS-forespørsler, -oppgaver og -sertifikat:**</span><span class="sxs-lookup"><span data-stu-id="bcc44-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="bcc44-203">Registrer og oppdater TDS-sertifikatnumre og -datoer.</span><span class="sxs-lookup"><span data-stu-id="bcc44-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="bcc44-204">Generer en TDS-forespørsel og en postert TDS-forespørsel.</span><span class="sxs-lookup"><span data-stu-id="bcc44-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="bcc44-205">Generer de kvartalsvise oppgavene Form 27A, Form 26Q og Form 27Q for TDS og e-TDS.</span><span class="sxs-lookup"><span data-stu-id="bcc44-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="bcc44-206">Generere et TDS-sertifikat for Form 16A.</span><span class="sxs-lookup"><span data-stu-id="bcc44-206">Generate a Form 16A TDS certificate.</span></span>
