---
title: Innsikt i kundebetaling (forhåndsvisning)
description: Dette emnet beskriver funksjonene for betalingsinnsikt som hjelper deg med å forstå de vanlige betalingspraksisene til en kunde. Funksjonen kan også hjelpe til med å identifisere omstendigheter som fører til at du starter innkrevingsprosesser tidligere enn du ellers ville starte dem.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 21516cb7ef6e95dcef27638ddb72520f492958a5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207333"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="14daf-104">Innsikt i kundebetaling (forhåndsvisning)</span><span class="sxs-lookup"><span data-stu-id="14daf-104">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="14daf-105">Dette emnet beskriver funksjonene for betalingsinnsikt som hjelper deg med å forstå de vanlige betalingspraksisene til en kunde.</span><span class="sxs-lookup"><span data-stu-id="14daf-105">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices.</span></span> <span data-ttu-id="14daf-106">Funksjonen kan også hjelpe til med å identifisere omstendigheter som fører til at du starter innkrevingsprosesser tidligere enn du ellers ville starte dem.</span><span class="sxs-lookup"><span data-stu-id="14daf-106">The feature can help you identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="14daf-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="14daf-107">Overview</span></span>

<span data-ttu-id="14daf-108">Det kan være vanskelig å forutse når kunder betaler fakturaer.</span><span class="sxs-lookup"><span data-stu-id="14daf-108">It can be hard to predict when customers will pay their invoices.</span></span> <span data-ttu-id="14daf-109">Denne mangelen på innsikt fører til mindre nøyaktige kontantstrømprognoser, innkrevingsprosesser som starter for sent, og ordrer som blir frigitt til kunder som ikke har utført betalingen.</span><span class="sxs-lookup"><span data-stu-id="14daf-109">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="14daf-110">Kundebetalingsinnsikt (forhåndsversjon) hjelper organisasjoner med å forutse når en kundefaktura skal betales.</span><span class="sxs-lookup"><span data-stu-id="14daf-110">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="14daf-111">Denne informasjonen kan hjelpe organisasjoner med å opprette strategier for innsamling som forbedrer sannsynligheten for betaling i tide.</span><span class="sxs-lookup"><span data-stu-id="14daf-111">This information can help organizations create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="14daf-112">Prognoser</span><span class="sxs-lookup"><span data-stu-id="14daf-112">Predictions</span></span>

<span data-ttu-id="14daf-113">Betalingsprognoser gjør det mulig for organisasjoner å forbedre forretnings prosessene ved å hjelpe dem til enkelt å identifisere fakturaene som sannsynligvis betales for sent, og for å få riktige tiltak som forbedrer sjansen til å få betalt i tide.</span><span class="sxs-lookup"><span data-stu-id="14daf-113">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="14daf-114">Ved bruk av en maskinlæringsmodell, som benytter historiske fakturaer, betalinger og kundedata, kan kundebetalingsinnsikt (forhåndsvisning) mer nøyaktige forutsi når en kunde vil betale en utestående faktura.</span><span class="sxs-lookup"><span data-stu-id="14daf-114">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="14daf-115">For hver åpne faktura kan Kundebetalingsinnsikt (forhåndsvisning) predikere tre sannsynligheter for betaling:</span><span class="sxs-lookup"><span data-stu-id="14daf-115">For each open invoice, Customer payment insights (Preview) can predict three payment probabilities:</span></span>

-   <span data-ttu-id="14daf-116">Sannsynlighet for at betalingen utføres i tide</span><span class="sxs-lookup"><span data-stu-id="14daf-116">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="14daf-117">Sannsynlighet for at betalingen utføres sent</span><span class="sxs-lookup"><span data-stu-id="14daf-117">Probability of payment being made late</span></span>
-   <span data-ttu-id="14daf-118">Sannsynlighet for at betalingen utføres veldig sent</span><span class="sxs-lookup"><span data-stu-id="14daf-118">Probability of payment being made very late</span></span>

<span data-ttu-id="14daf-119">For å hjelpe organisasjoner med å forstå det totale betalingsbeløpet de kan forvente fra en kunde i én av de tre periodene, til rett tid, for sent og veldig sent, gir Kundebetalingsinnsikt (forhåndsvisning) også en samlet visning av forventede betalinger.</span><span class="sxs-lookup"><span data-stu-id="14daf-119">Customer payment insights (Preview) also provides an aggregated view of expected payments, which can help organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late.</span></span>

<span data-ttu-id="14daf-120">[![Aggregert visning av betalingsprognoser](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="14daf-120">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="14daf-121">Hver faktura blir også tildelt en sannsynlighet for betaling i tide.</span><span class="sxs-lookup"><span data-stu-id="14daf-121">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="14daf-122">Hvis sannsynlighet for betaling til rett tid er mindre enn 50 %, blir fakturaene merket med en rød sirkel for å angi at disse fakturaene kan måtte innkreves.</span><span class="sxs-lookup"><span data-stu-id="14daf-122">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="14daf-123">[![Liste over sannsynligheter for betaling](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="14daf-123">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="14daf-124">Innsikt i kundebetaling (forhåndsvisning) inneholder også kontekstavhengig informasjon som forklarer de viktigste faktorene som påvirket prognosene, den gjeldende forretningsstatusen til kunden og detaljer om den historiske kundebetalingsatferden.</span><span class="sxs-lookup"><span data-stu-id="14daf-124">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="14daf-125">I mange bedrifter har innkrevingsprosessen vært en reaktiv aktivitet, innkrevingsprosessen starter ikke før fakturaer forfaller.</span><span class="sxs-lookup"><span data-stu-id="14daf-125">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="14daf-126">Med Innsikt i kundebetaling (forhåndsvisning) kan organisasjoner bli mer proaktive om innkrevinger.</span><span class="sxs-lookup"><span data-stu-id="14daf-126">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="14daf-127">De trenger ikke lenger å vente på at transaksjonene skal forfalle før start av innkrevingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="14daf-127">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="14daf-128">I stedet kan de bruke betalingsprognosefunksjonen til å fastslå om proaktive innkrevinger vil forbedre sannsynligheten for å bli betalt i tide.</span><span class="sxs-lookup"><span data-stu-id="14daf-128">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="14daf-129">Betalingsforutsigelse gir også virksomheter informasjonen som kreves for å kunne starte innkrevingsprosessen tidlig.</span><span class="sxs-lookup"><span data-stu-id="14daf-129">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="14daf-130">Metodologi</span><span class="sxs-lookup"><span data-stu-id="14daf-130">Methodology</span></span>

<span data-ttu-id="14daf-131">Utvikling og distribusjon av en AI-løsning er vanskelig.</span><span class="sxs-lookup"><span data-stu-id="14daf-131">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="14daf-132">Det krever en gruppe med datateknikere, fageksperter og teknikere som arbeider i lenge på et lengre tidsrom for å formulere, utvikle, distribuere og vedlikeholde en brukbar AI-løsning.</span><span class="sxs-lookup"><span data-stu-id="14daf-132">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="14daf-133">Vi gjør det enkelt å distribuere og bruke AI-løsninger i Finance.</span><span class="sxs-lookup"><span data-stu-id="14daf-133">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="14daf-134">Vi forhåndspakker AI-løsninger i Finance som er bygd på toppen av Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="14daf-134">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="14daf-135">En sluttbruker kan med et enkelt klikk på en knapp distribuere AI-løsningen og begynne å utnytte fordelene med intelligente prognoser.</span><span class="sxs-lookup"><span data-stu-id="14daf-135">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="14daf-136">Hvis en organisasjon ikke er tilfreds med nøyaktigheten i prognosene, kan en privilegert bruker med ett enkelt klikk angi utvidelsesopplevelsen for AI Builder, og deretter merke av for eller fjerne merket for feltene som brukes til å generere prognoser.</span><span class="sxs-lookup"><span data-stu-id="14daf-136">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="14daf-137">Når de er klare, kan de kalibrere og publisere endringene, og den nyutformede modellen blir automatisk plukket opp for prognoser i Finance.</span><span class="sxs-lookup"><span data-stu-id="14daf-137">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="14daf-138">Få tilgang til Kundebetalingsinnsikt (forhåndsvisning)</span><span class="sxs-lookup"><span data-stu-id="14daf-138">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="14daf-139">Hvis du er interessert i å prøve Kundebetalingsinnsikt (forhåndsvisning), kan du sende en e-post til [Innsikt i kundebetaling (forhåndsvisning)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="14daf-139">Send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="14daf-140">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="14daf-140">Privacy Notice</span></span>

<span data-ttu-id="14daf-141">Forhåndsvisninger (1) kan bruke mindre personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i tjenestenivåavtalen for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.</span><span class="sxs-lookup"><span data-stu-id="14daf-141">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]