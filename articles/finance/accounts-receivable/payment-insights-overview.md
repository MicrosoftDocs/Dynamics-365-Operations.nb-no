---
title: Innsikt i kundebetaling (forhåndsvisning)
description: Dette emnet beskriver innsikt i kundebetaling, som bidrar til å forbedre forståelsen av individuelle kunders vanlige betalingspraksis, og kan identifisere omstendigheter som justerer innkrevingsprosesser tidligere enn det du har gjort ellers.
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
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774018"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="cd738-103">Innsikt i kundebetaling (forhåndsvisning)</span><span class="sxs-lookup"><span data-stu-id="cd738-103">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="cd738-104">Dette emnet beskriver innsikt i kundebetaling, som bidrar til å forbedre forståelsen av individuelle kunders vanlige betalingspraksis, og som kan identifisere omstendigheter som justerer innkrevingsprosesser tidligere enn det du kunne ha gjort ellers.</span><span class="sxs-lookup"><span data-stu-id="cd738-104">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices and that can identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="cd738-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="cd738-105">Overview</span></span>

<span data-ttu-id="cd738-106">For organisasjoner er det ofte vanskelig å forutse når kunder betaler fakturaer.</span><span class="sxs-lookup"><span data-stu-id="cd738-106">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="cd738-107">Denne mangelen på innsikt fører til mindre nøyaktige kontantstrømprognoser, innkrevingsprosesser som starter for sent, og ordrer som blir frigitt til kunder som ikke har utført betalingen.</span><span class="sxs-lookup"><span data-stu-id="cd738-107">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="cd738-108">Kundebetalingsinnsikt (forhåndsvisning) hjelper organisasjoner med å forutse når en kundefaktura skal betales, og hjelper organisasjoner å opprette innkrevingsstrategier som forbedrer sannsynligheten for at betalinger skjer i tide.</span><span class="sxs-lookup"><span data-stu-id="cd738-108">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid, helping organization create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="cd738-109">Prognoser</span><span class="sxs-lookup"><span data-stu-id="cd738-109">Predictions</span></span>

<span data-ttu-id="cd738-110">Betalingsprognoser gjør det mulig for organisasjoner å forbedre forretnings prosessene ved å hjelpe dem til enkelt å identifisere fakturaene som sannsynligvis betales for sent, og for å få riktige tiltak som forbedrer sjansen til å få betalt i tide.</span><span class="sxs-lookup"><span data-stu-id="cd738-110">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="cd738-111">Ved bruk av en maskinlæringsmodell, som benytter historiske fakturaer, betalinger og kundedata, kan kundebetalingsinnsikt (forhåndsvisning) mer nøyaktige forutsi når en kunde vil betale en utestående faktura.</span><span class="sxs-lookup"><span data-stu-id="cd738-111">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="cd738-112">For hver åpne faktura, forutser Kundebetalingsinnsikt (forhåndsvisning) tre sannsynligheter for betaling:</span><span class="sxs-lookup"><span data-stu-id="cd738-112">For each open invoice, Customer payment insights (Preview) predicts three payment probabilities:</span></span>

-   <span data-ttu-id="cd738-113">Sannsynlighet for at betalingen utføres i tide</span><span class="sxs-lookup"><span data-stu-id="cd738-113">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="cd738-114">Sannsynlighet for at betalingen utføres sent</span><span class="sxs-lookup"><span data-stu-id="cd738-114">Probability of payment being made late</span></span>
-   <span data-ttu-id="cd738-115">Sannsynlighet for at betalingen utføres veldig sent</span><span class="sxs-lookup"><span data-stu-id="cd738-115">Probability of payment being made very late</span></span>

<span data-ttu-id="cd738-116">For å hjelpe organisasjoner med å forstå det totale betalingsbeløpet de kan forvente fra en kunde i én av de tre periodene, til rett tid, for sent og veldig sent, gir kundebetalingsinnsikt (forhåndsvisning) også en samlet visning av forventede betalinger.</span><span class="sxs-lookup"><span data-stu-id="cd738-116">To help Organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late, Customer payment insights (Preview) also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="cd738-117">[![Aggregert visning av betalingsprognoser](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="cd738-117">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="cd738-118">Hver faktura blir også tildelt en sannsynlighet for betaling i tide.</span><span class="sxs-lookup"><span data-stu-id="cd738-118">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="cd738-119">Hvis sannsynlighet for betaling til rett tid er mindre enn 50 %, blir fakturaene merket med en rød sirkel for å angi at disse fakturaene kan måtte innkreves.</span><span class="sxs-lookup"><span data-stu-id="cd738-119">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="cd738-120">[![Liste over sannsynligheter for betaling](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="cd738-120">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="cd738-121">Innsikt i kundebetaling (forhåndsvisning) inneholder også kontekstavhengig informasjon som forklarer de viktigste faktorene som påvirket prognosene, den gjeldende forretningsstatusen til kunden og detaljer om den historiske kundebetalingsatferden.</span><span class="sxs-lookup"><span data-stu-id="cd738-121">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="cd738-122">I mange bedrifter har innkrevingsprosessen vært en reaktiv aktivitet, innkrevingsprosessen starter ikke før fakturaer forfaller.</span><span class="sxs-lookup"><span data-stu-id="cd738-122">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="cd738-123">Med Innsikt i kundebetaling (forhåndsvisning) kan organisasjoner bli mer proaktive om innkrevinger.</span><span class="sxs-lookup"><span data-stu-id="cd738-123">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="cd738-124">De trenger ikke lenger å vente på at transaksjonene skal forfalle før start av innkrevingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="cd738-124">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="cd738-125">I stedet kan de bruke betalingsprognosefunksjonen til å fastslå om proaktive innkrevinger vil forbedre sannsynligheten for å bli betalt i tide.</span><span class="sxs-lookup"><span data-stu-id="cd738-125">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="cd738-126">Betalingsforutsigelse gir også virksomheter informasjonen som kreves for å kunne starte innkrevingsprosessen tidlig.</span><span class="sxs-lookup"><span data-stu-id="cd738-126">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="cd738-127">Metodologi</span><span class="sxs-lookup"><span data-stu-id="cd738-127">Methodology</span></span>

<span data-ttu-id="cd738-128">Utvikling og distribusjon av en AI-løsning er vanskelig.</span><span class="sxs-lookup"><span data-stu-id="cd738-128">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="cd738-129">Det krever en gruppe med datateknikere, fageksperter og teknikere som arbeider i lenge på et lengre tidsrom for å formulere, utvikle, distribuere og vedlikeholde en brukbar AI-løsning.</span><span class="sxs-lookup"><span data-stu-id="cd738-129">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy and maintain a usable AI solution.</span></span> <span data-ttu-id="cd738-130">Vi gjør det enkelt å distribuere og bruke AI-løsninger i Finance.</span><span class="sxs-lookup"><span data-stu-id="cd738-130">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="cd738-131">Vi forhåndspakker AI-løsninger i Finance som er bygd på toppen av Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="cd738-131">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="cd738-132">En sluttbruker kan med et enkelt klikk på en knapp distribuere AI-løsningen og begynne å utnytte fordelene med intelligente prognoser.</span><span class="sxs-lookup"><span data-stu-id="cd738-132">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="cd738-133">Hvis en organisasjon ikke er tilfreds med nøyaktigheten i prognosene, kan en privilegert bruker med ett enkelt klikk angi utvidelsesopplevelsen for AI Builder, og deretter merke av for eller fjerne merket for feltene som brukes til å generere prognoser.</span><span class="sxs-lookup"><span data-stu-id="cd738-133">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="cd738-134">Når de er klare, kan de kalibrere og publisere endringene, og den nyutformede modellen blir automatisk plukket opp for prognoser i Finance.</span><span class="sxs-lookup"><span data-stu-id="cd738-134">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="cd738-135">Få tilgang til Kundebetalingsinnsikt (forhåndsvisning)</span><span class="sxs-lookup"><span data-stu-id="cd738-135">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="cd738-136">Hvis du er interessert i å prøve Kundebetalingsinnsikt (forhåndsvisning), kan du sende en e-post til [Innsikt i kundebetaling (forhåndsvisning)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="cd738-136">Please send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="cd738-137">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="cd738-137">Privacy Notice</span></span>

<span data-ttu-id="cd738-138">Forhåndsvisninger (1) kan bruke mindre personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i tjenestenivåavtalen for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.</span><span class="sxs-lookup"><span data-stu-id="cd738-138">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


