---
title: Kjør og Overvåk et eksperiment
description: Dette emnet beskriver hvordan du kjører og overvåker et eksperiment i en tredjepartstjeneste. Det beskriver også hvordan du endrer variasjoner etter at eksperimentet er startet.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4cb7d863d9d69612aa0c340099c1f7861c9d12ba
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930259"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="c4ff1-104">Kjør og Overvåk et eksperiment</span><span class="sxs-lookup"><span data-stu-id="c4ff1-104">Run and monitor an experiment</span></span>

<span data-ttu-id="c4ff1-105">Dette emnet beskriver hvordan du kjører og overvåker eksperimentet i en tredjepartsapp, og om nødvendig endre variasjoner.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="c4ff1-106">Før du fullfører trinnene i dette emnet, må du [publisere](experimentation-preview-publish.md) eksperimentet i Commerce.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-106">Before you complete the steps in this topic, you'll need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> <span data-ttu-id="c4ff1-107">Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c4ff1-108">Flere trinn er beskrevet i separate emner.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="c4ff1-109">[ ![Brukerreise for eksperimentering – kjøre og overvåke](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c4ff1-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="c4ff1-110">Når du har publisert variasjonene, utføres alle trinnene du må gjøre i Commerce for å kjøre eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-110">After you publish your variations, all the steps you need to do in Commerce to run your experiment are done.</span></span> <span data-ttu-id="c4ff1-111">Neste trinn avgjør hvilken variasjon som skal vises for hver bruker når de ber om en side.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="c4ff1-112">Tredjepartstjenesten avgjør dette, men først må du aktivere eksperimentet i tjenesten.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="c4ff1-113">Siden trinnene for aktivering av et eksperiment varierer fra tjeneste til tjeneste, må du følge instruksjonene som er inkludert i tjenesten eller fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="c4ff1-114">Hvis eksperimentet ikke er aktivert, vil brukere bare se standardversjonen av siden – ingen variasjoner vil bli vist.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-114">If the experiment is not activated, users will only see the default version of the page - no variations will be displayed.</span></span>

<span data-ttu-id="c4ff1-115">Du må kjøre eksperimentet lenge nok til å samle inn data for statistisk gyldige resultater.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="c4ff1-116">Bruk tredjepartstjenesten til å overvåke eksperimentrelaterte data og analyser mens eksperimentet kjører.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="c4ff1-117">Justere variasjonene</span><span class="sxs-lookup"><span data-stu-id="c4ff1-117">Adjust your variations</span></span>
<span data-ttu-id="c4ff1-118">Hvis du av en eller annen grunn må endre variasjonene, følger du fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4ff1-119">Hvis du utfører endringer i et liveeksperiment i Commerce eller en tredjepartstjeneste, kan resultatene bli betydelig påvirket.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="c4ff1-120">Vurder å la eksperimentet kjøre ferdig og deretter opprette et nytt eksperimenter for store endringer.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="c4ff1-121">Gå til kategorien **Eksperimenter** i områdebygger, og velg eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-121">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
1. <span data-ttu-id="c4ff1-122">Velg variasjonen du vil oppdatere fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="c4ff1-123">Utføre nødvendige endringer, og forhåndsvis og publiser deretter variasjonene.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-123">Make needed changes, then preview and publish the variations.</span></span> <span data-ttu-id="c4ff1-124">Hvis du vil ha mer informasjon, kan du se [Forhåndsvise og publisere et eksperiment](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="c4ff1-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="c4ff1-125">Gå til tredjepartstjenesten for å gjøre endringer som er knyttet til eksperimentoppsettet.</span><span class="sxs-lookup"><span data-stu-id="c4ff1-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="c4ff1-126">Forrige trinn</span><span class="sxs-lookup"><span data-stu-id="c4ff1-126">Previous step</span></span>
[<span data-ttu-id="c4ff1-127">Forhåndsvise og publisere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="c4ff1-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="c4ff1-128">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="c4ff1-128">Next step</span></span>
[<span data-ttu-id="c4ff1-129">Fremme en variasjon og fullføre et eksperiment</span><span class="sxs-lookup"><span data-stu-id="c4ff1-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)
