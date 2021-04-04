---
title: Når skal et data mart tilbakestilles
description: Dette emnet viser en oversikt over forhold som kan forbedres ved å tilbakestille et data mart, og forhold der det er usannsynlig at tilbakestilling av data mart hjelper.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71324d4aa2d20dd6ae4729412a017d130ab0144f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563743"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="13057-103">Når skal et data mart tilbakestilles</span><span class="sxs-lookup"><span data-stu-id="13057-103">When to reset a data mart</span></span>

<span data-ttu-id="13057-104">Det kan være tidkrevende å tilbakestille et data mart.</span><span class="sxs-lookup"><span data-stu-id="13057-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="13057-105">Denne handlingen er kanskje ikke løsningen som trengs, avhengig av forholdene.</span><span class="sxs-lookup"><span data-stu-id="13057-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="13057-106">Dette emnet viser en oversikt over forhold som kan forbedres ved å tilbakestille et data mart, og forhold der det er usannsynlig at tilbakestilling av data mart hjelper.</span><span class="sxs-lookup"><span data-stu-id="13057-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="13057-107">Når må du tilbakestille et data mart?</span><span class="sxs-lookup"><span data-stu-id="13057-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="13057-108">Vurder følgende spørsmål før du tilbakestiller et data mart.</span><span class="sxs-lookup"><span data-stu-id="13057-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="13057-109">Hvis du svarer ja på ett eller flere spørsmål, kan det bety at organisasjonen kan dra nytte av å tilbakestille data mart.</span><span class="sxs-lookup"><span data-stu-id="13057-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="13057-110">Programdatabasen ble gjenopprettet, men data mart-databasen ble ikke gjenopprettet.</span><span class="sxs-lookup"><span data-stu-id="13057-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="13057-111">Du ser uriktige data for en regnskapsperiode, som ikke er resultatet av et problem med rapportutformingen.</span><span class="sxs-lookup"><span data-stu-id="13057-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="13057-112">Du ser uriktige data for en regnskapsperiode, og postene vises under Integreringsforsøk på siden **Integreringsstatus** i Rapportutforming (start Rapportutforming og velg **Verktøy > Integreringsstatus**).</span><span class="sxs-lookup"><span data-stu-id="13057-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="13057-113">Du har åpnet en støttehendelse, og en kundestøttetekniker har bedt deg om å tilbakestille data mart som en del av et feilsøkingstrinn.</span><span class="sxs-lookup"><span data-stu-id="13057-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="13057-114">Når passer det ikke å tilbakestille et data mart?</span><span class="sxs-lookup"><span data-stu-id="13057-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="13057-115">Det finnes visse omstendigheter der vi anbefaler at du ikke tilbakestiller et data mart.</span><span class="sxs-lookup"><span data-stu-id="13057-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="13057-116">Disse omfatter følgende.</span><span class="sxs-lookup"><span data-stu-id="13057-116">These include the following.</span></span> 

- <span data-ttu-id="13057-117">Hver gang årsaken ikke er oppført i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="13057-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="13057-118">Du har ytelsesproblemer som er knyttet til en datasynkronisering. I slike omstendigheter hjelper det sannsynligvis ikke å tilbakestille data mart.</span><span class="sxs-lookup"><span data-stu-id="13057-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="13057-119">Hvis du har et gjentakende tilbakestillingsmønster av en av følgende årsaker:</span><span class="sxs-lookup"><span data-stu-id="13057-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="13057-120">**Manglende data** – Først eliminerer du for eksempel problemer med rapportutforming og tidsberegning av synkronisering som du ser at faktatilordningen ikke har kjørt siden manglende data ble postert.</span><span class="sxs-lookup"><span data-stu-id="13057-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="13057-121">**Fastlåst integreringstilstand** – Hvis integreringen går tregt eller ser ut til å ha låst seg, kan du sannsynligvis ikke løse problemet ved å tilbakestille data mart.</span><span class="sxs-lookup"><span data-stu-id="13057-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="13057-122">**Forsøk på å tilbakestille har vært mislykket** – Hvis det er gjort en rekke forsøk på å fullføre en tilbakestilling, og alle forsøkene mislyktes på grunn av manglende data, anbefaler vi at du åpner en støttehendelse og arbeider med en kundestøttetekniker for å analysere situasjonen, før du prøver å tilbakestille data mart på nytt.</span><span class="sxs-lookup"><span data-stu-id="13057-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="13057-123">**Foreldede poster** – Foreldede poster alene gir ikke nødvendigvis en god grunn til å tilbakestille data mart.</span><span class="sxs-lookup"><span data-stu-id="13057-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="13057-124">Hvis du har et stort datasett, tar det litt tid å kjøre tilbakestillingsprosessen, men den fører sannsynligvis ikke til forbedringer.</span><span class="sxs-lookup"><span data-stu-id="13057-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="13057-125">Hva en tilbakestilling av data mart ikke gjør</span><span class="sxs-lookup"><span data-stu-id="13057-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="13057-126">En tilbakestilling starter bare når eksisterende oppgaver er fullført.</span><span class="sxs-lookup"><span data-stu-id="13057-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="13057-127">Dette sikrer at gamle data ikke settes inn.</span><span class="sxs-lookup"><span data-stu-id="13057-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="13057-128">På dette tidspunktet kan du for eksempel få meldingen «Tilbakestillingen av data mart kan ikke behandles på grunn av en aktiv oppgave.</span><span class="sxs-lookup"><span data-stu-id="13057-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="13057-129">Prøv på nytt senere.»</span><span class="sxs-lookup"><span data-stu-id="13057-129">Please try again later.”</span></span>
- <span data-ttu-id="13057-130">Tilbakestillingen deaktiverer integreringsoppgavene og sletter alle data mart-data.</span><span class="sxs-lookup"><span data-stu-id="13057-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="13057-131">Integreringen aktiveres på nytt.</span><span class="sxs-lookup"><span data-stu-id="13057-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="13057-132">Følgende punkter angir to ting som tilbakestilling av et data mart *ikke* gjør.</span><span class="sxs-lookup"><span data-stu-id="13057-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="13057-133">Tilbakestillinger fjerner ikke rapportutforminger.</span><span class="sxs-lookup"><span data-stu-id="13057-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="13057-134">Tilbakestillinger fjerner ikke firmadata eller brukerdata med mindre dette velges.</span><span class="sxs-lookup"><span data-stu-id="13057-134">Resets do not clear company data or user data unless selected.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]