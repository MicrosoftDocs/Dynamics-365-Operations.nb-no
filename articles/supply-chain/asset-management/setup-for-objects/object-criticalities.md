---
title: Type kritisk aktivitet for aktiva
description: Emnet forklarer typer kritsk aktivitet for aktiva i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c6d3742425a3b92282a62c142b9c325e2d7042f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216603"
---
# <a name="asset-criticality-types"></a><span data-ttu-id="2e62c-103">Type kritisk aktivitet for aktiva</span><span class="sxs-lookup"><span data-stu-id="2e62c-103">Asset criticality types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2e62c-104">Emnet forklarer typer kritsk aktivitet for aktiva i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="2e62c-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="2e62c-105">Kritiske forhold omkring aktiva er knyttet til aktiva og overføres til arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="2e62c-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="2e62c-106">Dette kan ikke endres på en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="2e62c-106">It can't be changed on a work order.</span></span> <span data-ttu-id="2e62c-107">Kritiske forhold omkring aktiva brukes til å beregne arbeidsordrekritikalitet under planlegging av arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="2e62c-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="2e62c-108">Det brukes med andre ord til å beregne i hvilken grad en vedlikeholdsjobb på et aktivum påvirker produksjonsplanen og produktiviteten i selskapet.</span><span class="sxs-lookup"><span data-stu-id="2e62c-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="2e62c-109">Hvis du vil ha mer informasjon om oppsettet som er knyttet til beregning av poengsummer for arbeidsordreplanlegging, kan du se [Parametere i Aktivastyring](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2e62c-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="2e62c-110">Hvis du vil definere kritikalitet, må du først opprette kritikalitetstypene som skal brukes i aktivaoppsettet.</span><span class="sxs-lookup"><span data-stu-id="2e62c-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="2e62c-111">Deretter konfigurerer du aktivakritikalitetene.</span><span class="sxs-lookup"><span data-stu-id="2e62c-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="2e62c-112">Definere kritikalitetstyper</span><span class="sxs-lookup"><span data-stu-id="2e62c-112">Set up criticality types</span></span>

1. <span data-ttu-id="2e62c-113">Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Type kritisk aktivitet**.</span><span class="sxs-lookup"><span data-stu-id="2e62c-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="2e62c-114">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="2e62c-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="2e62c-115">I **Kritikalitet**-feltet angir du et tall som angir kritikalitet.</span><span class="sxs-lookup"><span data-stu-id="2e62c-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="2e62c-116">I **Navn**-feltet angir du et navn på kritikalitetstypen.</span><span class="sxs-lookup"><span data-stu-id="2e62c-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="2e62c-117">Angi en faktor i feltet **Faktor**.</span><span class="sxs-lookup"><span data-stu-id="2e62c-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="2e62c-118">Denne faktoren brukes under beregning av arbeidsordreplanlegging for å bestemme kritikalitetsposten som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="2e62c-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="2e62c-119">(Posten som har den høyeste faktoren er alltid brukt.) Denne innstillingen er relevant hvis, som vist i illustrasjonen nedenfor, det opprettes kritikalitetslinjer som har samme kritikalitetsverdi.</span><span class="sxs-lookup"><span data-stu-id="2e62c-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![Siden Type kritisk aktivitet](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="2e62c-121">Definer kritiske forhold omkring aktiva</span><span class="sxs-lookup"><span data-stu-id="2e62c-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="2e62c-122">Velg **Aktivastyring** \> **Oppset** \> **Kritiske forhold omkring aktiva**.</span><span class="sxs-lookup"><span data-stu-id="2e62c-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="2e62c-123">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="2e62c-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="2e62c-124">Avhengig av det påkrevde nivået for aktivakritikalitet kan du foreta relevante valg i feltene **Arbeidssted**, **Aktivatype**, **Produsent**, **Modell**, **Aktivum**, **Jobbtypekategori**, **Jobbtype**, **Jobbtypevariant** og **Jobbehov**.</span><span class="sxs-lookup"><span data-stu-id="2e62c-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2e62c-125">Når en aktivumkritikalitet er valgt, gjennomgår Aktivastyring alle aktivakritikalitetsposter for å kontrollere om det finnes et mulig samsvar.</span><span class="sxs-lookup"><span data-stu-id="2e62c-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="2e62c-126">Den kontrollerer alltid den mest spesifikke kombinasjonen først.</span><span class="sxs-lookup"><span data-stu-id="2e62c-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="2e62c-127">Med andre ord kontrollerer Aktivastyring først **jobbehovet**.</span><span class="sxs-lookup"><span data-stu-id="2e62c-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="2e62c-128">Hvis det ikke blir funnet noen treff, kontrolleres **jobbtypevarianten**.</span><span class="sxs-lookup"><span data-stu-id="2e62c-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="2e62c-129">Hvis det ikke blir funnet noen treff, kontrolleres **jobbtypen** og så videre.</span><span class="sxs-lookup"><span data-stu-id="2e62c-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="2e62c-130">Som du kan se i oppsettet av siden, betyr dette at for å finne den mest spesifikke kombinasjonen, kontrollerer Aktivastyring hver post fra høyre til venstre for et treff.</span><span class="sxs-lookup"><span data-stu-id="2e62c-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="2e62c-131">Hvis det ikke blir funnet noen treff, brukes "standard"-oppføringen som ikke har noen valg.</span><span class="sxs-lookup"><span data-stu-id="2e62c-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="2e62c-132">I **Kritikalitet**-feltet velger du en av de kritikalitetsverdiene du opprettet i forrige fremgangsmåte.</span><span class="sxs-lookup"><span data-stu-id="2e62c-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="2e62c-133">Merknader om kritikalitetsoppsett</span><span class="sxs-lookup"><span data-stu-id="2e62c-133">Notes about criticality setup</span></span>

- <span data-ttu-id="2e62c-134">Hvis du endrer en aktivumkritikalitet i dette oppsettet etter at du allerede har brukt den på en arbeidsordre, oppdateres ikke kritikaliteten i arbeidsordren i henhold til dette.</span><span class="sxs-lookup"><span data-stu-id="2e62c-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="2e62c-135">Kritikaliteten i en arbeidsordre beregnes på nytt hver gang en arbeidsordrelinje legges til eller slettes fra arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="2e62c-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="2e62c-136">Hvis en arbeidsordre inneholder flere arbeidsordrejobber, brukes alltid den høyeste kritikaliteten i henhold til **Faktor**-feltet på siden **Kritikalitetstyper** i arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="2e62c-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="2e62c-137">Vanligvis kan aktivakritikalitet endres over en periode.</span><span class="sxs-lookup"><span data-stu-id="2e62c-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="2e62c-138">Kritikalitet kan påvirkes ved kjøp av nytt utstyr, saneringer, og så videre.</span><span class="sxs-lookup"><span data-stu-id="2e62c-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="2e62c-139">Vurder å reevaluere aktivakritikalitetene med jevne mellomrom (for eksempel én gang per år eller hvert annet år) for å sikre at kritikalitetsdefinisjonene samsvarer med det gjeldende produksjonsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="2e62c-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>
