---
title: Definere leietablåer
description: Dette emnet beskriver informasjonen som vedlikeholdes i leietablåer. Leietablåer inneholder regnskapsretningslinjer som bestemmer hvordan en leieavtale gjøres rede for i systemet.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446594"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="8eb81-104">Definere leietablåer</span><span class="sxs-lookup"><span data-stu-id="8eb81-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8eb81-105">Leietablåer inneholder regnskapsretningslinjer som bestemmer hvordan en leieavtale gjøres rede for i systemet.</span><span class="sxs-lookup"><span data-stu-id="8eb81-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="8eb81-106">I tillegg til kontantprinsippregnskap støtter aktivaleie følgende standarder:</span><span class="sxs-lookup"><span data-stu-id="8eb81-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="8eb81-107">Generally Accepted Accounting Principles i USA (amerikansk GAAP)</span><span class="sxs-lookup"><span data-stu-id="8eb81-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="8eb81-108">Accounting Standards Codification-emne 842 (ASC 842)</span><span class="sxs-lookup"><span data-stu-id="8eb81-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="8eb81-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="8eb81-109">ASC 840</span></span>
- <span data-ttu-id="8eb81-110">International Financial Reporting Standard 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="8eb81-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="8eb81-111">International Accounting Standard 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="8eb81-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="8eb81-112">Hvis du vil opprette et leietablå, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="8eb81-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="8eb81-113">Gå til **Aktivaleie \> Oppsett \> Leietablåer**.</span><span class="sxs-lookup"><span data-stu-id="8eb81-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="8eb81-114">Velg **Ny** for å legge til et tablå.</span><span class="sxs-lookup"><span data-stu-id="8eb81-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="8eb81-115">Angi følgende felt.</span><span class="sxs-lookup"><span data-stu-id="8eb81-115">Set the following fields.</span></span>

    | <span data-ttu-id="8eb81-116">Navn</span><span class="sxs-lookup"><span data-stu-id="8eb81-116">Name</span></span>                                     | <span data-ttu-id="8eb81-117">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8eb81-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="8eb81-118">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="8eb81-118">Posting layer</span></span>                            | <span data-ttu-id="8eb81-119">Velg posteringslaget som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="8eb81-119">Select the posting layer to use.</span></span> <span data-ttu-id="8eb81-120">Hver bok som er knyttet til en leieavtale, defineres for et bestemt posteringslag.</span><span class="sxs-lookup"><span data-stu-id="8eb81-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="8eb81-121">Hvert posteringslag har forskjellige posteringsformål.</span><span class="sxs-lookup"><span data-stu-id="8eb81-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="8eb81-122">Leietype</span><span class="sxs-lookup"><span data-stu-id="8eb81-122">Lease type</span></span>                               | <span data-ttu-id="8eb81-123">Velg om leieavtalen skal klassifiseres automatisk, eller om den skal forhåndsdefineres som finansiell leie eller gjeldende leie.</span><span class="sxs-lookup"><span data-stu-id="8eb81-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="8eb81-124">Regnskapsrammeverk</span><span class="sxs-lookup"><span data-stu-id="8eb81-124">Accounting framework</span></span>                     | <span data-ttu-id="8eb81-125">Velg rammeverket som er tilknyttet tablået.</span><span class="sxs-lookup"><span data-stu-id="8eb81-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="8eb81-126">Konfigurasjon av leieperiode/levetid</span><span class="sxs-lookup"><span data-stu-id="8eb81-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="8eb81-127">Systemet klassifiserer leieavtalen som finansiell leie hvis leietypen er satt til **Automatisk**, og hvis leieperioden for levetiden for aktivaet er større enn eller lik prosentdelen som er angitt i dette feltet.</span><span class="sxs-lookup"><span data-stu-id="8eb81-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="8eb81-128">Konfigurasjon av nåværende verdi / virkelig verdi på aktivum</span><span class="sxs-lookup"><span data-stu-id="8eb81-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="8eb81-129">Angi et helttall for å definere terskelen som skal fastsette leietypen.</span><span class="sxs-lookup"><span data-stu-id="8eb81-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="8eb81-130">Hvis nå-verdien av fremtidige minimumsbetalinger for leie er mer enn den brukerdefinerte verdien fra tablåoppsettet, og hvis tablåets leieklassifisering er satt til automatisk, vil systemet klassifisere leieavtalen som en finansiell leie.</span><span class="sxs-lookup"><span data-stu-id="8eb81-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="8eb81-131">Korttidsterskel</span><span class="sxs-lookup"><span data-stu-id="8eb81-131">Short-term threshold</span></span>                     | <span data-ttu-id="8eb81-132">Angi antall måneder som skal brukes som en terskel for kortsiktige leieavtaler.</span><span class="sxs-lookup"><span data-stu-id="8eb81-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="8eb81-133">Hvis leieperioden er mindre enn eller lik antallet måneder du angir her, vil systemet klassifisere leieavtalen som en kortsiktig leieavtale, og utsatt leie vil bli brukt.</span><span class="sxs-lookup"><span data-stu-id="8eb81-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="8eb81-134">Terskel for lav verdi</span><span class="sxs-lookup"><span data-stu-id="8eb81-134">Low value threshold</span></span>                      | <span data-ttu-id="8eb81-135">Angi et beløp som skal brukes som terskel for lavverdileie.</span><span class="sxs-lookup"><span data-stu-id="8eb81-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="8eb81-136">Hvis virkelig verdi for aktivumet er mindre enn eller lik verdien du angir her, vil systemet klassifisere leieavtalen som en lavverdileie, og utsatt leie vil bli brukt.</span><span class="sxs-lookup"><span data-stu-id="8eb81-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="8eb81-137">Betal til leverandør</span><span class="sxs-lookup"><span data-stu-id="8eb81-137">Pay to vendor</span></span>                            | <span data-ttu-id="8eb81-138">Sett dette alternativet til **Ja** for å tillate at leiebetalinger kan posteres, som en faktura, til leverandørkontoen som er angitt for hver leieavtale.</span><span class="sxs-lookup"><span data-stu-id="8eb81-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="8eb81-139">Når en leiebetaling posteres, vil leverandørkontoen bli kreditert.</span><span class="sxs-lookup"><span data-stu-id="8eb81-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="8eb81-140">Hvis dette alternativet er satt til **Nei**, vil kontoen som er angitt for **Leiebetaling**-posteringstypen på siden **Parametere for leiepostering**, bli kreditert i stedet.</span><span class="sxs-lookup"><span data-stu-id="8eb81-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
