---
title: Nedetid ved vedlikehold
description: Dette emnet beskriver nedetid ved vedlikehold i Aktivastyring.
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
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918250"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="0b4f0-103">Nedetid ved vedlikehold</span><span class="sxs-lookup"><span data-stu-id="0b4f0-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="0b4f0-104">Du kan opprette registreringer av nedetid ved vedlikehold for aktivaet som er valgt i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="0b4f0-105">Dette er nyttig hvis du vil registrere vedlikeholdsnedetid på én eller flere maskiner i produksjonsområdet.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="0b4f0-106">Først oppretter du årsakskodene for vedlikeholdsnedetid du vil bruke, for eksempel stopp og planlagt stopp.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="0b4f0-107">Dette gjøres i **Årsakskoder for nedetid ved vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="0b4f0-108">Deretter kan du opprette registreringer for nedetid ved vedlikehold, i **Nedetid ved vedlikehold**, og legge til de aktuelle årsakskodene.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="0b4f0-109">Opprette årsakskoder for nedetid ved vedlikehold</span><span class="sxs-lookup"><span data-stu-id="0b4f0-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="0b4f0-110">Klikk på **Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Årsakskoder for nedetid ved vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="0b4f0-111">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-111">Click **New**.</span></span>

3. <span data-ttu-id="0b4f0-112">Sett inn en ID i feltet **Årsakskode for nedetid ved vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="0b4f0-113">Sett inn et navn på årsakskoden i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="0b4f0-114">Merk av for **KPI inkluder** hvis årsakskoden skal tas med i aktiva-KPI-beregninger.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="0b4f0-115">Vanligvis bør ikke planlagte produksjonsstopp tas med i KPI-beregninger fordi de ikke påvirker forventet ytelse.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="0b4f0-116">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-116">Click **Save**.</span></span>

![Figur 1](media/15-work-orders.png)


<span data-ttu-id="0b4f0-118">Når du har opprettet årsakskodene for vedlikeholdsnedetid som du vil bruke, kan du opprette registreringer for nedetid ved vedlikehold for arbeidsordrer og aktiva.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="0b4f0-119">Opprette registreringer for nedetid ved vedlikehold</span><span class="sxs-lookup"><span data-stu-id="0b4f0-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="0b4f0-120">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0b4f0-121">Velg arbeidsordren, og klikk på **Nedetid ved vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="0b4f0-122">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-122">Click **New**.</span></span>

4. <span data-ttu-id="0b4f0-123">Sett inn dato- og klokkeslettsintervall for registreringen av vedlikeholdsnedetid i **Fra**- og **Til**-feltene.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="0b4f0-124">Når du går ut av **Til**-feltet, settes varigheten i timer automatisk inn i **Varighet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="0b4f0-125">Velg en årsakskode i feltet **Årsakskode for nedetid ved vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="0b4f0-126">Gjenta trinn 3-6 hvis du vil legge til flere registreringer.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="0b4f0-127">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-127">Click **Save**.</span></span>


![Figur 2](media/16-work-orders.png)


<span data-ttu-id="0b4f0-129">Kalenderen som brukes til å beregne en registrering av nedetid for vedlikehold er avhengig av hva du velger i oppsettet for aktiva og parametere.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="0b4f0-130">Hvis en ressurs er valgt for et aktiva i **Alle aktiva** > **Anleggsmiddel**-hurtigfanen > **Ressurs**-feltet, brukes kalenderoppsettet for den tilknyttede ressursgruppen, som vist i følgende figur.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![Figur 3](media/17-work-orders.png)


<span data-ttu-id="0b4f0-132">Hvis det ikke er valgt en ressurs for aktivaet, brukes standardkalenderen som er valgt i **Aktivabehandlingsparametere**, som vist i følgende figur.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![Figur 4](media/18-work-orders.png)


<span data-ttu-id="0b4f0-134">Klikk på **Enterprise asset management** > **Forespørsler** > **Nedetid ved vedlikehold** hvis du vil se en oversikt over alle registreringer av vedlikeholdsnedetid.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="0b4f0-135">Alle kalendere som brukes i modulen **Aktivastyring**, defineres i **Organisasjonsstyring** > **Oppsett** > **Kalendere** > **Kalendere**.</span><span class="sxs-lookup"><span data-stu-id="0b4f0-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

