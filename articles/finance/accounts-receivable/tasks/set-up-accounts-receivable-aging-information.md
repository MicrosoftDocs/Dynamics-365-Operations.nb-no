---
title: Definere og generere informasjon om aldersfordeling for kunde
description: Denne veiledningen vil hjelpe deg med å sette opp en definisjon av aldersfordelingsperioden, aldersfordele kundesaldoer og vise saldoer i den aldersfordelte saldolisten og Innkrevinger-siden.
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19b60d5fcfba995d08f12d0548f41a0c3d2781fb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012092"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="7b272-103">Definere og generere informasjon om aldersfordeling for kunde</span><span class="sxs-lookup"><span data-stu-id="7b272-103">Set up and generate accounts receivable aging information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7b272-104">Denne veiledningen vil hjelpe deg med å sette opp en definisjon av aldersfordelingsperioden, aldersfordele kundesaldoer og vise saldoer i den aldersfordelte saldolisten og Innkrevinger-siden.</span><span class="sxs-lookup"><span data-stu-id="7b272-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="7b272-105">Denne registreringen bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="7b272-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="7b272-106">Opprette definisjon av en aldersfordelingsperiode</span><span class="sxs-lookup"><span data-stu-id="7b272-106">Create an aging period definition</span></span>
1. <span data-ttu-id="7b272-107">Gå til **Navigasjonsrute > Moduler > Kreditt og innkreving > Oppsett > Definisjoner av aldersfordelingsperiode**.</span><span class="sxs-lookup"><span data-stu-id="7b272-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Aging period definitions**.</span></span>
2. <span data-ttu-id="7b272-108">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7b272-108">Click **New**.</span></span>
3. <span data-ttu-id="7b272-109">Angi en verdi i feltet **Definisjon av aldersfordelingsperiode**.</span><span class="sxs-lookup"><span data-stu-id="7b272-109">In the **Aging period definition** field, type a value.</span></span>
4. <span data-ttu-id="7b272-110">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7b272-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="7b272-111">Klikk **Legg til nedenfor** for å sette inn en ny aldersfordelingsperiode.</span><span class="sxs-lookup"><span data-stu-id="7b272-111">Click **Add below** to insert a new aging period.</span></span>
6. <span data-ttu-id="7b272-112">Angi beskrivelsen skal vises i rapporter for aldersfordeling, i **Periode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7b272-112">In the **Period** field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="7b272-113">Angi et tall i **Enhet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7b272-113">In the **Unit** field, enter a number.</span></span>
8. <span data-ttu-id="7b272-114">Velg et alternativ i **Intervall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7b272-114">In the **Interval** field, select an option.</span></span> <span data-ttu-id="7b272-115">Finansperiode samsvarer med perioden til finanskalenderen.</span><span class="sxs-lookup"><span data-stu-id="7b272-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="7b272-116">Dag, uke, måned, kvartal og år definerer størrelsen på intervallet etter datotype.</span><span class="sxs-lookup"><span data-stu-id="7b272-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="7b272-117">Ubegrenset velger alle transaksjoner som er før eller etter forrige periode, avhengig av om det er den første eller siste perioden.</span><span class="sxs-lookup"><span data-stu-id="7b272-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="7b272-118">Velg et alternativ i feltet **Indikator for aldersfordeling**.</span><span class="sxs-lookup"><span data-stu-id="7b272-118">In the **Aging indicator** field, select an option.</span></span>
10. <span data-ttu-id="7b272-119">Velg perioden øverst i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="7b272-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="7b272-120">Oppdater beskrivelsen for å beskrive den eldste perioden i definisjonen av aldersfordelingsperiode.</span><span class="sxs-lookup"><span data-stu-id="7b272-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="7b272-121">Angi den nye beskrivelsen for aldersfordelingsperiode i **Periode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7b272-121">In the **Period** field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="7b272-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7b272-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="7b272-123">Aldersfordele saldoere</span><span class="sxs-lookup"><span data-stu-id="7b272-123">Age the balances</span></span>
1. <span data-ttu-id="7b272-124">Gå til **Kreditt og innkreving > Periodiske oppgaver > Aldersfordel kundesaldoer**.</span><span class="sxs-lookup"><span data-stu-id="7b272-124">Go to **Credit and collections > Periodic tasks > Age customer balances**.</span></span>
2. <span data-ttu-id="7b272-125">Velg definisjonen av aldersfordelingsperiode som du opprettet, i feltet **Definisjon av aldersfordelingsperiode**.</span><span class="sxs-lookup"><span data-stu-id="7b272-125">In the **Aging period definition** field, select the aging period definition that you created.</span></span>
    + <span data-ttu-id="7b272-126">Du kan ha ett aktivt øyeblikksbilde for hver definisjon av aldersfordelingsperiode.</span><span class="sxs-lookup"><span data-stu-id="7b272-126">You can have one active snapshot for each aging period definition.</span></span>  
    + <span data-ttu-id="7b272-127">Alle kunder behandles som standard.</span><span class="sxs-lookup"><span data-stu-id="7b272-127">All customers are processed by default.</span></span> <span data-ttu-id="7b272-128">Du kan bruke dette valget til å beregne en enkelt samlingspulje med kunder.</span><span class="sxs-lookup"><span data-stu-id="7b272-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    + <span data-ttu-id="7b272-129">Velg datoen fra transaksjonen som du vil bruke for aldersfordeling.</span><span class="sxs-lookup"><span data-stu-id="7b272-129">Select the date from the transaction that you will use for the aging.</span></span>  
    + <span data-ttu-id="7b272-130">Velg en "per"-dato for aldersfordeling.</span><span class="sxs-lookup"><span data-stu-id="7b272-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="7b272-131">Standarden er i dag, men hvis du endrer dette feltet til Valgt dato, vil du kunne velge den ønskede datoen.</span><span class="sxs-lookup"><span data-stu-id="7b272-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="7b272-132">For satsvis behandling kan du bruke dagens dato.</span><span class="sxs-lookup"><span data-stu-id="7b272-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="7b272-133">Utvid **Firma**-området.</span><span class="sxs-lookup"><span data-stu-id="7b272-133">Expand the **Company** range.</span></span> <span data-ttu-id="7b272-134">Du kan velge firmaene som skal inkluderes i det statiske utvalget.</span><span class="sxs-lookup"><span data-stu-id="7b272-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="7b272-135">Det gjeldende selskapet er valgt som standard.</span><span class="sxs-lookup"><span data-stu-id="7b272-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="7b272-136">Klikk **OK** for å behandle øyeblikksbildet.</span><span class="sxs-lookup"><span data-stu-id="7b272-136">Click **Ok** to process the snapshot.</span></span> <span data-ttu-id="7b272-137">Det vil ta litt tid, så vent til glidebryteren forsvinner og kontroller meldingssentret for en melding.</span><span class="sxs-lookup"><span data-stu-id="7b272-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="7b272-138">Se på saldoene på listen over aldersfordelte saldoer og på innkrevingssiden</span><span class="sxs-lookup"><span data-stu-id="7b272-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="7b272-139">Gå til **Kreditt og innkreving > Innkrevinger > Aldersfordelte saldoer**.</span><span class="sxs-lookup"><span data-stu-id="7b272-139">Go to **Credit and collections > Collections > Aged balances**.</span></span> <span data-ttu-id="7b272-140">Listesiden viser saldoene for kunden.</span><span class="sxs-lookup"><span data-stu-id="7b272-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="7b272-141">Aldersfordelingsikonet viser aldersfordelingsperioden for den eldste transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="7b272-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="7b272-142">Velg en kunde med en saldo.</span><span class="sxs-lookup"><span data-stu-id="7b272-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="7b272-143">Vis faktaboksområdet **Aldersfordeling** for å vise de aldersfordelte saldoene.</span><span class="sxs-lookup"><span data-stu-id="7b272-143">Expand the **Aging fact** box area to view the aged balances.</span></span> <span data-ttu-id="7b272-144">Definisjonen av aldersfordelingsperiode for faktaboksen hentes fra standarddefinisjonen av aldersfordelingsperiode angitt i parameterne.</span><span class="sxs-lookup"><span data-stu-id="7b272-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="7b272-145">Du kan endre den ved hjelp av Samle inn-menyen.</span><span class="sxs-lookup"><span data-stu-id="7b272-145">You can change it using the Collect menu.</span></span>  

