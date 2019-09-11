---
title: Automatisk oppdatering av anleggsmiddeltellere
description: Dette emnet beskriver automatisk oppdatering av aktivatellere i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875826"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="69ecc-103">Automatisk oppdatering av anleggsmiddeltellere</span><span class="sxs-lookup"><span data-stu-id="69ecc-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="69ecc-104">I den forrige delen beskrives manuell registrering av anleggsmiddeltellere.</span><span class="sxs-lookup"><span data-stu-id="69ecc-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="69ecc-105">Oppsett av anleggsmiddeltellere beskrives i [Tellere](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="69ecc-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="69ecc-106">Tellerverdier kan også oppdateres automatisk fra produksjonsregistreringer, basert på produksjonstimer eller produksjonsantall.</span><span class="sxs-lookup"><span data-stu-id="69ecc-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="69ecc-107">Dette gjøres i **Oppdater anleggsmiddeltellere**.</span><span class="sxs-lookup"><span data-stu-id="69ecc-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="69ecc-108">Du kan oppdatere ett eller flere anleggsmidler ved å sette inn én parameter, **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="69ecc-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="69ecc-109">Denne parameteren angir startdatoen for produksjonsregistreringer (timer eller produsert antall), som betyr startdatoen som tellerverdier skal oppdateres fra.</span><span class="sxs-lookup"><span data-stu-id="69ecc-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="69ecc-110">Alle aktiva som er relatert til en ressurs *og* og har anleggsmiddeltellere, som er definert til å oppdateres basert på produsert antall eller produksjonstimer, blir inkludert i en automatisk oppdatering, og nye tellerverdier blir opprettet.</span><span class="sxs-lookup"><span data-stu-id="69ecc-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="69ecc-111">Når det gjelder tellere basert på produksjonsantall, blir både korrekt antall og feil antall registrert i tellingen.</span><span class="sxs-lookup"><span data-stu-id="69ecc-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="69ecc-112">Hvis enheten som brukes til registrering av produsert antall, er forskjellig fra enheten som brukes på telleren, konverteres antallet for å samsvare med tellerenheten.</span><span class="sxs-lookup"><span data-stu-id="69ecc-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="69ecc-113">Som nevnt ovenfor kan automatiske tellere oppdateres fra produksjonsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="69ecc-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="69ecc-114">Derfor må anleggsmiddelet du vil oppdatere tellere automatisk for, være relatert til en ressurs (maskin).</span><span class="sxs-lookup"><span data-stu-id="69ecc-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="69ecc-115">Beskrivelsene nedenfor gir en oversikt over oppsett og behandling av produksjonsordrer (i modulen for **produksjonskontroll**), som brukes som et grunnlag for automatisk oppdatering av tellere for et anleggsmiddel i modulen **Aktivastyring**.</span><span class="sxs-lookup"><span data-stu-id="69ecc-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="69ecc-116">Når produsert antall eller produksjonstimer er registrert på ressursen, kan du oppdatere de tilknyttede anleggsmiddeltellerne.</span><span class="sxs-lookup"><span data-stu-id="69ecc-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="69ecc-117">Klikk på **Aktivastyring** > **Periodisk** > **Aktiva** > **Oppdater anleggsmiddeltellere**.</span><span class="sxs-lookup"><span data-stu-id="69ecc-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="69ecc-118">Velg startdatoen for den automatiske oppdateringen i **Fra dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="69ecc-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="69ecc-119">Datoen i dette feltet er datoen for arbeid som pågår fra **Rutetransaksjoner** (**Produksjonskontroll** > **Forespørsler og rapporterer** > **Produksjon** > **Rutetransaksjoner** > **Fysisk dato**-feltet).</span><span class="sxs-lookup"><span data-stu-id="69ecc-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="69ecc-120">Hvis du vil velge bestemte aktiva, aktivatyper eller ressurser for den automatisk oppdateringen, klikker du på **Filter** i hurtigfanen **Poster som skal inkluderes**, og gjør de aktuelle valgene.</span><span class="sxs-lookup"><span data-stu-id="69ecc-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="69ecc-121">På hurtigfanen **Kjør i bakgrunnen** kan du definere den automatiske oppdateringen som en satsvis jobb, om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="69ecc-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![Figur 1](media/12-work-orders.png)

5. <span data-ttu-id="69ecc-123">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="69ecc-123">Click **OK**.</span></span> <span data-ttu-id="69ecc-124">Når den automatiske oppdateringen av anleggsmiddelteller er utført, kan du se tellerregistreringene som er knyttet til aktivumet i **Aktivatetellere** (**Aktivastyring** > **Felles** > **Aktiva** > **Alle aktiva** > velg aktivum **Tellere** -knappen).</span><span class="sxs-lookup"><span data-stu-id="69ecc-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="69ecc-125">I **Aktivateller totalt** kan du få en oversikt over den siste registreringen utført på alle tellertyper på alle anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="69ecc-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="69ecc-126">Klikk **Aktivastyring** > **Forespørsler** > **Aktiva** > **Akkumulert verdi for aktivum**.</span><span class="sxs-lookup"><span data-stu-id="69ecc-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="69ecc-127">Visningen ligner veldig **Aktivatellere**, men du kan ikke legge til eller redigere registreringer i **Akkumulert verdi for aktivum**.</span><span class="sxs-lookup"><span data-stu-id="69ecc-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="69ecc-128">Den gjelder bare for oversikt.</span><span class="sxs-lookup"><span data-stu-id="69ecc-128">It is for overview only.</span></span>

![Figur 2](media/13-work-orders.png)


- <span data-ttu-id="69ecc-130">Det er fremdeles mulig å opprette manuelle registreringer av tellerverdi for tellertyper som oppdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="69ecc-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="69ecc-131">Se delen "Manuell oppdatering av anleggsmiddeltellere" hvis du vil ha mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="69ecc-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="69ecc-132">Du kan definere tellere relatert til en annen teller, som betyr at når en teller oppdateres, oppdateres relaterte tellere automatisk samtidig.</span><span class="sxs-lookup"><span data-stu-id="69ecc-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="69ecc-133">Se emnet [Tellere](../setup-for-objects/counters.md) om oppsett av relaterte tellere.</span><span class="sxs-lookup"><span data-stu-id="69ecc-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
