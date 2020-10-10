---
title: Definer foretrukne vedlikeholdspersoner
description: Dette emnet forklarer hvordan du definerer foretrukne vedlikeholdspersoner i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c0637609a34890360a3b81355a8d21ef1b9faf8c
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888935"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="2991e-103">Definer foretrukne vedlikeholdspersoner</span><span class="sxs-lookup"><span data-stu-id="2991e-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2991e-104">Under planlegging av arbeidsordrer kan du angi hvilke vedlikeholdspersoner eller hvilken arbeidsgruppe som foretrekkes til å fullføre arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="2991e-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="2991e-105">Bruk av denne funksjonaliteten er valgfri, men den kan hjelpe deg med å velge vedlikeholdspersonen som er mest kvalifisert for å fullføre en jobb, basert på arbeiderkompetanse.</span><span class="sxs-lookup"><span data-stu-id="2991e-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="2991e-106">Bare vedlikeholdspersoner som er tilgjengelige på planleggingstidspunktet, vil bli planlagt.</span><span class="sxs-lookup"><span data-stu-id="2991e-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="2991e-107">Hvis et oppsett av foretrukken vedlikeholdsperson samsvarer med en arbeidsordre under planlegging, men vedlikeholdspersonen er tilordnet andre jobber, blir arbeidsordren planlagt til en annen, tilgjengelig vedlikeholdsperson.</span><span class="sxs-lookup"><span data-stu-id="2991e-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="2991e-108">Før du kan definere foretrukne vedlikeholdsarbeidere, må du først definere vedlikeholdsarbeiderne og arbeidsgruppene.</span><span class="sxs-lookup"><span data-stu-id="2991e-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="2991e-109">Se [Vedlikeholdspersoner og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md) hvis du vil ha en beskrivelse av hvordan du definerer vedlikeholdspersoner og arbeidsgrupper.</span><span class="sxs-lookup"><span data-stu-id="2991e-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="2991e-110">Definere foretrukne arbeidere</span><span class="sxs-lookup"><span data-stu-id="2991e-110">Set up preferred workers</span></span>

<span data-ttu-id="2991e-111">En foretrukket vedlikeholdsperson eller arbeidsgruppe kan knyttes til én eller flere av følgende:</span><span class="sxs-lookup"><span data-stu-id="2991e-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="2991e-112">handel</span><span class="sxs-lookup"><span data-stu-id="2991e-112">trade</span></span>  
- <span data-ttu-id="2991e-113">variant av vedlikeholdsjobbtype</span><span class="sxs-lookup"><span data-stu-id="2991e-113">maintenance job type variant</span></span>  
- <span data-ttu-id="2991e-114">type vedlikeholdsjobb</span><span class="sxs-lookup"><span data-stu-id="2991e-114">maintenance job type</span></span>  
- <span data-ttu-id="2991e-115">kategori for type vedlikeholdsjobb</span><span class="sxs-lookup"><span data-stu-id="2991e-115">maintenance job type category</span></span>  
- <span data-ttu-id="2991e-116">eiendeler</span><span class="sxs-lookup"><span data-stu-id="2991e-116">asset</span></span>  
- <span data-ttu-id="2991e-117">aktivumtype</span><span class="sxs-lookup"><span data-stu-id="2991e-117">asset type</span></span>  

<span data-ttu-id="2991e-118">Jo flere valg du gjør for den samme posten, jo mer spesifikt blir oppsettet.</span><span class="sxs-lookup"><span data-stu-id="2991e-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="2991e-119">Klikk på **Aktivastyring** > **Oppsett** > **Arbeidere** > **Foretrukne vedlikeholdspersoner**.</span><span class="sxs-lookup"><span data-stu-id="2991e-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="2991e-120">Klikk **Ny** for å opprette en ny post.</span><span class="sxs-lookup"><span data-stu-id="2991e-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="2991e-121">Start ved å opprette en "standard" vedlikeholdsarbeider eller arbeidsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2991e-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="2991e-122">Dette betyr at du bare gjør et valg i feltet **Foretrukket vedlikeholdspersongruppe** eller feltet **Foretrukket vedlikeholdsperson**.</span><span class="sxs-lookup"><span data-stu-id="2991e-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="2991e-123">I skjermdumpen nedenfor ser du et eksempel i den første posten der "Forespørsler" er valgt som **Foretrukket vedlikeholdspersongruppe**.</span><span class="sxs-lookup"><span data-stu-id="2991e-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="2991e-124">Standardoppsettet vil bli brukt ved arbeidsordreplanlegging hvis ingen annen, mer spesifikk kombinasjon samsvarer med innholdet i arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="2991e-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="2991e-125">Gjenta trinn 2 for å opprette en ny post.</span><span class="sxs-lookup"><span data-stu-id="2991e-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="2991e-126">Gjør de nødvendige valgene, avhengig av detaljnivået for den foretrukne arbeideren eller arbeidsgruppen.</span><span class="sxs-lookup"><span data-stu-id="2991e-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="2991e-127">*Eksempel:* I skjermdumpen nedenfor i den sjette posten er vedlikeholdsarbeideren Shawn Richardson valgt som foretrukket arbeider.</span><span class="sxs-lookup"><span data-stu-id="2991e-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="2991e-128">Han velges automatisk under planlegging av en arbeidsordre som inneholder aktivaet "CH-BP1-03-02" og vedlikeholdsjobbtypen "Fasilitetsvurdering" hvis han er tilgjengelig på det planlagte tidspunktet.</span><span class="sxs-lookup"><span data-stu-id="2991e-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="2991e-129">Når en foretrukket vedlikeholdsarbeider velges under planlegging av arbeidsordre, går vanligvis Aktivastyring gjennom alle **Foretrukne vedlikeholdspersoner**-postene for å se etter et mulig treff, og kontrollerer alltid den mest spesifikke kombinasjonen først.</span><span class="sxs-lookup"><span data-stu-id="2991e-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="2991e-130">Hvis det ikke blir funnet noe treff, brukes standardposten med et valg i enten feltet **Foretrukket vedlikeholdsarbeidsgruppe** eller feltet **Foretrukket vedlikeholdsperson**.</span><span class="sxs-lookup"><span data-stu-id="2991e-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![Figur 1](media/02-work-order-scheduling.png)

<span data-ttu-id="2991e-132">Du kan også definere *ansvarlige* vedlikeholdspersoner som kan velges når en vedlikeholdsforespørsel eller arbeidsordre opprettes.</span><span class="sxs-lookup"><span data-stu-id="2991e-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="2991e-133">I **Alle arbeidsordrer** og **Alle vedlikeholdsforespørsler** kan du redigere valget hvis det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="2991e-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="2991e-134">Se [Ansvarlige vedlikeholdsarbeidere](../setup-for-maintenance-requests/responsible-workers.md) for å få mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="2991e-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="2991e-135">Under planleggingen av arbeidsordrer beregnes ulike poeng for å bestemme hvilke arbeidere som skal fullføre jobbene for en arbeidsordre (disse resultatene defineres i **Aktivabehandlingsparametere** > **Planlegging av arbeidsordre**-koblingen).</span><span class="sxs-lookup"><span data-stu-id="2991e-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="2991e-136">Hvis to eller flere foretrukne vedlikeholdsarbeidere eller ansvarlige vedlikeholdsarbeidere får samme resultat under planleggingen av arbeidsordre, blir én arbeider tilfeldig valgt.</span><span class="sxs-lookup"><span data-stu-id="2991e-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="2991e-137">Ellers er det alltid arbeideren med den høyeste poengsummen som tilordnes for å fullføre en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="2991e-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

