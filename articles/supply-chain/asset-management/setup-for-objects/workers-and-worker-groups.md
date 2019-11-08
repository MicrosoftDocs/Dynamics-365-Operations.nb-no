---
title: Vedlikeholdsarbeidere og arbeidsgrupper
description: Dette emnet forklarer vedlikeholdspersoner og arbeidergrupper i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0a8fcf26da02bd42f6ee45687c585091e3b945e
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570984"
---
# <a name="maintenance-workers-and-worker-groups"></a><span data-ttu-id="57885-103">Vedlikeholdsarbeidere og arbeidsgrupper</span><span class="sxs-lookup"><span data-stu-id="57885-103">Maintenance workers and worker groups</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="57885-104">Dette emnet forklarer vedlikeholdspersoner og arbeidergrupper i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="57885-104">This topic explains maintenance workers and worker groups in Asset Management.</span></span> <span data-ttu-id="57885-105">I Aktivastyring kan du koble vedlikeholdspersoner arbeidere til arbeidssteder.</span><span class="sxs-lookup"><span data-stu-id="57885-105">In Asset Management, you can connect maintenance workers to functional locations.</span></span> <span data-ttu-id="57885-106">(Hvis du vil ha mer informasjon om arbeidssteder, se [Opprette arbeidssteder](../functional-locations/create-functional-locations.md).) Denne funksjonaliteten kan være nyttig hvis du for eksempel planlegger en vedlikeholdsjobb på en maskin som er plassert på arbeidssted 01, og du vil tilordne vedlikeholdspersoner fra samme sted til å utføre jobben.</span><span class="sxs-lookup"><span data-stu-id="57885-106">(For more information about functional locations, see [Create functional locations](../functional-locations/create-functional-locations.md).) This functionality might be useful if, for example, you're scheduling a maintenance job on a machine that is located in functional location 01, and you want to allocate maintenance workers from the same location to perform the job.</span></span>

<span data-ttu-id="57885-107">Du kan også opprette vedlikeholdspersongrupper og knytte vedlikeholdspersoner til dem.</span><span class="sxs-lookup"><span data-stu-id="57885-107">You can also create maintenance worker groups and associate maintenance workers with them.</span></span> <span data-ttu-id="57885-108">Denne funksjonaliteten er nyttig når du utfører enkel ordreplanlegging, og du vil planlegge en gruppe med vedlikeholdspersoner i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="57885-108">This functionality is useful when you do simple work order scheduling, and you want to schedule a group of maintenance workers on a work order.</span></span> <span data-ttu-id="57885-109">Du kan bruke vedlikeholdspersoner og vedlikeholdspersongrupper til å definere foretrukne vedlikeholdspersoner og ansvarlige for vedlikeholdspersoner.</span><span class="sxs-lookup"><span data-stu-id="57885-109">You can use maintenance workers and maintenance worker groups to set up preferred maintenance workers and responsible maintenance workers.</span></span> 


## <a name="create-workers"></a><span data-ttu-id="57885-110">Opprett arbeidere</span><span class="sxs-lookup"><span data-stu-id="57885-110">Create workers</span></span>

1. <span data-ttu-id="57885-111">Velg **Aktivastyring** \> **Oppsett** \> **Arbeidere** \> **Arbeidere**.</span><span class="sxs-lookup"><span data-stu-id="57885-111">Select **Asset management** \> **Setup** \> **Workers** \> **Workers**.</span></span>
2. <span data-ttu-id="57885-112">Velg **Ny** for å legge til en ny arbeider i listen.</span><span class="sxs-lookup"><span data-stu-id="57885-112">Select **New** to add a worker to the list.</span></span>
3. <span data-ttu-id="57885-113">Velg arbeideren i **Arbeider**-feltet.</span><span class="sxs-lookup"><span data-stu-id="57885-113">In the **Worker** field, select the worker.</span></span>
4. <span data-ttu-id="57885-114">Sett **Aktiv**-alternativet til **Ja** for å planlegge arbeideren på arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="57885-114">Set the **Active** option to **Yes** to schedule the worker on work orders.</span></span>

    <span data-ttu-id="57885-115">I hurtigfanen **Generelt** fylles feltene **Ressurs** og **Beskrivelse** ut automatisk hvis en ressurs er valgt for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="57885-115">On the **General** FastTab, the **Resource** and **Description** fields are automatically filled in if a resource has been selected for the worker.</span></span> <span data-ttu-id="57885-116">**Kalender**-feltet fylles også automatisk ut, forutsatt at du har definert arbeideren som en ressurs og tildelt en kalender til ressursen på **Ressurser**-siden (**Organisasjonsadministrasjon** \> **Ressurser** \> **Ressurser**).</span><span class="sxs-lookup"><span data-stu-id="57885-116">The **Calendar** field is also automatically filled in, provided that you've set up the worker as a resource and allocated a calendar to that resource on the **Resources** page (**Organization administration** \> **Resources** \> **Resources**).</span></span>

5. <span data-ttu-id="57885-117">På hurtigfanen **Grupper** velger du **Legg til**, og velg deretter en vedlikeholdspersongruppe for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="57885-117">On the **Groups** FastTab, select **Add**, and then select a maintenance worker group for the worker.</span></span> <span data-ttu-id="57885-118">En arbeider kan knyttes til flere enn én gruppe.</span><span class="sxs-lookup"><span data-stu-id="57885-118">A worker can be affiliated with more than one group.</span></span>
6. <span data-ttu-id="57885-119">I standardoppsettet er en arbeiders tilknytning til en gruppe gyldig fra datoen når du legger til gruppen, og den utløper aldri.</span><span class="sxs-lookup"><span data-stu-id="57885-119">In the standard setup, a worker's affiliation with a group is effective from the date when you add the group, and it never expires.</span></span> <span data-ttu-id="57885-120">Denne datoen vises i **Gyldighet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="57885-120">This date is shown in the **Effective** field.</span></span> <span data-ttu-id="57885-121">Hvis du vil se **Gyldighet**-feltet, velger du **Vis** \> **Alle**.</span><span class="sxs-lookup"><span data-stu-id="57885-121">To see the **Effective** field, select **View** \> **All**.</span></span> <span data-ttu-id="57885-122">Hvis arbeiderens tilknytning til en gruppe, skal være begrenset til en bestemt periode, bruker du feltene **Gyldighet** og **Utløp** felt til å definere perioden.</span><span class="sxs-lookup"><span data-stu-id="57885-122">If the worker's affiliation with a group should be limited to a specific period, use the **Effective** and **Expiration** fields to define the period.</span></span>
7. <span data-ttu-id="57885-123">På hurtigfanen **Arbeidssteder** velger du **Legg til**, og velg deretter et arbeidssted for vedlikeholdspersonen.</span><span class="sxs-lookup"><span data-stu-id="57885-123">On the **Functional locations** FastTab, select **Add**, and then select a functional location for the maintenance worker.</span></span> <span data-ttu-id="57885-124">Angi også hvilket sted som er det primære arbeidsstedet for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="57885-124">Also specify which location is the primary functional location for the worker.</span></span>

    > [!NOTE]
    > <span data-ttu-id="57885-125">Når du legger til arbeidssteder for en arbeider, vises alle aktive aktiva som er relatert til arbeidsstedene, på ulike menyelementer, for eksempel **Mine aktiva aktiva** og **Mine aktive arbeidssteder**.</span><span class="sxs-lookup"><span data-stu-id="57885-125">When you add functional locations to a worker, all active assets that are related to those functional locations appear on various menu items, such as **My active assets** and **My active functional locations**.</span></span> <span data-ttu-id="57885-126">De vises også i aktivaoppslagene som vises når du oppretter et nytt aktivum, en vedlikeholdsanmodning eller en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="57885-126">They also appear in the asset lookups that are shown when you create a new asset, maintenance request, or work order.</span></span>

    <span data-ttu-id="57885-127">Feltene på hurtigfanen **Detaljer** viser antall vedlikeholdspersongrupper og arbeidssteder som den valgte vedlikeholdspersonen er relatert til.</span><span class="sxs-lookup"><span data-stu-id="57885-127">The fields on the **Details** FastTab show the number of maintenance worker groups and functional locations that the selected maintenance worker is related to.</span></span>

## <a name="create-worker-groups"></a><span data-ttu-id="57885-128">Opprett arbeidergrupper</span><span class="sxs-lookup"><span data-stu-id="57885-128">Create worker groups</span></span>

1. <span data-ttu-id="57885-129">Velg **Aktivastyring** \> **Oppsett** \> **Arbeidere** \> **Vedlikeholdsarbeidergrupper**.</span><span class="sxs-lookup"><span data-stu-id="57885-129">Select **Asset management** \> **Setup** \> **Workers** \> **Maintenance worker groups**.</span></span>
2. <span data-ttu-id="57885-130">Velg **Ny** for å legge til en ny arbeidergruppe i listen.</span><span class="sxs-lookup"><span data-stu-id="57885-130">Select **New** to add a worker group to the list.</span></span>
3. <span data-ttu-id="57885-131">Angi en gruppe-ID i feltet **Vedlikeholdspersongruppe**.</span><span class="sxs-lookup"><span data-stu-id="57885-131">In the **Maintenance worker group** field, enter a group ID.</span></span>
4. <span data-ttu-id="57885-132">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="57885-132">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="57885-133">På hurtigfanen **Arbeidere** velger du **Legg til**, og velg deretter en vedlikeholdsperson for arbeidergruppen.</span><span class="sxs-lookup"><span data-stu-id="57885-133">On the **Workers** FastTab, select **Add**, and then select a maintenance worker for the worker group.</span></span> <span data-ttu-id="57885-134">Hvis du vil ha informasjon om feltene **Gyldighet** og **Utløp**, kan du se trinn 6 i forrige fremgangsmåte.</span><span class="sxs-lookup"><span data-stu-id="57885-134">For information about the **Effective** and **Expiration** fields, see step 6 in the previous procedure.</span></span>
6. <span data-ttu-id="57885-135">Hvis en ressursgruppe skal knyttes til den valgte vedlikeholdspersongruppen, velger du **Kopier fra ressursgruppe**.</span><span class="sxs-lookup"><span data-stu-id="57885-135">If a resource group should be related to the selected maintenance worker group, select **Copy from resource group**.</span></span> <span data-ttu-id="57885-136">I **Gruppe**-feltet velger du ressursgruppen du vil kopiere kalenderinnstillinger fra.</span><span class="sxs-lookup"><span data-stu-id="57885-136">In the **Group** field, select the resource group to copy calendar settings from.</span></span> <span data-ttu-id="57885-137">I feltet **Arbeidsgruppe** velger du arbeidergruppen du vil kopiere kalenderinnstillingene for ressursgruppen til.</span><span class="sxs-lookup"><span data-stu-id="57885-137">Then, in the **Worker group** field, select the worker group to copy the resource group's calendar settings to.</span></span> <span data-ttu-id="57885-138">Dette trinnet er bare relevant hvis du vil at vedlikeholdspersoner skal bruke kalenderen som er relatert til en ressurs (arbeidssenter) under arbeidsordreplanlegging.</span><span class="sxs-lookup"><span data-stu-id="57885-138">This step is relevant only if you want maintenance workers to use the calendar that is related to a resource (work center) during work order scheduling.</span></span>

    <span data-ttu-id="57885-139">Feltet på hurtigfanen **Detaljer** viser antall vedlikeholdspersoner som er definert for den valgte vedlikeholdspersongruppen.</span><span class="sxs-lookup"><span data-stu-id="57885-139">The field on the **Details** FastTab shows the number of maintenance workers that have been set up on the selected maintenance worker group.</span></span>
