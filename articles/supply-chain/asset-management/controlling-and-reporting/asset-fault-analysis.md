---
title: Feilanalyse av aktivum
description: Dette emnet beskriver feilanalyse for aktiva i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c9330cc7b3a8839d94c8945418548033254786b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918447"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="3105a-103">Feilanalyse av aktivum</span><span class="sxs-lookup"><span data-stu-id="3105a-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3105a-104">I Aktivastyring kan du analysere feilregistreringer for anleggsmidler for å få en oversikt over det totale antallet feil som er registrert i en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="3105a-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="3105a-105">Feilregistreringer kan analyseres fra ulike perspektiver, for eksempel fokus på aktiva, anleggsmiddeltyper, arbeidssteder, feilsymptomer eller feiltyper.</span><span class="sxs-lookup"><span data-stu-id="3105a-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="3105a-106">Klikk **Aktivastyring** > **Forespørsler** > **Aktivumfeil** > **Feilanalyse av aktivum**.</span><span class="sxs-lookup"><span data-stu-id="3105a-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="3105a-107">I dialogboksen **Beregning av feilanalyse av aktivum** kan du bruke **Nivå**-feltet til å angi hvor detaljert du vil at anleggsmiddellinjene skal være angående arbeidssteder.</span><span class="sxs-lookup"><span data-stu-id="3105a-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> <span data-ttu-id="3105a-108">Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle anleggsmiddellinjer for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="3105a-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="3105a-109">Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle anleggsmiddellinjer på alle arbeidsstedsnivået de er relatert til.</span><span class="sxs-lookup"><span data-stu-id="3105a-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="3105a-110">Hvis du vil begrense søket, kan du velge bestemte anleggsmidler, feildatoer, feilårsaker og feilløsninger i hurtigfanen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="3105a-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="3105a-111">Klikk på **OK** for å starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="3105a-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="3105a-112">I kategorien **Feilanalyse av aktivum** klikker du én eller flere knapper i handlingsrutegruppene **Grupper etter...** for å vise detaljnivået du vil se.</span><span class="sxs-lookup"><span data-stu-id="3105a-112">On the **Asset fault analysis** tab, click one or more buttons in the **Group by...** action pane groups to display the detail level you want to see.</span></span> <span data-ttu-id="3105a-113">Aktiverte knapper er uthevet.</span><span class="sxs-lookup"><span data-stu-id="3105a-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="3105a-114">Aktiver eller deaktiver en knapp ved å klikke på den.</span><span class="sxs-lookup"><span data-stu-id="3105a-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="3105a-115">Klikk **Oppdater beregninger** for å vise valgene dine på skjermen.</span><span class="sxs-lookup"><span data-stu-id="3105a-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="3105a-116">Hver gang du aktiverer eller deaktiverer knapper i handlingsrutegruppene **Grupper etter...**, må du huske å klikke **Oppdater beregninger**-knappen etter at du har endret valgene.</span><span class="sxs-lookup"><span data-stu-id="3105a-116">Every time you activate or deactivate buttons in the **Group by...** action pane groups, remember to click the **Update calculations** button after you changed the selections.</span></span> <span data-ttu-id="3105a-117">Dette er obligatorisk fordi en stor mengde data behandles når du beregner feilsannsynlighet på nytt.</span><span class="sxs-lookup"><span data-stu-id="3105a-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

<span data-ttu-id="3105a-118">Det er mange måter å analysere feilregistreringer på.</span><span class="sxs-lookup"><span data-stu-id="3105a-118">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="3105a-119">Nedenfor ser du eksempler i fem skjermbilder på hvordan ulike datavalg gir forskjellige typer informasjon.</span><span class="sxs-lookup"><span data-stu-id="3105a-119">Below you see examples in five screenshots of how different data selections provide different pieces of information.</span></span> <span data-ttu-id="3105a-120">Du vil se hvordan forskjellige valg gir mer innsikt og detaljer når du analyserer feilregistreringer for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="3105a-120">You will see how different selections provide more insight and detail when analyzing asset fault registrations.</span></span>

<span data-ttu-id="3105a-121">I skjermbildet nedenfor er det bare merket av for **Symptom**-knappen.</span><span class="sxs-lookup"><span data-stu-id="3105a-121">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="3105a-122">Feilregistreringer er gjort på tre feilsymptomer: "Luftlekkasje", "Sikring er gått" og "Fastkjørt utstyr".</span><span class="sxs-lookup"><span data-stu-id="3105a-122">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="3105a-123">I kolonnen **Sannsynlighets-%** utgjør alle prosentdeler samlet 100 %.</span><span class="sxs-lookup"><span data-stu-id="3105a-123">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="3105a-124">Sannsynlighet er basert på alle **Symptom**-registreringer i denne feilanalysen.</span><span class="sxs-lookup"><span data-stu-id="3105a-124">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![Figur 1](media/06-controlling-and-reporting.png)


<span data-ttu-id="3105a-126">I skjermbildet nedenfor er **År** og **Måned** lagt til for å vise hvordan du kan vise feilregistreringer i en valgt periode.</span><span class="sxs-lookup"><span data-stu-id="3105a-126">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="3105a-127">Feilsymptomene vises nå som registreringer per år/måned.</span><span class="sxs-lookup"><span data-stu-id="3105a-127">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="3105a-128">Hvis du legger til alle prosentdeler for hver måned i kolonnen **Sannsynlighets-%**, blir det 100 % til sammen.</span><span class="sxs-lookup"><span data-stu-id="3105a-128">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="3105a-129">Sannsynlighet er basert på alle **Symptom**-registreringene i denne feilanalysen.</span><span class="sxs-lookup"><span data-stu-id="3105a-129">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="3105a-130">Hvis du har et stort antall linjer i et anleggsmiddel, men en stor prosentdel vises på en linje, vil dette være en indikasjon på et feilsymptom som bør undersøkes nøyere for å finne en måte å begrense antall registreringer for dette feilsymptomet på.</span><span class="sxs-lookup"><span data-stu-id="3105a-130">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Figur 2](media/07-controlling-and-reporting.png)


- <span data-ttu-id="3105a-132">Kombinasjonen av aktiva og en aktivatype brukes som grunnlag for beregningene som vises i de tre skjermbildene nedenfor, som øker i detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="3105a-132">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  
- <span data-ttu-id="3105a-133">Knappene i handlingsrutegruppene **Grupper etter dato**, **Grupper etter aktiva**, **Grupper etter arbeidssted** samt **Feil**-knappen (feil-ID) inneholder vanligvis perioder eller aktivarelasjoner.</span><span class="sxs-lookup"><span data-stu-id="3105a-133">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** action pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="3105a-134">Knappene **Symptom**, **Område**, **Type**, **Årsak** og **Løsning** er kategoriseringer som brukes i feilbehandling til å analysere registreringer av aktivafeil og finne problemområder.</span><span class="sxs-lookup"><span data-stu-id="3105a-134">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="3105a-135">I skjermbildet nedenfor ble **Aktiva** og **Aktivatype** lagt til for å gi mer informasjon om feilregistreringer.</span><span class="sxs-lookup"><span data-stu-id="3105a-135">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="3105a-136">Feilsymptomene er nå delt opp i kombinasjoner av **Aktiva** / **Aktivatype** / **Symptom**.</span><span class="sxs-lookup"><span data-stu-id="3105a-136">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="3105a-137">Hvis du i kolonnen **Sannsynlighets-%** legger til alle prosentdeler for kombinasjonen av **Aktiva** / **Aktivatype** / **Symptom**, utgjør de 100 % til sammen.</span><span class="sxs-lookup"><span data-stu-id="3105a-137">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="3105a-138">Sannsynlighet er basert på alle **Symptom**-registreringer i denne feilanalysen.</span><span class="sxs-lookup"><span data-stu-id="3105a-138">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="3105a-139">Hvis du har et stort antall linjer i et anleggsmiddel, men en stor prosentdel vises på en linje, vil dette være en indikasjon på et feilsymptom som bør undersøkes nøyere for å finne en måte å begrense antall registreringer for dette feilsymptomet på.</span><span class="sxs-lookup"><span data-stu-id="3105a-139">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Figur 3](media/08-controlling-and-reporting.png)


<span data-ttu-id="3105a-141">I skjermbildet nedenfor ble **Område** lagt til i **Symptom**, **Aktiva** og **Aktivatype** for å gi mer informasjon om feilregistreringer.</span><span class="sxs-lookup"><span data-stu-id="3105a-141">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="3105a-142">Hvis du i kolonnen **Sannsynlighets-%** legger til alle prosentdeler for kombinasjonen av **Aktiva** / **Aktivatype** / **Symptom** for et aktivum, utgjør de 100 % til sammen.</span><span class="sxs-lookup"><span data-stu-id="3105a-142">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="3105a-143">Sannsynlighet er basert på kombinasjonen av **Symptom** og **Område** i denne feilanalysen.</span><span class="sxs-lookup"><span data-stu-id="3105a-143">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="3105a-144">Hvis du har et stort antall linjer i et anleggsmiddel, men en stor prosentdel vises på en linje, vil dette være en indikasjon på et feilområde som bør undersøkes nøyere for å finne en måte å begrense antall registreringer for dette feilområdet på.</span><span class="sxs-lookup"><span data-stu-id="3105a-144">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![Figur 4](media/09-controlling-and-reporting.png)


<span data-ttu-id="3105a-146">I skjermbildet nedenfor ble **Type** lagt til, og den mest detaljerte beregningen i dette eksemplet vises.</span><span class="sxs-lookup"><span data-stu-id="3105a-146">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="3105a-147">Hvis du i kolonnen **Sannsynlighets-%** legger til alle prosentdeler for kombinasjonen av **Aktiva** / **Aktivatype** / **Symptom** for et aktivum, utgjør de 100 % til sammen.</span><span class="sxs-lookup"><span data-stu-id="3105a-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="3105a-148">Sannsynlighet er basert på kombinasjonen av **Symptom**, **Område** og **Type** i denne feilanalysen.</span><span class="sxs-lookup"><span data-stu-id="3105a-148">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="3105a-149">Hvis du har et stort antall linjer i et anleggsmiddel, men en stor prosentdel vises på en linje, vil dette være en indikasjon på en feiltype som bør undersøkes nøyere for å finne en måte å begrense antall registreringer for denne feiltypen på.</span><span class="sxs-lookup"><span data-stu-id="3105a-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![Figur 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="3105a-151">Hvis du vil ha en oversikt over alle feilregistreringer som er opprettet på arbeidsordrer og vedlikeholdsanmodninger, klikker du **Aktivastyring** > **Forespørsler** > **Aktivumfeil** > **Aktivafeil**.</span><span class="sxs-lookup"><span data-stu-id="3105a-151">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="3105a-152">På siden **Aktivafeil** velger du en registrering av aktivafeil og utvider ruten **Beslektet informasjon** for å se informasjon om den beslektede arbeidsordren eller vedlikeholdsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="3105a-152">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

