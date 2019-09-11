---
title: Definer foretrukne vedlikeholdspersoner
description: Dette emnet forklarer hvordan du definerer foretrukne vedlikeholdspersoner i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887417"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="7e9de-103">Foretrukne vedlikeholdspersoner</span><span class="sxs-lookup"><span data-stu-id="7e9de-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="7e9de-104">Du kan angi hvilke vedlikeholdspersoner som foretrekkes til å fullføre arbeidsordrer under planlegging av arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="7e9de-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="7e9de-105">Bruk av denne funksjonaliteten er valgfri, men den kan hjelpe deg med å velge vedlikeholdspersonen som er mest kvalifisert for å fullføre en jobb, basert på arbeiderkompetanse.</span><span class="sxs-lookup"><span data-stu-id="7e9de-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="7e9de-106">I planleggingen av arbeidsordrer blir derfor oppsettet i **Foretrukne vedlikeholdspersoner** brukt til å avgjøre om en bestemt vedlikeholdsperson eller arbeidsgruppe skal planlegges for en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="7e9de-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="7e9de-107">Bare vedlikeholdspersoner som er tilgjengelige på planleggingstidspunktet, vil bli planlagt.</span><span class="sxs-lookup"><span data-stu-id="7e9de-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="7e9de-108">Hvis et oppsett av foretrukken vedlikeholdsperson samsvarer med en arbeidsordre under planlegging, men vedlikeholdspersonen er tilordnet andre jobber, blir arbeidsordren planlagt til en annen, tilgjengelig vedlikeholdsperson.</span><span class="sxs-lookup"><span data-stu-id="7e9de-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="7e9de-109">Før du kan definere foretrukne vedlikeholdsarbeidere, må du først definere vedlikeholdsarbeidere og vedlikeholdsarbeidergrupper som skal være tilgjengelige for valg.</span><span class="sxs-lookup"><span data-stu-id="7e9de-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="7e9de-110">Se [Vedlikeholdspersoner og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md) hvis du vil ha en beskrivelse av hvordan du definerer vedlikeholdspersoner og arbeidsgrupper.</span><span class="sxs-lookup"><span data-stu-id="7e9de-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="7e9de-111">Definere foretrukne arbeidere</span><span class="sxs-lookup"><span data-stu-id="7e9de-111">Set up preferred workers</span></span>

<span data-ttu-id="7e9de-112">En foretrukket vedlikeholdsperson eller arbeidsgruppe kan knyttes til en bestemt</span><span class="sxs-lookup"><span data-stu-id="7e9de-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="7e9de-113">handel</span><span class="sxs-lookup"><span data-stu-id="7e9de-113">trade</span></span>  
- <span data-ttu-id="7e9de-114">variant av vedlikeholdsjobbtype</span><span class="sxs-lookup"><span data-stu-id="7e9de-114">maintenance job type variant</span></span>  
- <span data-ttu-id="7e9de-115">type vedlikeholdsjobb</span><span class="sxs-lookup"><span data-stu-id="7e9de-115">maintenance job type</span></span>  
- <span data-ttu-id="7e9de-116">kategori for type vedlikeholdsjobb</span><span class="sxs-lookup"><span data-stu-id="7e9de-116">maintenance job type category</span></span>  
- <span data-ttu-id="7e9de-117">eiendeler</span><span class="sxs-lookup"><span data-stu-id="7e9de-117">asset</span></span>  
- <span data-ttu-id="7e9de-118">aktivumtype</span><span class="sxs-lookup"><span data-stu-id="7e9de-118">asset type</span></span>  

<span data-ttu-id="7e9de-119">eller en kombinasjon av disse valgene.</span><span class="sxs-lookup"><span data-stu-id="7e9de-119">or a combination of those selections.</span></span> <span data-ttu-id="7e9de-120">Jo flere valg du gjør for den samme posten, jo mer spesifikt blir oppsettet.</span><span class="sxs-lookup"><span data-stu-id="7e9de-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="7e9de-121">Klikk på **Aktivastyring** > **Oppsett** > **Arbeidere** > **Foretrukne vedlikeholdspersoner**.</span><span class="sxs-lookup"><span data-stu-id="7e9de-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="7e9de-122">Klikk **Ny** for å opprette en ny post.</span><span class="sxs-lookup"><span data-stu-id="7e9de-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="7e9de-123">Start ved å opprette et standardoppsett for vedlikeholdspersoner eller arbeidsgruppe som ikke har noen valg i feltene som vises i punktlisten ovenfor.</span><span class="sxs-lookup"><span data-stu-id="7e9de-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="7e9de-124">Dette betyr at du bare gjør et valg i feltet **Foretrukket vedlikeholdspersongruppe** eller feltet **Foretrukket vedlikeholdsperson**.</span><span class="sxs-lookup"><span data-stu-id="7e9de-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="7e9de-125">I figuren nedenfor ser du et eksempel i den første posten der "Forespørsler" er valgt som foretrukket vedlikeholdspersongruppe.</span><span class="sxs-lookup"><span data-stu-id="7e9de-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="7e9de-126">Standardoppsettet vil bli brukt ved arbeidsordreplanlegging hvis ingen annen, mer spesifikk kombinasjon samsvarer med innholdet i arbeidsordren under arbeidsordreplanleggingen.</span><span class="sxs-lookup"><span data-stu-id="7e9de-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="7e9de-127">Gjenta trinn 2 for å opprette en ny post.</span><span class="sxs-lookup"><span data-stu-id="7e9de-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="7e9de-128">Gjør de nødvendige valgene, avhengig av detaljnivået for den foretrukne arbeideren eller arbeidsgruppen.</span><span class="sxs-lookup"><span data-stu-id="7e9de-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="7e9de-129">*Eksempel:* I figuren nedenfor i den sjette posten er vedlikeholdsarbeideren Shawn Richardson valgt som foretrukket arbeider.</span><span class="sxs-lookup"><span data-stu-id="7e9de-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="7e9de-130">Han velges automatisk under planlegging av en arbeidsordre som inneholder aktivaet "CH-BP1-03-02" og vedlikeholdsjobbtypen "Fasilitetsvurdering" hvis han er tilgjengelig på det planlagte tidspunktet.</span><span class="sxs-lookup"><span data-stu-id="7e9de-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="7e9de-131">Når en foretrukket vedlikeholdsarbeider velges under planlegging av arbeidsordre, går vanligvis Aktivastyring gjennom alle **Foretrukne vedlikeholdspersoner**-postene for å se etter et mulig treff, og kontrollerer alltid den mest spesifikke kombinasjonen først.</span><span class="sxs-lookup"><span data-stu-id="7e9de-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="7e9de-132">Hvis det ikke blir funnet noe treff, brukes standardposten med et valg i enten feltet **Foretrukket vedlikeholdsarbeidsgruppe** eller feltet **Foretrukket vedlikeholdsperson**.</span><span class="sxs-lookup"><span data-stu-id="7e9de-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![Figur 1](media/02-work-order-scheduling.png)

<span data-ttu-id="7e9de-134">Du kan også definere ansvarlige vedlikeholdspersoner som kan velges når en vedlikeholdsforespørsel eller arbeidsordre opprettes.</span><span class="sxs-lookup"><span data-stu-id="7e9de-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="7e9de-135">I **Alle arbeidsordrer** og **Alle vedlikeholdsforespørsler** kan du redigere valget hvis det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="7e9de-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="7e9de-136">Se [Ansvarlige vedlikeholdsarbeidere](../setup-for-maintenance-requests/responsible-workers.md) for å få mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="7e9de-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="7e9de-137">Under planleggingen av arbeidsordrer beregnes ulike poeng for å bestemme hvilke arbeidere som skal fullføre jobbene for en arbeidsordre (disse resultatene defineres i **Aktivabehandlingsparametere** > **Planlegging av arbeidsordre**-koblingen).</span><span class="sxs-lookup"><span data-stu-id="7e9de-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="7e9de-138">Hvis to eller flere foretrukne vedlikeholdsarbeidere eller ansvarlige vedlikeholdsarbeidere får samme resultat under planleggingen av arbeidsordre, blir én arbeider tilfeldig valgt.</span><span class="sxs-lookup"><span data-stu-id="7e9de-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="7e9de-139">Ellers er det alltid arbeideren med den høyeste poengsummen som tilordnes for å fullføre en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="7e9de-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

