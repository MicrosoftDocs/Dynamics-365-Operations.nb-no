---
title: Konfigurere reiseregning
description: "Denne artikkelen beskriver vurderingene og beslutningene som du må ta i planleggingsprosessen før du konfigurerer Reiseregning og utlegg i Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e213c4436452ddf1d0e22d791c7ee2cee803edc7
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="configure-expense-management"></a><span data-ttu-id="f5988-103">Konfigurere reiseregning</span><span class="sxs-lookup"><span data-stu-id="f5988-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5988-104">Dette emnet beskriver vurderingene og beslutningene som du må ta i planleggingsprosessen før du konfigurerer Reiseregning og utlegg i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f5988-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="f5988-105">I Reiseregning kan du lagre informasjon om betalingsmetoder, reiserekvisisjoner, utgiftsrapporter, retningslinjer, og så videre.</span><span class="sxs-lookup"><span data-stu-id="f5988-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="f5988-106">Fordi mange av valgene du gjør når du planlegger konfigurasjonen for Reiseregning og utlegg, er basert på organisasjonens hierarki og økonomiske struktur, må du referere til planleggingsdokumentene for disse områdene.</span><span class="sxs-lookup"><span data-stu-id="f5988-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="f5988-107">Konserninterne utgifter</span><span class="sxs-lookup"><span data-stu-id="f5988-107">Intercompany expenses</span></span>

<span data-ttu-id="f5988-108">Når du aktiverer konserninterne utgifter, tillater du juridiske personer og ansatte å pådra seg utgifter på vegne av en annen juridisk enhet, og samle inn betaling fra den juridiske enheten for ansettelse i organisasjonen din.</span><span class="sxs-lookup"><span data-stu-id="f5988-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="f5988-109">For eksempel, en ansatt i juridisk enhet A fullfører et prosjekt for juridisk enhet B, og prosjektet har reiserelaterte utgifter.</span><span class="sxs-lookup"><span data-stu-id="f5988-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="f5988-110">Hvis konserninterne utgifter er aktivert kan ansatte sende inn en utgiftsrapport som legger utgiften til juridisk enhet B, og utgiften må da betales av juridisk enhet A. Hvis organisasjonen ikke har flere juridiske enheter, trenger du ikke å aktivere konserninterne utgifter.</span><span class="sxs-lookup"><span data-stu-id="f5988-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="f5988-111">**Beslutning:** Vil du aktivere konserninterne utgifter?</span><span class="sxs-lookup"><span data-stu-id="f5988-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="f5988-112">Økonomistyring</span><span class="sxs-lookup"><span data-stu-id="f5988-112">Financial management</span></span>

<span data-ttu-id="f5988-113">Reiseregning og utlegg er tett integrert med økonomistyring av organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="f5988-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="f5988-114">Mange konfigurasjoner for reiseregning vil være basert på de beslutningene du har gjort for organisasjonens økonomi.</span><span class="sxs-lookup"><span data-stu-id="f5988-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="f5988-115">I de følgende avsnittene beskrives de ulike områdene som krever planlegging og beslutninger, basert på organisasjonens økonomiske beslutninger og veiledning fra lederskapet ditt.</span><span class="sxs-lookup"><span data-stu-id="f5988-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="f5988-116">Kostgodtgjørelse</span><span class="sxs-lookup"><span data-stu-id="f5988-116">Per diems</span></span>

<span data-ttu-id="f5988-117">Du må definere kostgodtgjørelse for ansatte som organisasjonen gir.</span><span class="sxs-lookup"><span data-stu-id="f5988-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="f5988-118">Fordi kostgodtgjørelse vanligvis brukes til å dekke utgifter som måltider, overnatting og andre tilfeldige utgifter, kan du opprette regler for kostgodtgjørelse som organisasjonen skal tilby.</span><span class="sxs-lookup"><span data-stu-id="f5988-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="f5988-119">kostgodtgjørelsessatser kan være basert på tid på året, reisestedet, eller begge deler.</span><span class="sxs-lookup"><span data-stu-id="f5988-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="f5988-120">Når du definerer en kostgodtgjørelsesregel, kan du angi at en prosentandel av kostgodtgjørelsessatsen skal holdes tilbake hvis en arbeider mottar gratis måltider eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="f5988-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="f5988-121">Du kan også definere kostgodtgjørelsessatser for å angi minimum og maksimum antall timer som kostgodtgjørelsessatsen kan brukes på en arbeiders reise.</span><span class="sxs-lookup"><span data-stu-id="f5988-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="f5988-122">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="f5988-122">**Decisions:**</span></span>

- <span data-ttu-id="f5988-123">Standard kostgodtgjørelsesregler for de første og siste dagene:</span><span class="sxs-lookup"><span data-stu-id="f5988-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="f5988-124">Hva er minste antall timer en ansatt kan kreve for en dag og fremdeles motta kostgodtgjørelse?</span><span class="sxs-lookup"><span data-stu-id="f5988-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="f5988-125">Er det en reduksjon i beløpet som tilbys for måltider for første dag og siste dag?</span><span class="sxs-lookup"><span data-stu-id="f5988-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="f5988-126">Hvis det er en reduksjon, hva er prosentsatsen for reduksjonen?</span><span class="sxs-lookup"><span data-stu-id="f5988-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="f5988-127">Er det en reduksjon i beløpet som tilbys for et hotell for den første og siste dagen?</span><span class="sxs-lookup"><span data-stu-id="f5988-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="f5988-128">Hvis det er en reduksjon, hva er prosentsatsen for reduksjonen?</span><span class="sxs-lookup"><span data-stu-id="f5988-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="f5988-129">Er det en reduksjon i beløpet som tilbys for andre utgifter som påløper første dag og siste dag?</span><span class="sxs-lookup"><span data-stu-id="f5988-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="f5988-130">Hvis det er en reduksjon, hva er prosentsatsen for reduksjonen?</span><span class="sxs-lookup"><span data-stu-id="f5988-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="f5988-131">Standard kostgodtgjørelseregler:</span><span class="sxs-lookup"><span data-stu-id="f5988-131">Default per diem rules:</span></span>

    - <span data-ttu-id="f5988-132">Finnes det en prosentvis reduksjon i kostgodtgjørelsen for hvert måltid hvis måltidet eksempelvis er gratis?</span><span class="sxs-lookup"><span data-stu-id="f5988-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="f5988-133">Hvis det er en reduksjon, hva er reduksjonsprosentsatsen for hvert måltid?</span><span class="sxs-lookup"><span data-stu-id="f5988-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="f5988-134">Beregnes måltidsreduksjonen per dag, per tur eller etter antall måltider per dag?</span><span class="sxs-lookup"><span data-stu-id="f5988-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="f5988-135">Bør kostgodtgjørelsesbeløp avrundes på vanlig måte eller rundes opp?</span><span class="sxs-lookup"><span data-stu-id="f5988-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="f5988-136">Beregnes kostgodtgjørelse basert på en periode på 24 timer eller en kalenderdag?</span><span class="sxs-lookup"><span data-stu-id="f5988-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="f5988-137">Kostgodtgjørelse er basert på lokasjon:</span><span class="sxs-lookup"><span data-stu-id="f5988-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="f5988-138">Er kostgodtgjørelsen ulik basert på lokasjon?</span><span class="sxs-lookup"><span data-stu-id="f5988-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="f5988-139">Hvilke lokasjoner inkluderes?</span><span class="sxs-lookup"><span data-stu-id="f5988-139">What locations are included?</span></span>
    - <span data-ttu-id="f5988-140">Hvis kostgodtgjørelsen er ulik basert på lokasjon, hva er prosentsats og beløp som tilbys for følgende typer utgifter, for hver lokasjon:</span><span class="sxs-lookup"><span data-stu-id="f5988-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="f5988-141">Måltider</span><span class="sxs-lookup"><span data-stu-id="f5988-141">Meals</span></span>
        - <span data-ttu-id="f5988-142">Hotell</span><span class="sxs-lookup"><span data-stu-id="f5988-142">Hotel</span></span>
        - <span data-ttu-id="f5988-143">Andre utgifter</span><span class="sxs-lookup"><span data-stu-id="f5988-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="f5988-144">Journaler og kontoer for reiseregninger og utlegg</span><span class="sxs-lookup"><span data-stu-id="f5988-144">Expense management journals and accounts</span></span>

<span data-ttu-id="f5988-145">Administrasjon av reiseregninger og utlegg krever at du bruker flere journaler og kontoer.</span><span class="sxs-lookup"><span data-stu-id="f5988-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="f5988-146">Du må angi for eksempel om den samme kontoen brukes for forskudd og kredittkorttvister.</span><span class="sxs-lookup"><span data-stu-id="f5988-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="f5988-147">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="f5988-147">**Decisions:**</span></span>

- <span data-ttu-id="f5988-148">Hvilken finansjournal posteres godkjente reiseregninger til?</span><span class="sxs-lookup"><span data-stu-id="f5988-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="f5988-149">Hvilken konto brukes til forskudd?</span><span class="sxs-lookup"><span data-stu-id="f5988-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="f5988-150">Bør forskudd posteres umiddelbart?</span><span class="sxs-lookup"><span data-stu-id="f5988-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="f5988-151">Betalingsmåter</span><span class="sxs-lookup"><span data-stu-id="f5988-151">Payment methods</span></span>

<span data-ttu-id="f5988-152">Når du lar ansatte pådra seg utgifter på vegne av firmaet, må du definere betalingsmåtene som ansatte kan bruke.</span><span class="sxs-lookup"><span data-stu-id="f5988-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="f5988-153">Du kan for eksempel tillate at ansatte kan bruke kontanter eller et firmakredittkort.</span><span class="sxs-lookup"><span data-stu-id="f5988-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="f5988-154">Du kan også tillate at ansatte skal bruke personlige kredittkort, og deretter tilbakebetale de ansatte.</span><span class="sxs-lookup"><span data-stu-id="f5988-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="f5988-155">Du må ta følgende avgjørelser for hver enkelt betalingsmåte du godkjenner.</span><span class="sxs-lookup"><span data-stu-id="f5988-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="f5988-156">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="f5988-156">**Decisions:**</span></span>

- <span data-ttu-id="f5988-157">Hvilke betalingsmåter er tillatt?</span><span class="sxs-lookup"><span data-stu-id="f5988-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="f5988-158">Hvem eier betalingsmåteutgiftene?</span><span class="sxs-lookup"><span data-stu-id="f5988-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="f5988-159">Finnes det en motkontotype?</span><span class="sxs-lookup"><span data-stu-id="f5988-159">Is there an offset account type?</span></span> <span data-ttu-id="f5988-160">Hvis det finnes en motkontotype, hva er den?</span><span class="sxs-lookup"><span data-stu-id="f5988-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="f5988-161">Hvis det finnes en motkonto, hva er kontoen?</span><span class="sxs-lookup"><span data-stu-id="f5988-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="f5988-162">Hvis betalingsmåten er et kredittkort, bør betalingsmåten bare brukes med importerte transaksjoner?</span><span class="sxs-lookup"><span data-stu-id="f5988-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="f5988-163">Utgiftskategorier og delte kategorier</span><span class="sxs-lookup"><span data-stu-id="f5988-163">Expense categories and shared categories</span></span>

<span data-ttu-id="f5988-164">Når ansatte oppretter en reiseregning, må hver utgift de registrerer, være tilknyttet en utgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="f5988-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="f5988-165">Utgiftskategorier er hentet fra delte kategorier som kan deles på tvers av juridiske enheter i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="f5988-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="f5988-166">Disse kategoriene kan også deles i Prosjektledelse og regnskap, avhengig av hvordan organisasjonen din er definert.</span><span class="sxs-lookup"><span data-stu-id="f5988-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="f5988-167">Basert på definisjonen for organisasjonen din og veiledningen fra implementeringsteamet, avgjør om kategoriene som brukes i Reiseregning kun skal brukes i Reiseregning, eller om de skal deles mellom Prosjektledelse og regnskap og Utgiftsstyring.</span><span class="sxs-lookup"><span data-stu-id="f5988-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="f5988-168">Legg merke til at disse kategoriene kan deles mellom prosjekt og utgifter eller prosjekt og produksjon, men ikke mellom utgifter og produksjon.</span><span class="sxs-lookup"><span data-stu-id="f5988-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="f5988-169">Du må ta følgende avgjørelser for hver utgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="f5988-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="f5988-170">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="f5988-170">**Decisions:**</span></span>

- <span data-ttu-id="f5988-171">Hva er utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="f5988-171">What is the expense category?</span></span> <span data-ttu-id="f5988-172">Eksempler inkluderer kategorier for flyreiser, hotell eller kjørelengde.</span><span class="sxs-lookup"><span data-stu-id="f5988-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="f5988-173">Kan utgiftskategorien også brukes i Prosjektledelse og regnskap?</span><span class="sxs-lookup"><span data-stu-id="f5988-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="f5988-174">Hva er utgiftstypen?</span><span class="sxs-lookup"><span data-stu-id="f5988-174">What is the expense type?</span></span>
- <span data-ttu-id="f5988-175">Hva er standard betalingsmåte for utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="f5988-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="f5988-176">Skal utgifter i utgiftskategorien spesifiseres?</span><span class="sxs-lookup"><span data-stu-id="f5988-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="f5988-177">Hva er hovedstandardkontoen for utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="f5988-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="f5988-178">Hva er standard mva-gruppe for vare for utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="f5988-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="f5988-179">Er flere betalingsmåter tillatt for utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="f5988-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="f5988-180">Hvis flere betalingsmåter er tillatt, hva er de?</span><span class="sxs-lookup"><span data-stu-id="f5988-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="f5988-181">Er det underkategorier i denne utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="f5988-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="f5988-182">Hvis det er underkategorier, må du også gjøre følgende beslutninger:</span><span class="sxs-lookup"><span data-stu-id="f5988-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="f5988-183">Er noen av underkategoriene utelatt fra skatterefusjon?</span><span class="sxs-lookup"><span data-stu-id="f5988-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="f5988-184">Hva er mva-gruppe for vare for underkategoriene?</span><span class="sxs-lookup"><span data-stu-id="f5988-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="f5988-185">Hvis utgiftskategorien også brukes i Prosjektledelse og regnskap, besvar følgende gjenstående spørsmål</span><span class="sxs-lookup"><span data-stu-id="f5988-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="f5988-186">Eller gå videre til neste del.</span><span class="sxs-lookup"><span data-stu-id="f5988-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="f5988-187">Hvilke kostnadsregnskap vil bli brukt til følgende utgifter?</span><span class="sxs-lookup"><span data-stu-id="f5988-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="f5988-188">Kostnad</span><span class="sxs-lookup"><span data-stu-id="f5988-188">Cost</span></span>
    - <span data-ttu-id="f5988-189">Lønnsfordeling</span><span class="sxs-lookup"><span data-stu-id="f5988-189">Payroll allocation</span></span>
    - <span data-ttu-id="f5988-190">RIA - Kostverdi</span><span class="sxs-lookup"><span data-stu-id="f5988-190">WIP-cost value</span></span>
    - <span data-ttu-id="f5988-191">Kostnad - vare</span><span class="sxs-lookup"><span data-stu-id="f5988-191">Cost-item</span></span>
    - <span data-ttu-id="f5988-192">RIA - kostverdi - vare</span><span class="sxs-lookup"><span data-stu-id="f5988-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="f5988-193">Påløpt tap</span><span class="sxs-lookup"><span data-stu-id="f5988-193">Accrued loss</span></span>
    - <span data-ttu-id="f5988-194">RIA - påløpt tap</span><span class="sxs-lookup"><span data-stu-id="f5988-194">WIP-accrued loss</span></span>

- <span data-ttu-id="f5988-195">Hvilke inntektskontoer brukes til følgende?</span><span class="sxs-lookup"><span data-stu-id="f5988-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="f5988-196">Fakturert omsetning</span><span class="sxs-lookup"><span data-stu-id="f5988-196">Invoiced revenue</span></span>
    - <span data-ttu-id="f5988-197">Påløpte inntekter - salgsverdi</span><span class="sxs-lookup"><span data-stu-id="f5988-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="f5988-198">RIA - Salgsverdi</span><span class="sxs-lookup"><span data-stu-id="f5988-198">WIP-sales value</span></span>
    - <span data-ttu-id="f5988-199">Påløpte inntekter - produksjon</span><span class="sxs-lookup"><span data-stu-id="f5988-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="f5988-200">RIA - Produksjon</span><span class="sxs-lookup"><span data-stu-id="f5988-200">WIP-production</span></span>
    - <span data-ttu-id="f5988-201">Påløpte inntekter - fortjeneste</span><span class="sxs-lookup"><span data-stu-id="f5988-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="f5988-202">RIA - Fortjeneste</span><span class="sxs-lookup"><span data-stu-id="f5988-202">WIP-profit</span></span>
    - <span data-ttu-id="f5988-203">Påløpte inntekter - abonnement</span><span class="sxs-lookup"><span data-stu-id="f5988-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="f5988-204">RIA - abonnement</span><span class="sxs-lookup"><span data-stu-id="f5988-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="f5988-205">Avgifter</span><span class="sxs-lookup"><span data-stu-id="f5988-205">Taxes</span></span>

<span data-ttu-id="f5988-206">For utgiftsrelaterte avgifter må du bestemme hva som inkluderes eller aktivert for reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="f5988-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="f5988-207">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="f5988-207">**Decisions:**</span></span>

- <span data-ttu-id="f5988-208">Er mva inkludert i utgiftsbeløp?</span><span class="sxs-lookup"><span data-stu-id="f5988-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="f5988-209">Skal skatterefusjon aktiveres for utgifter?</span><span class="sxs-lookup"><span data-stu-id="f5988-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="f5988-210">Når du planlegger hovedboken, kan du ikke aktivere skatteutvinning på utgifter hvis du bestemte deg for å søke om amerikansk omsetningsavgift og bruke skatteregler.</span><span class="sxs-lookup"><span data-stu-id="f5988-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="f5988-211">(For å søke om amerikansk omsetningsavgift og skatteregler, angi **Søk om omsetningsavgift**-alternativet til **Ja**.)</span><span class="sxs-lookup"><span data-stu-id="f5988-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="f5988-212">Policyer</span><span class="sxs-lookup"><span data-stu-id="f5988-212">Policies</span></span>

<span data-ttu-id="f5988-213">Ved å opprette regnskapsrapportpolicyer kan du hjelpe organisasjonen med å spare tid og penger når ansatte pådrar seg utgifter på vegne av denne.</span><span class="sxs-lookup"><span data-stu-id="f5988-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="f5988-214">Policyene sikrer at ansatte er på budsjett, gir all nødvendig informasjon, og bruker kun penger etter hvert som de trenger det.</span><span class="sxs-lookup"><span data-stu-id="f5988-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="f5988-215">Du må ta følgende avgjørelser for hver utgiftsrapportpolicy og hver utgiftsrapportgodkjenning du oppretter.</span><span class="sxs-lookup"><span data-stu-id="f5988-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="f5988-216">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="f5988-216">**Decisions:**</span></span>

- <span data-ttu-id="f5988-217">Hva er navnet på policyen?</span><span class="sxs-lookup"><span data-stu-id="f5988-217">What is the name of the policy?</span></span>
- <span data-ttu-id="f5988-218">Hva er utgiftspolicyen for?</span><span class="sxs-lookup"><span data-stu-id="f5988-218">What is the expense policy for?</span></span>
- <span data-ttu-id="f5988-219">Hvis du tidligere har besluttet å aktivere konserninterne utgifter, hvilke firmaer i organisasjonen din vil denne policyen gjelde for?</span><span class="sxs-lookup"><span data-stu-id="f5988-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="f5988-220">Når trer policyen i kraft?</span><span class="sxs-lookup"><span data-stu-id="f5988-220">When does the policy become effective?</span></span>
- <span data-ttu-id="f5988-221">Når utløper policyen?</span><span class="sxs-lookup"><span data-stu-id="f5988-221">When does the policy expire?</span></span>
- <span data-ttu-id="f5988-222">Hva er policyregelen?</span><span class="sxs-lookup"><span data-stu-id="f5988-222">What is the policy rule?</span></span>
- <span data-ttu-id="f5988-223">Hva er resultatet av policyregelen?</span><span class="sxs-lookup"><span data-stu-id="f5988-223">What is the outcome of the policy rule?</span></span>

