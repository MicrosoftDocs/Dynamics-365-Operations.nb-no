---
title: Kundebetalingsinnsikt (forhåndsvisning)
description: Dette emnet beskriver hvordan kundebetalingsinnsikt kan bidra til å forutse når en faktura skal betales, og hjelpe organisasjoner å opprette optimaliseringsstrategier som forbedrer sannsynligheten for at betalinger skjer i tide.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "344668"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="74d34-103">Kundebetalingsinnsikt (forhåndsvisning)</span><span class="sxs-lookup"><span data-stu-id="74d34-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="74d34-104">Denne funksjonen er en del av en bestemt versjon, og den er bare tilgjengelig for brukere som har valgt privat forhåndsvisning.</span><span class="sxs-lookup"><span data-stu-id="74d34-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="74d34-105">Denne funksjonen vil inkluderes i en kommende versjon som blir generelt tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="74d34-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="74d34-106">Oversikt</span><span class="sxs-lookup"><span data-stu-id="74d34-106">Overview</span></span>

<span data-ttu-id="74d34-107">For organisasjoner er det ofte vanskelig å forutse når en kunde betaler fakturaer.</span><span class="sxs-lookup"><span data-stu-id="74d34-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="74d34-108">Denne mangelen på innsikt kan føre til unøyaktige kontantstrømprognoser, tidkrevende innkrevingsprosesser og mulighet for at ordrer frigis til kunder som kan utgjøre en kredittrisiko.</span><span class="sxs-lookup"><span data-stu-id="74d34-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="74d34-109">Kundebetalingsinnsikt (forhåndsvisning) bruker maskinlæring til å forutse når en faktura blir betalt.</span><span class="sxs-lookup"><span data-stu-id="74d34-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="74d34-110">I tillegg gir den optimaliseringsstrategier som kan skreddersys for å øke sannsynligheten for at kunder betaler innen fristen.</span><span class="sxs-lookup"><span data-stu-id="74d34-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="74d34-111">Prognoser</span><span class="sxs-lookup"><span data-stu-id="74d34-111">Predictions</span></span>

<span data-ttu-id="74d34-112">Betalingsprognoser gjor det mulig for organisasjoner å forbedre forretningsprosessene sine ved å:</span><span class="sxs-lookup"><span data-stu-id="74d34-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="74d34-113">Lett å identifisere fakturaer som sannsynligvis blir betalte for seint.</span><span class="sxs-lookup"><span data-stu-id="74d34-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="74d34-114">Ta nødvendige forholdsregler for å forbedre sjansen for å få betaling i tide.</span><span class="sxs-lookup"><span data-stu-id="74d34-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="74d34-115">Kundebetalingsinnsikt (forhåndsvisning) bruker maskinlæring til å forutse når en faktura blir betalt.</span><span class="sxs-lookup"><span data-stu-id="74d34-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="74d34-116">Den bruker historisk faktura, betaling og kundedata for å opprette en maskinlæringsmodell som brukes til å forutse når en faktura skal betales.</span><span class="sxs-lookup"><span data-stu-id="74d34-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="74d34-117">For hver åpne faktura, forutser Kundebetalingsinnsikt (forhåndsvisning) tre sannsynligheter for betaling:</span><span class="sxs-lookup"><span data-stu-id="74d34-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="74d34-118">Sannsynlighet for at betalingen blir gjort til rett tid (innen fakturaens forfallsdato).</span><span class="sxs-lookup"><span data-stu-id="74d34-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="74d34-119">Sannsynlighet for at betalingen blir gjort innen 30 dager for fakturaens forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="74d34-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="74d34-120">Sannsynlighet for at betalingen blir gjort etter 30 dager for fakturaens forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="74d34-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="74d34-121">Sannsynligheten for betalinger vises i prognosedelen.</span><span class="sxs-lookup"><span data-stu-id="74d34-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="74d34-122">[![Betalingsprognoser](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="74d34-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="74d34-123">Hver faktura er også tilordnet en vinnende sannsynlighet for betaling som bruker én av de tre sannsynlige betalingscenarioene som er definert ovenfor.</span><span class="sxs-lookup"><span data-stu-id="74d34-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="74d34-124">Scenariet med størst sannsynlighet for betaling, er det vinnende scenariet.</span><span class="sxs-lookup"><span data-stu-id="74d34-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="74d34-125">La oss for eksempel anta at det for en faktura er en prognose som viser en 71 prosent sannsynlighet for at fakturaen betales innen tidsfristen, 13 prosent sannsynlighet for at fakturaen betales innen 30 dager etter forfallsdatoen, og 16 prosent sannsynlighet for at fakturaen betales etter 30 dager etter forfallsdatoen.</span><span class="sxs-lookup"><span data-stu-id="74d34-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="74d34-126">Den høyeste sannsynligheten viser at fakturaen vil bli betalt innen tidsfristen, så fakturaen merkes med sannsynlighet for betaling innen tidsfristen.</span><span class="sxs-lookup"><span data-stu-id="74d34-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="74d34-127">[![Betalingsprognoser](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="74d34-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="74d34-128">Strategier for optimalisering</span><span class="sxs-lookup"><span data-stu-id="74d34-128">Optimization strategies</span></span>

<span data-ttu-id="74d34-129">I tillegg til betalingsprognoser kan Kundebetalingsinnsikt (forhåndsvisning) bruke optimaliseringsstrategier til å forbedre sjansene for å få betalt i tide.</span><span class="sxs-lookup"><span data-stu-id="74d34-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="74d34-130">Dette gjør det mulig for organisasjoner å foreta "Hva skjer hvis"-analyse ved å tillate brukere å justere faktura- og kundeparametere, og deretter sammenligne den tilhørende innvirkningen på sannsynligheten for å motta fakturabetalinger i tide.</span><span class="sxs-lookup"><span data-stu-id="74d34-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="74d34-131">En organisasjon ønsker for eksempel kanskje å evaluere virkningen av å oppdatere kontantrabatten på fakturaer med sannsynlighet for å motta betalingen til rett tid.</span><span class="sxs-lookup"><span data-stu-id="74d34-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="74d34-132">Når fakturaene er optimalisert til å bruke den nye rabatten, kan brukerne se effekten av å bruke rabatten på sannsynligheten for å motta betalinger for disse fakturaene innen tidsfristen.</span><span class="sxs-lookup"><span data-stu-id="74d34-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="74d34-133">Hvis kostnaden av å bruke rabatten er minimal sammenlignet med fordelen med å fp betaling innen tidsfristen, kan organisasjonen velge å bruke den valgte rabatten på alle fremtidige åpne ordrer.</span><span class="sxs-lookup"><span data-stu-id="74d34-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="74d34-134">For øyeblikket er bare rabatt tilgjengelig som optimaliseringsstrategi for Kundebetalingsinnsikt (forhåndsvisning).</span><span class="sxs-lookup"><span data-stu-id="74d34-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="74d34-135">[![Optimaliserte prognoser](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="74d34-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="74d34-136">Få tilgang til Kundebetalingsinnsikt (forhåndsvisning)</span><span class="sxs-lookup"><span data-stu-id="74d34-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="74d34-137">Hvis du er interessert i å prøve Kundebetalingsinnsikt (forhåndsvisning), kan du sende en e-post til [teamet for forhåndsvisning av økonomisk innsikt](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="74d34-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="74d34-138">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="74d34-138">Privacy Statement</span></span>

<span data-ttu-id="74d34-139">Forhåndsvisninger lagrer kundedata i USA.</span><span class="sxs-lookup"><span data-stu-id="74d34-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="74d34-140">I tillegg (1) kan forhåndsvisninger bruke mindre personvern og færre sikkerhetstiltak enn Dynamics 365 for Finance and Operations-tjenesten, (2) er forhåndsvisninger ikke inkludert i tjenestenivåavtalen for denne tjenesten, (3) må forhåndsvisninger ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) forhåndsvisninger har begrenset støtte.</span><span class="sxs-lookup"><span data-stu-id="74d34-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>
