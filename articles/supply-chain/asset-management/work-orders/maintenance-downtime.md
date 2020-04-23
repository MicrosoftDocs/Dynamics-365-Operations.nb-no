---
title: Nedetid ved vedlikehold
description: Dette emnet beskriver nedetid ved vedlikehold i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b4960aea95d63486207699f3bbd7f4b4f3cf0488
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206872"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="1c9d8-103">Nedetid ved vedlikehold</span><span class="sxs-lookup"><span data-stu-id="1c9d8-103">Maintenance downtime</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="1c9d8-104">Du kan opprette registreringer av nedetid ved vedlikehold for aktivaet som er valgt i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="1c9d8-105">Denne funksjonen er nyttig hvis du vil registrere vedlikeholdsnedetid på én eller flere maskiner i produksjonsområdet.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="1c9d8-106">Først oppretter du årsakskodene for vedlikeholdsnedetid du vil bruke, for eksempel **Stopp** og **Planlagt stopp**.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="1c9d8-107">Dette trinnet utføres på siden **Årsakskoder for nedetid ved vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="1c9d8-108">Du kan deretter opprette registreringer for nedetid ved vedlikehold på siden **Nedetid ved vedlikehold** og legge til de aktuelle årsakskodene for nedetiden.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="1c9d8-109">Opprette årsakskoder for nedetid ved vedlikehold</span><span class="sxs-lookup"><span data-stu-id="1c9d8-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="1c9d8-110">Velg **Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Årsakskoder for nedetid ved vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="1c9d8-111">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-111">Select **New**.</span></span>

3. <span data-ttu-id="1c9d8-112">I feltet **Årsakskode for nedetid ved vedlikehold** angir du en ID for årsakskoden nedetid ved vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="1c9d8-113">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="1c9d8-114">Merk av for **KPI inkluder** hvis årsakskoden skal tas med i beregninger av sentrale nøkkelytelsesindikatorer (KPIer) for aktivumet.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="1c9d8-115">Generelt bør ikke planlagte produksjonsstopp tas med i KPI-beregninger fordi de ikke påvirker forventet ytelse.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="1c9d8-116">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-116">Select **Save**.</span></span>

<span data-ttu-id="1c9d8-117">Illustrasjonen nedenfor viser et eksempel på siden **Årsakskoder for nedetid ved vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![Figur 1](media/15-work-orders.png)

<span data-ttu-id="1c9d8-119">Når du har opprettet årsakskodene for vedlikeholdsnedetid som du vil bruke, kan du opprette registreringer for nedetid ved vedlikehold for arbeidsordrer og aktiva.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="1c9d8-120">Opprette registreringer for nedetid ved vedlikehold</span><span class="sxs-lookup"><span data-stu-id="1c9d8-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="1c9d8-121">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="1c9d8-122">Velg arbeidsordren, og deretter går du til kategorien **Arbeidsordre** i gruppen **Aktivum** og velger **Nedetid ved vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="1c9d8-123">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-123">Select **New**.</span></span>

4. <span data-ttu-id="1c9d8-124">Angi dato- og klokkeslettsintervall for registreringen av vedlikeholdsnedetid i **Fra**- og **Til**-feltene.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="1c9d8-125">Når du går ut av **Til**-feltet, settes varigheten i timer automatisk inn i **Varighet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="1c9d8-126">Velg en årsakskode i feltet **Årsakskode for nedetid ved vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="1c9d8-127">Gjenta trinn 3 til og med 5 hvis du vil legge til flere registreringer.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="1c9d8-128">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-128">Select **Save**.</span></span>

<span data-ttu-id="1c9d8-129">Illustrasjonen nedenfor viser et eksempel på en registreringer for nedetid ved vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![Figur 2](media/16-work-orders.png)

<span data-ttu-id="1c9d8-131">Kalenderen som brukes til å beregne en registrering av nedetid ved vedlikehold er avhengig av hva du velger i oppsettet for aktiva og parametere.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="1c9d8-132">Hvis en ressurs er valgt for et aktiva i feltet **Ressurs** i hurtigfanen **Anleggsmiddel** på siden **Alle aktiva**, brukes kalenderoppsettet for den tilknyttede ressursgruppen, som vist i følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![Figur 3](media/17-work-orders.png)

<span data-ttu-id="1c9d8-134">Hvis det ikke er valgt en ressurs for aktivumet, brukes standardkalenderen som er valgt på siden **Aktivabehandlingsparametere**, som vist i følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![Figur 4](media/18-work-orders.png)

<span data-ttu-id="1c9d8-136">Klikk på **Aktivabehandling** > **Forespørsler** > **Nedetid ved vedlikehold** hvis du vil se en oversikt over alle registreringer av vedlikeholdsnedetid.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="1c9d8-137">Alle kalendere som brukes i modulen **Aktivastyring**, defineres i **Organisasjonsstyring** > **Oppsett** > **Kalendere** > **Kalendere**.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

