---
title: Kostnads- og datokontroll
description: Dette emnet beskriver kostnads- og datokontroll i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 18373ff16b63ea61a3a4bc38ee7fa0b5e33154b5
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889679"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="33d23-103">Kostnads- og datokontroll</span><span class="sxs-lookup"><span data-stu-id="33d23-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="33d23-104">I Aktivastyring kan du beregne kostnader for å få en oversikt over faktiske kostnader sammenlignet med budsjetterte kostnader for aktiva, arbeidssteder og arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="33d23-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="33d23-105">Faktiske kostnader er basert på posterte transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="33d23-105">Actual costs are based on posted transactions.</span></span> 

<span data-ttu-id="33d23-106">Du kan også foreta en datoberegning hvis du vil sammenligne planlagte start- og sluttdatoer med faktiske start- og sluttdatoer på arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="33d23-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="33d23-107">Kostnadskontroll for aktiva, arbeidssteder og arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="33d23-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="33d23-108">Beregningene for aktiva, arbeidssteder og arbeidsordrer er nesten identiske.</span><span class="sxs-lookup"><span data-stu-id="33d23-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="33d23-109">Den eneste forskjellen er at for anleggsmidler og arbeidssteder kan du også inkludere underordnede aktiva og underordnede arbeidssteder i beregningen.</span><span class="sxs-lookup"><span data-stu-id="33d23-109">The only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="33d23-110">Datoen er transaksjonsdatoen da registreringen ble registrert.</span><span class="sxs-lookup"><span data-stu-id="33d23-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="33d23-111">Klikk på **Aktivastyring** > **Forespørsler** > **Aktiva** > **Kostnadskontroll for aktivum** eller **Kostnadskontroll for arbeidssted**, eller **Aktivastyring** > **Forespørsler** > **Arbeidsordrer** > **Kostnadskontroll for arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="33d23-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="33d23-112">I dialogboksen **Kostnadskontroll for aktivum** / **Kostnadskontroll for arbeidssted** / **Kostnadskontroll for arbeidsordre** velger du en periode som skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="33d23-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a time range to be calculated.</span></span>

3. <span data-ttu-id="33d23-113">Hvis det er nødvendig, velger du et finansdimensjonssett som skal tas med i beregningen.</span><span class="sxs-lookup"><span data-stu-id="33d23-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="33d23-114">Velg "Ja" på veksleknappen **Hopp over null** hvis du ikke vil vise resultater med en nullverdi.</span><span class="sxs-lookup"><span data-stu-id="33d23-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="33d23-115">Du kan bruke **Nivå**-feltet til å angi hvor detaljert kostnadskontrollinjene skal være når det gjelder arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="33d23-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="33d23-116">Hvis du for eksempel setter inn tallet 1 i feltet, og du har et arbeidsstedshierarki med flere nivåer, vises alle kostnadskontrollinjer for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="33d23-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="33d23-117">Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle kostnadskontrollinjene på alle arbeidsstedsnivåene de er relatert til.</span><span class="sxs-lookup"><span data-stu-id="33d23-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="33d23-118">Velg "Ja" på veksleknappen **Vis åpen igangsatt kost** hvis du vil inkludere den aktuelle kolonnen i beregningen.</span><span class="sxs-lookup"><span data-stu-id="33d23-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="33d23-119">Velg Ja på veksleknappen **Inkluder underordnede aktiva** for å vise kostnader knyttet til underordnede aktiva som separate linjer.</span><span class="sxs-lookup"><span data-stu-id="33d23-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="33d23-120">Hvis du vil begrense søket, kan du velge bestemte anleggsmidler/arbeidssteder/arbeidsordrer i hurtigfanen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="33d23-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="33d23-121">Klikk på **OK** for å starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="33d23-121">Click **OK** to start the calculation.</span></span>

    <span data-ttu-id="33d23-122">Figuren nedenfor viser et eksempel på dialogboksen **Kostnadskontroll for aktivum**.</span><span class="sxs-lookup"><span data-stu-id="33d23-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

    ![Dialogboksen Kostnadskontroll for aktivum](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="33d23-124">På siden **Kostnadskontroll for aktivum** klikker du på knappen **Grupper etter** for å vise det nødvendige detaljnivået for beregningen.</span><span class="sxs-lookup"><span data-stu-id="33d23-124">On the **Asset cost control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="33d23-125">De valgte **Grupper etter**-knappen er uthevet.</span><span class="sxs-lookup"><span data-stu-id="33d23-125">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="33d23-126">Klikk på en knapp for å aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="33d23-126">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="33d23-127">Eksempel</span><span class="sxs-lookup"><span data-stu-id="33d23-127">Example</span></span>

<span data-ttu-id="33d23-128">Skjermbildet nedenfor viser et eksempel på beregningsresultater i **Kostnadskontroll for aktivum**.</span><span class="sxs-lookup"><span data-stu-id="33d23-128">The screenshot below shows an example of calculation results in **Asset cost control**.</span></span>

- <span data-ttu-id="33d23-129">Feltet **Opprinnelig budsjett** viser budsjettkostnader fra arbeidsordreprognosen.</span><span class="sxs-lookup"><span data-stu-id="33d23-129">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="33d23-130">Feltet **Igangsatt kost** viser det totale utgiftsbeløpet som en juridisk enhet har avtalt å betale.</span><span class="sxs-lookup"><span data-stu-id="33d23-130">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> 
- <span data-ttu-id="33d23-131">Feltet **Åpen igangsatt kost** viser forpliktelser som skal betales for varer, timer og tjenester du har bestilt eller mottatt, men ennå ikke betalt for.</span><span class="sxs-lookup"><span data-stu-id="33d23-131">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> 
- <span data-ttu-id="33d23-132">Feltet **Faktiske kostnader** viser de relaterte kostnadene etter at alle forbruksregistreringene er postert.</span><span class="sxs-lookup"><span data-stu-id="33d23-132">The **Actual cost** field shows related costs after all consumption registrations have been posted.</span></span>

![Eksempel på beregningsresultater for kostnadskontroll for aktivum](media/02-controlling-and-reporting.png)

<span data-ttu-id="33d23-134">En annen måte å gjøre en kostnadsberegning på er å velge flere aktiva i **Alle aktiva** eller **Aktive aktiva**.</span><span class="sxs-lookup"><span data-stu-id="33d23-134">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="33d23-135">Deretter klikker du **Kostnadskontroll**-knappen i fanen **Generelt**. I dialogboksen **Kostnadskontroll for aktivum** settes de valgte anleggsmidlene automatisk inn i **Aktivum**-feltet i hurtigfanen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="33d23-135">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="33d23-136">Klikk **OK**, så vises den en beregning av kostnadene for de valgte anleggsmidlene.</span><span class="sxs-lookup"><span data-stu-id="33d23-136">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="33d23-137">Den samme fremgangsmåten kan brukes for arbeidssteder i **Alle arbeidssteder** eller **Aktive arbeidssteder**, og for arbeidsordrer i **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="33d23-137">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


## <a name="work-order-date-control"></a><span data-ttu-id="33d23-138">Datokontroll for arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="33d23-138">Work order date control</span></span>

<span data-ttu-id="33d23-139">Bruk denne siden til å få en oversikt over forventede start- og sluttdatoer sammenlignet med faktiske start- og sluttdatoer på arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="33d23-139">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="33d23-140">Klikk **Aktivastyring** > **Forespørsler** > **Arbeidsordrer** > **Datokontroll for arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="33d23-140">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="33d23-141">Klikk **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="33d23-141">Click **Calculate**.</span></span>

3. <span data-ttu-id="33d23-142">Velg et arbeidssted i **Arbeidssted**-feltet.</span><span class="sxs-lookup"><span data-stu-id="33d23-142">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="33d23-143">Sett inn perioden du vil gjøre beregningen for, i feltene **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="33d23-143">Insert the range for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="33d23-144">Alle arbeidsordrer med forventet startdata i perioden, blir inkludert.</span><span class="sxs-lookup"><span data-stu-id="33d23-144">All work orders with expected start date within the range will be included.</span></span>

5. <span data-ttu-id="33d23-145">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="33d23-145">Click **OK**.</span></span>

6. <span data-ttu-id="33d23-146">Klikk på knappene **Grupper etter** for å vise det nødvendige detaljnivået for beregningen.</span><span class="sxs-lookup"><span data-stu-id="33d23-146">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="33d23-147">De valgte **Grupper etter**-knappen er uthevet.</span><span class="sxs-lookup"><span data-stu-id="33d23-147">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="33d23-148">Klikk på en knapp for å aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="33d23-148">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="33d23-149">Eksempel</span><span class="sxs-lookup"><span data-stu-id="33d23-149">Example</span></span>

<span data-ttu-id="33d23-150">Skjermbildet nedenfor viser et eksempel på beregningsresultater i **Datokontroll for arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="33d23-150">The screenshot below shows an example of calculation results in **Work order date control**.</span></span>

- <span data-ttu-id="33d23-151">Feltet **Gj.sn. oppstartsforsinkelse** viser forskjellen i dager mellom planlagt startdato for en arbeidsordre sammenlignet med faktisk startdato.</span><span class="sxs-lookup"><span data-stu-id="33d23-151">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="33d23-152">Hvis for eksempel den faktiske startdatoen var to dager før den planlagte startdatoen, vil -2 vises i dette feltet.</span><span class="sxs-lookup"><span data-stu-id="33d23-152">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="33d23-153">Feltet **Gj.sn. sluttforsinkelse** viser forskjellen i dager mellom planlagt sluttdato for en arbeidsordre sammenlignet med faktisk sluttdato.</span><span class="sxs-lookup"><span data-stu-id="33d23-153">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="33d23-154">Hvis for eksempel den faktiske sluttdatoen var tre dager etter den planlagte sluttdatoen, vil 3 vises i dette feltet.</span><span class="sxs-lookup"><span data-stu-id="33d23-154">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="33d23-155">**Forekomster**-feltene viser antall ganger avvik forekommer i forhold til planlagt og faktisk startdato, og planlagt og faktisk sluttdato i arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="33d23-155">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

![Eksempel på beregningsresultater for Datokontroll for arbeidsordre](media/03-controlling-and-reporting.png)


