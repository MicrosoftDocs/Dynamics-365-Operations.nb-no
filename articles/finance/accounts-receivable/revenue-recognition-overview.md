---
title: Oversikt over inntektsføring
description: Dette emnet inneholder informasjon om funksjonen Inntektsføring. Funksjonen gir en fleksibel ramme som lar deg definere firmaspesifikke regler for å gjenkjenne både inntektsprisen og inntektsplanen for ordrer med flere elementer.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 92af567499c1a8a23cd4d51e5bab48eaab2d8422
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2020
ms.locfileid: "4459668"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="b058c-104">Oversikt over inntektsføring</span><span class="sxs-lookup"><span data-stu-id="b058c-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="b058c-105">Funksjonen Inntektsføring kan ikke aktiveres via Funksjonsbehandling.</span><span class="sxs-lookup"><span data-stu-id="b058c-105">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="b058c-106">For øyeblikket må du bruke konfigurasjonsnøkler for å aktivere den.</span><span class="sxs-lookup"><span data-stu-id="b058c-106">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="b058c-107">Firmaer i bransjer som selger flere varer, for eksempel produkter, tjenester, abonnementer og så videre, må kunne dele opp ordrer med flere elementer, slik at inntekten kan gjenkjennes på grunnlag av et sett med firmaspesifikke og bransjespesifikke retningslinjer.</span><span class="sxs-lookup"><span data-stu-id="b058c-107">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

<span data-ttu-id="b058c-108">Generelt kan inntektsføringsprosessen brukes til å utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="b058c-108">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="b058c-109">Tildele inntekt for å sikre at den relevante inntektsprisen føres på grunnlag av verdien til komponentene i ordrer med flere elementer.</span><span class="sxs-lookup"><span data-stu-id="b058c-109">Allocate revenue, to help guarantee that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="b058c-110">Utsette inntekt basert på en inntektsplan som representerer den kontraktsmessige tidsrammen og prosentandelene for inntektsføring over tid.</span><span class="sxs-lookup"><span data-stu-id="b058c-110">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="b058c-111">Videoen [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (vises over) er inkludert i [spillelisten for Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.</span><span class="sxs-lookup"><span data-stu-id="b058c-111">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="b058c-112">Funksjonen Inntektsføring gir en fleksibel ramme som lar deg definere firmaspesifikke regler for å gjenkjenne både inntektsprisen og inntektsplanen.</span><span class="sxs-lookup"><span data-stu-id="b058c-112">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="b058c-113">Frigitte produkter brukes til å støtte inntektsføring på salgsordredokumenter.</span><span class="sxs-lookup"><span data-stu-id="b058c-113">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="b058c-114">De frigitte produktene inneholder oppsettet som kreves for å bestemme inntektsprisen og inntektsplanen.</span><span class="sxs-lookup"><span data-stu-id="b058c-114">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="b058c-115">Salgsordren kan stamme fra et Etter regning-prosjekt.</span><span class="sxs-lookup"><span data-stu-id="b058c-115">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="b058c-116">Firmaer kan bruke funksjonen for inntektsplan uten å bruke funksjonen for inntektspris.</span><span class="sxs-lookup"><span data-stu-id="b058c-116">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="b058c-117">Derfor brukes prisen på salgsordrelinjene som enten inntekt eller utsatt inntekt.</span><span class="sxs-lookup"><span data-stu-id="b058c-117">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="b058c-118">Hvis det finnes en inntektsplan på salgsordrelinjen, utsettes prisen på salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="b058c-118">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="b058c-119">Hvis det ikke finnes en inntektsplan på salgsordrelinjen, posteres prisen på salgsordrelinjen til en inntektskonto når den faktureres.</span><span class="sxs-lookup"><span data-stu-id="b058c-119">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="b058c-120">Inntektsprisen beregnes enten når salgsordren bekreftes eller når fakturaen posteres.</span><span class="sxs-lookup"><span data-stu-id="b058c-120">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="b058c-121">Hvis du vil forhåndsvise inntektsprisen før fakturaen posteres, må du bekrefte salgsordren.</span><span class="sxs-lookup"><span data-stu-id="b058c-121">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="b058c-122">Når salgsordren bekreftes, opprettes det også en forventet inntektsplan hvis noen av salgsordrelinjene har en inntektsplan.</span><span class="sxs-lookup"><span data-stu-id="b058c-122">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="b058c-123">Når salgsordren faktureres, slettes den forventede inntektsplanen, og den forventede inntektsplanen erstattes med den faktiske inntektsføringsplanen.</span><span class="sxs-lookup"><span data-stu-id="b058c-123">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="b058c-124">Detaljene for inntektsføringsplanen opprettholdes for hver salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="b058c-124">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="b058c-125">Den inntektsføringsansvarlige kan vise detaljene og frigi linjer til inntekt når kontraktsforpliktelsen er fullført.</span><span class="sxs-lookup"><span data-stu-id="b058c-125">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="b058c-126">På slutten av hver periode kan inntektsføringsansvarlig opprette en inntektsjournal for å frigi eventuelle planleggingslinjer som forfaller på eller før en dato vedkommende definerer.</span><span class="sxs-lookup"><span data-stu-id="b058c-126">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="b058c-127">Denne inntektsjournalen posteres ikke umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="b058c-127">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="b058c-128">Derfor kan inntektsføringsansvarlig kontrollere at de riktige beløpene frigis fra utsatt inntekt til faktisk inntekt.</span><span class="sxs-lookup"><span data-stu-id="b058c-128">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="b058c-129">Hvis en kontraktsmessig endring fører til at en ny salgsordrelinje legges til enten i den eksisterende salgsordren eller i en ny salgsordre, kan en prosess for ny tildeling kjøres for å korrigere inntektsprisen på tvers av alle linjene på salgsordrene.</span><span class="sxs-lookup"><span data-stu-id="b058c-129">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
