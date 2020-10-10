---
title: Feilanalyse av aktivum
description: Dette emnet beskriver feilanalyse for aktiva i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e911f7ca3b67acd9d5a1b170d8c99135da730847
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889152"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="f6ee2-103">Feilanalyse av aktivum</span><span class="sxs-lookup"><span data-stu-id="f6ee2-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f6ee2-104">I Aktivastyring kan du analysere feilregistreringer for anleggsmidler for å få en oversikt over det totale antallet feil som er registrert i en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="f6ee2-105">Feilregistreringer kan analyseres fra ulike perspektiver, for eksempel fokus på aktiva, anleggsmiddeltyper, arbeidssteder, feilsymptomer eller feiltyper.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="f6ee2-106">Klikk **Aktivastyring** > **Forespørsler** > **Aktivumfeil** > **Feilanalyse av aktivum**.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="f6ee2-107">I dialogboksen **Beregning av feilanalyse av aktivum** kan du bruke **Nivå**-feltet til å angi hvor detaljert du vil at anleggsmiddellinjene skal være angående arbeidssteder.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="f6ee2-108">Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle anleggsmiddellinjer for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
        
    <span data-ttu-id="f6ee2-109">Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle anleggsmiddellinjer på alle arbeidsstedsnivået de er relatert til.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="f6ee2-110">Hvis du vil begrense søket, kan du velge bestemte anleggsmidler, feildatoer, feilårsaker og feilløsninger i hurtigfanen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="f6ee2-111">Klikk på **OK** for å starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="f6ee2-112">I kategorien **Feilanalyse av aktivum** klikker du én eller flere **Grupper etter**-knapper for å vise detaljnivået du vil se.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-112">On the **Asset fault analysis** tab, click one or more **Group by** buttons to display the detail level you want to see.</span></span> <span data-ttu-id="f6ee2-113">Aktiverte knapper er uthevet.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="f6ee2-114">Aktiver eller deaktiver en knapp ved å klikke på den.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="f6ee2-115">Klikk **Oppdater beregninger** for å vise valgene dine på skjermen.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="f6ee2-116">Hver gang du aktiverer eller deaktiverer en **Grupper etter** -knapp, må du huske å klikke på **Oppdater beregninger**-knappen.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-116">Every time you activate or deactivate a **Group by** button, remember to click the **Update calculations** button.</span></span> <span data-ttu-id="f6ee2-117">Dette er obligatorisk fordi en stor mengde data behandles når du beregner feilsannsynlighet på nytt.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

## <a name="examples"></a><span data-ttu-id="f6ee2-118">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f6ee2-118">Examples</span></span>

<span data-ttu-id="f6ee2-119">Det er mange måter å analysere feilregistreringer på.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-119">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="f6ee2-120">Denne delen inneholder fem eksempler som viser hvordan ulike datavalg kan gi mer innsikt og detaljer når du analyserer feilregistreringer for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-120">This section has five examples of how different data selections can provide more insight and detail when analyzing asset fault registrations.</span></span>

### <a name="group-by-symptoms"></a><span data-ttu-id="f6ee2-121">Gruppere etter symptomer</span><span class="sxs-lookup"><span data-stu-id="f6ee2-121">Group by symptoms</span></span>

<span data-ttu-id="f6ee2-122">I skjermbildet nedenfor er det bare merket av for **Symptom**-knappen.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-122">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="f6ee2-123">Feilregistreringer er gjort på tre feilsymptomer: "Luftlekkasje", "Sikring er gått" og "Fastkjørt utstyr".</span><span class="sxs-lookup"><span data-stu-id="f6ee2-123">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="f6ee2-124">I kolonnen **Sannsynlighets-%** utgjør alle prosentdeler samlet 100 %.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-124">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="f6ee2-125">Sannsynlighet er basert på alle **Symptom**-registreringer i denne feilanalysen.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-125">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![Figur 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a><span data-ttu-id="f6ee2-127">Gruppere etter symptomer og tidsperiode</span><span class="sxs-lookup"><span data-stu-id="f6ee2-127">Group by symptoms and time period</span></span>

<span data-ttu-id="f6ee2-128">I skjermbildet nedenfor er **År** og **Måned** lagt til for å vise hvordan du kan vise feilregistreringer i en valgt periode.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-128">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="f6ee2-129">Feilsymptomene vises nå som registreringer per år/måned.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-129">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="f6ee2-130">Hvis du legger til alle prosentdeler for hver måned i kolonnen **Sannsynlighets-%**, blir det 100 % til sammen.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-130">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="f6ee2-131">Sannsynlighet er basert på alle **Symptom**-registreringene i denne feilanalysen.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-131">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="f6ee2-132">Hvis du har et stort antall linjer i et anleggsmiddel, men en stor prosentdel vises på en linje, vil dette være en indikasjon på et feilsymptom som bør undersøkes nøyere for å finne en måte å begrense antall registreringer for dette feilsymptomet på.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-132">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Figur 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a><span data-ttu-id="f6ee2-134">Gruppere etter flere symptomer og aktiva</span><span class="sxs-lookup"><span data-stu-id="f6ee2-134">Group by multiple symptoms and assets</span></span>

<span data-ttu-id="f6ee2-135">Kombinasjonen av aktiva og en aktivatype brukes som grunnlag for beregningene som vises i de tre skjermbildene nedenfor, som øker i detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-135">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  

<span data-ttu-id="f6ee2-136">Knappene i handlingsrutegruppene **Grupper etter dato**, **Grupper etter aktiva**, **Grupper etter arbeidssted** samt **Feil**-knappen (feil-ID) inneholder vanligvis perioder eller aktivarelasjoner.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-136">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** Action Pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="f6ee2-137">Knappene **Symptom**, **Område**, **Type**, **Årsak** og **Løsning** er kategoriseringer som brukes i feilbehandling til å analysere registreringer av aktivafeil og finne problemområder.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-137">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="f6ee2-138">**Grupper etter symptom, aktiva og aktivatype**</span><span class="sxs-lookup"><span data-stu-id="f6ee2-138">**Group by symptom, asset, and asset type**</span></span>

<span data-ttu-id="f6ee2-139">I skjermbildet nedenfor ble **Aktiva** og **Aktivatype** lagt til for å gi mer informasjon om feilregistreringer.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-139">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="f6ee2-140">Feilsymptomene er nå delt opp i kombinasjoner av **Aktiva** / **Aktivatype** / **Symptom**.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-140">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="f6ee2-141">Hvis du i kolonnen **Sannsynlighets-%** legger til alle prosentdeler for kombinasjonen av **Aktiva** / **Aktivatype** / **Symptom**, utgjør de 100 % til sammen.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-141">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="f6ee2-142">Sannsynlighet er basert på alle **Symptom**-registreringer i denne feilanalysen.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-142">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="f6ee2-143">Hvis du har et stort antall linjer i et anleggsmiddel, men en stor prosentdel vises på en linje, vil dette være en indikasjon på et feilsymptom som bør undersøkes nøyere for å finne en måte å begrense antall registreringer for dette feilsymptomet på.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-143">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Figur 3](media/08-controlling-and-reporting.png)

<span data-ttu-id="f6ee2-145">**Grupper etter to symptomer, aktiva og aktivatype**</span><span class="sxs-lookup"><span data-stu-id="f6ee2-145">**Group by two symptoms, asset, and asset type**</span></span>

<span data-ttu-id="f6ee2-146">I skjermbildet nedenfor ble **Område** lagt til i **Symptom**, **Aktiva** og **Aktivatype** for å gi mer informasjon om feilregistreringer.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-146">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="f6ee2-147">Hvis du i kolonnen **Sannsynlighets-%** legger til alle prosentdeler for kombinasjonen av **Aktiva** / **Aktivatype** / **Symptom** for et aktivum, utgjør de 100 % til sammen.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="f6ee2-148">Sannsynlighet er basert på kombinasjonen av **Symptom** og **Område** i denne feilanalysen.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-148">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="f6ee2-149">Hvis du har et stort antall linjer i et anleggsmiddel, men en stor prosentdel vises på en linje, vil dette være en indikasjon på et feilområde som bør undersøkes nøyere for å finne en måte å begrense antall registreringer for dette feilområdet på.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![Figur 4](media/09-controlling-and-reporting.png)

<span data-ttu-id="f6ee2-151">**Grupper etter tre symptomer, aktiva og aktivatyper**</span><span class="sxs-lookup"><span data-stu-id="f6ee2-151">**Group by three symptom, asset, and asset type**</span></span>

<span data-ttu-id="f6ee2-152">I skjermbildet nedenfor ble **Type** lagt til, og den mest detaljerte beregningen i dette eksemplet vises.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-152">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="f6ee2-153">Hvis du i kolonnen **Sannsynlighets-%** legger til alle prosentdeler for kombinasjonen av **Aktiva** / **Aktivatype** / **Symptom** for et aktivum, utgjør de 100 % til sammen.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-153">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="f6ee2-154">Sannsynlighet er basert på kombinasjonen av **Symptom**, **Område** og **Type** i denne feilanalysen.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-154">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="f6ee2-155">Hvis du har et stort antall linjer i et anleggsmiddel, men en stor prosentdel vises på en linje, vil dette være en indikasjon på en feiltype som bør undersøkes nøyere for å finne en måte å begrense antall registreringer for denne feiltypen på.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-155">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![Figur 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="f6ee2-157">Hvis du vil ha en oversikt over alle feilregistreringer som er opprettet på arbeidsordrer og vedlikeholdsanmodninger, klikker du **Aktivastyring** > **Forespørsler** > **Aktivumfeil** > **Aktivafeil**.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-157">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="f6ee2-158">På siden **Aktivafeil** velger du en registrering av aktivafeil og utvider ruten **Beslektet informasjon** for å se informasjon om den beslektede arbeidsordren eller vedlikeholdsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="f6ee2-158">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

