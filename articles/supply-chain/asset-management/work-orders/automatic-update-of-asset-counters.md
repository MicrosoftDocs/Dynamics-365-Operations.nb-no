---
title: Automatisk oppdatering av anleggsmiddeltellere
description: Dette emnet beskriver automatisk oppdatering av aktivatellere i Aktivastyring.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9911d5b96bb58b5def3e7dfee0f36826d99f6ba1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263692"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="47a0d-103">Automatisk oppdatering av anleggsmiddeltellere</span><span class="sxs-lookup"><span data-stu-id="47a0d-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="47a0d-104">Hvis du vil ha informasjon om manuell registrering av aktivatellere, se [Manuell oppdatering av aktivatellere](../work-orders/manual-update-of-asset-counters.md)</span><span class="sxs-lookup"><span data-stu-id="47a0d-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="47a0d-105">Hvis du vil ha informasjon om hvordan du definerer aktivatellere, se [Tellere](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="47a0d-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="47a0d-106">Tellerverdier kan også oppdateres automatisk fra produksjonsregistreringer, basert på produksjonstimer eller produksjonsantall (dvs. antallet som produseres).</span><span class="sxs-lookup"><span data-stu-id="47a0d-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="47a0d-107">Denne oppdateringen utføres på siden **Oppdater aktivatellere**.</span><span class="sxs-lookup"><span data-stu-id="47a0d-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="47a0d-108">Du kan oppdatere ett eller flere aktiva ved å angi én parameter, **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="47a0d-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="47a0d-109">Denne parameteren angir startdatoen for produksjonsregistreringer (produksjonstimer eller produksjonsantall).</span><span class="sxs-lookup"><span data-stu-id="47a0d-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="47a0d-110">Den angir med andre ord datoen som tellerverdiene skal oppdateres fra.</span><span class="sxs-lookup"><span data-stu-id="47a0d-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="47a0d-111">Alle aktiva som er relatert til en ressurs *og* som har aktivatellere som er definert til å oppdateres basert på produksjonstimene eller produksjonsantallet, blir inkludert i en automatisk oppdatering.</span><span class="sxs-lookup"><span data-stu-id="47a0d-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="47a0d-112">Nye tellerverdier blir opprettet.</span><span class="sxs-lookup"><span data-stu-id="47a0d-112">New counter values will be created.</span></span>

<span data-ttu-id="47a0d-113">For tellere som er basert på produksjonsantallet, inneholder tellingen både antall korrekte og antall feil som er registrert.</span><span class="sxs-lookup"><span data-stu-id="47a0d-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="47a0d-114">Hvis enheten som brukes til registrering av produsert antall, er forskjellig fra enheten som brukes for telleren, konverteres antallet slik at det samsvarer med tellerenheten.</span><span class="sxs-lookup"><span data-stu-id="47a0d-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="47a0d-115">Som nevnt ovenfor kan automatiske tellere oppdateres fra produksjonsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="47a0d-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="47a0d-116">Derfor må anleggsmiddelet du vil oppdatere tellere automatisk for, være relatert til en ressurs (maskin).</span><span class="sxs-lookup"><span data-stu-id="47a0d-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="47a0d-117">Når produsert antall eller produksjonstimer er registrert på ressursen, kan du oppdatere de tilknyttede anleggsmiddeltellerne.</span><span class="sxs-lookup"><span data-stu-id="47a0d-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="47a0d-118">Velg **Aktivastyring** > **Periodisk** > **Aktiva** > **Oppdater aktivatellere**.</span><span class="sxs-lookup"><span data-stu-id="47a0d-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="47a0d-119">Velg startdatoen for den automatiske oppdateringen i **Fra dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="47a0d-119">In the **From date** field, select the start date of the automatic update.</span></span>

    >[!NOTE]
    ><span data-ttu-id="47a0d-120">Datoen i dette feltet er datoen for arbeid som pågår fra **Rutetransaksjoner** (**Produksjonskontroll** > **Forespørsler og rapporterer** > **Produksjon** > **Rutetransaksjoner** > **Fysisk dato**-feltet).</span><span class="sxs-lookup"><span data-stu-id="47a0d-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="47a0d-121">I hurtigfanen **Poster som skal inkluderes** kan du velge bestemte aktiva, aktivatyper eller ressurser for den automatiske oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="47a0d-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="47a0d-122">Velg **Filter**, og gjør de relevante valgene.</span><span class="sxs-lookup"><span data-stu-id="47a0d-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="47a0d-123">På hurtigfanen **Kjør i bakgrunnen** kan du definere den automatiske oppdateringen som en satsvis jobb, slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="47a0d-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

    <span data-ttu-id="47a0d-124">Illustrasjonen nedenfor viser et eksempel på dialogboksen **Oppdater aktivatellere**.</span><span class="sxs-lookup"><span data-stu-id="47a0d-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

    ![Figur 1](media/12-work-orders.png)

5. <span data-ttu-id="47a0d-126">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="47a0d-126">Select **OK**.</span></span> 

<span data-ttu-id="47a0d-127">Når oppdateringen for den automatiske aktivatelleren er utført, kan du vise tellerregistreringer som er knyttet til aktivumet, på siden **Aktivatellere**.</span><span class="sxs-lookup"><span data-stu-id="47a0d-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="47a0d-128">Velg **Aktivabehandling** > **Felles** > **Aktiva** > **Alle aktiva**, velg aktivumet, gå til handlingsruten, fanen **Aktiva**, gruppen **Foregyggende**, og velg **Tellere**.</span><span class="sxs-lookup"><span data-stu-id="47a0d-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="47a0d-129">På siden **Akkumulert verdi for aktivum** kan du få en oversikt over den siste registreringen som er utført på alle tellertyper på alle aktiva.</span><span class="sxs-lookup"><span data-stu-id="47a0d-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="47a0d-130">Velg **Aktivastyring** > **Forespørsler** > **Aktiva** > **Akkumulert verdi for aktivum**.</span><span class="sxs-lookup"><span data-stu-id="47a0d-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="47a0d-131">Denne siden ligner på siden **Aktivatellere**, men du kan ikke legge til eller redigere registreringer.</span><span class="sxs-lookup"><span data-stu-id="47a0d-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="47a0d-132">Den er bare en oversikt.</span><span class="sxs-lookup"><span data-stu-id="47a0d-132">It's for overview only.</span></span>

<span data-ttu-id="47a0d-133">Illustrasjonen nedenfor viser et eksempel på siden **Akkumulert verdi for aktivum**.</span><span class="sxs-lookup"><span data-stu-id="47a0d-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![Figur 2](media/13-work-orders.png)

<span data-ttu-id="47a0d-135">Merk følgende punkt:</span><span class="sxs-lookup"><span data-stu-id="47a0d-135">Note the following points:</span></span>

- <span data-ttu-id="47a0d-136">Det er fremdeles mulig å opprette manuelle registreringer av tellerverdi for tellertyper som oppdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="47a0d-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="47a0d-137">Se [Manuell oppdatering av anleggsmiddeltellere](../work-orders/manual-update-of-asset-counters.md) hvis du vil ha mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="47a0d-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="47a0d-138">Du kan definere tellere som er relatert til en annen teller.</span><span class="sxs-lookup"><span data-stu-id="47a0d-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="47a0d-139">I dette tilfellet oppdateres tilknyttede tellere automatisk samtidig når en teller oppdateres.</span><span class="sxs-lookup"><span data-stu-id="47a0d-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="47a0d-140">Hvis du vil ha informasjon om hvordan du definerer relaterte tellere, se [Tellere](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="47a0d-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]