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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: b21cf04674d01df31dc3304886e7cda035bdcce2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238262"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="ab8a5-104">Oversikt over inntektsføring</span><span class="sxs-lookup"><span data-stu-id="ab8a5-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab8a5-105">Firmaer i bransjer som selger flere varer, for eksempel produkter, tjenester, abonnementer og så videre, må kunne dele opp ordrer med flere elementer, slik at inntekten kan gjenkjennes på grunnlag av et sett med firmaspesifikke og bransjespesifikke retningslinjer.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-105">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

> [!NOTE]
> <span data-ttu-id="ab8a5-106">Funksjonen Inntektsføring kan ikke aktiveres via Funksjonsbehandling.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-106">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="ab8a5-107">For øyeblikket må du bruke konfigurasjonsnøkler for å aktivere den.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-107">Currently, you must use configuration keys to turn it on.</span></span>

> <span data-ttu-id="ab8a5-108">Inntektsføring, inkludert buntfunksjonalitet, innhold som ikke støttes for bruk i Commerce-kanaler (e-handel, salgssted, telefonsenter).</span><span class="sxs-lookup"><span data-stu-id="ab8a5-108">Revenue recognition, including bundle functionality, isn't supported for use in Commerce channels (e-commerce, POS, call center).</span></span> <span data-ttu-id="ab8a5-109">Varer som konfigureres med inntektsføring, bør ikke legges til i ordrer eller transaksjoner som er opprettet i Commerce-kanaler.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-109">Items configured with revenue recognition should not be added to orders or transactions created in Commerce channels.</span></span>

<span data-ttu-id="ab8a5-110">Generelt kan inntektsføringsprosessen brukes til å utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="ab8a5-110">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="ab8a5-111">Tildele inntekt for å sørge for at den relevante inntektsprisen føres på grunnlag av verdien til komponentene i ordrer med flere elementer.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-111">Allocate revenue, to help ensure that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="ab8a5-112">Utsette inntekt basert på en inntektsplan som representerer den kontraktsmessige tidsrammen og prosentandelene for inntektsføring over tid.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-112">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="ab8a5-113">Videoen [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (vises over) er inkludert i [spillelisten for Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-113">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="ab8a5-114">Funksjonen Inntektsføring gir en fleksibel ramme som lar deg definere firmaspesifikke regler for å gjenkjenne både inntektsprisen og inntektsplanen.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-114">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="ab8a5-115">Frigitte produkter brukes til å støtte inntektsføring på salgsordredokumenter.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-115">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="ab8a5-116">De frigitte produktene inneholder oppsettet som kreves for å bestemme inntektsprisen og inntektsplanen.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-116">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="ab8a5-117">Salgsordren kan stamme fra et Etter regning-prosjekt.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-117">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="ab8a5-118">Firmaer kan bruke funksjonen for inntektsplan uten å bruke funksjonen for inntektspris.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-118">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="ab8a5-119">Derfor brukes prisen på salgsordrelinjene som enten inntekt eller utsatt inntekt.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-119">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="ab8a5-120">Hvis det finnes en inntektsplan på salgsordrelinjen, utsettes prisen på salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-120">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="ab8a5-121">Hvis det ikke finnes en inntektsplan på salgsordrelinjen, posteres prisen på salgsordrelinjen til en inntektskonto når den faktureres.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-121">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="ab8a5-122">Inntektsprisen beregnes enten når salgsordren bekreftes eller når fakturaen posteres.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-122">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="ab8a5-123">Hvis du vil forhåndsvise inntektsprisen før fakturaen posteres, må du bekrefte salgsordren.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-123">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="ab8a5-124">Når salgsordren bekreftes, opprettes det også en forventet inntektsplan hvis noen av salgsordrelinjene har en inntektsplan.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-124">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="ab8a5-125">Når salgsordren faktureres, slettes den forventede inntektsplanen, og den forventede inntektsplanen erstattes med den faktiske inntektsføringsplanen.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-125">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="ab8a5-126">Detaljene for inntektsføringsplanen opprettholdes for hver salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-126">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="ab8a5-127">Den inntektsføringsansvarlige kan vise detaljene og frigi linjer til inntekt når kontraktsforpliktelsen er fullført.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-127">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="ab8a5-128">På slutten av hver periode kan inntektsføringsansvarlig opprette en inntektsjournal for å frigi eventuelle planleggingslinjer som forfaller på eller før en dato vedkommende definerer.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-128">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="ab8a5-129">Denne inntektsjournalen posteres ikke umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-129">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="ab8a5-130">Derfor kan inntektsføringsansvarlig kontrollere at de riktige beløpene frigis fra utsatt inntekt til faktisk inntekt.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-130">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="ab8a5-131">Hvis en kontraktsmessig endring fører til at en ny salgsordrelinje legges til enten i den eksisterende salgsordren eller i en ny salgsordre, kan en prosess for ny tildeling kjøres for å korrigere inntektsprisen på tvers av alle linjene på salgsordrene.</span><span class="sxs-lookup"><span data-stu-id="ab8a5-131">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]