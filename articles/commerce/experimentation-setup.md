---
title: Konfigurere et eksperiment
description: Dette emnet beskriver hvordan konfigurerer et eksperiment i en tredjepartstjeneste.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: 29c21ceb4c259f463f4a039942e51141201a9809
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/22/2020
ms.locfileid: "4414786"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="7a385-103">Konfigurere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="7a385-103">Set up an experiment</span></span>

<span data-ttu-id="7a385-104">Når du [definerer en hypotese og fastslår hvilke suksessmåledata du vil bruke](experimentation-identify.md), må du konfigurere eksperimentet i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="7a385-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="7a385-105">Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7a385-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="7a385-106">Flere trinn er beskrevet i separate emner.</span><span class="sxs-lookup"><span data-stu-id="7a385-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="7a385-107">[ ![Brukerreise for eksperimentering – konfigurere](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="7a385-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="7a385-108">Konfigurere eksperimentet i tredjepartstjenesten</span><span class="sxs-lookup"><span data-stu-id="7a385-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="7a385-109">Nå bør du ha valgt tredjepartstjenesten for å kjøre og overvåke eksperimentet og konfigurert eksperimenteringskoblingen.</span><span class="sxs-lookup"><span data-stu-id="7a385-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="7a385-110">Disse forutsetningene er oppført i [Eksperimentering i Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7a385-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="7a385-111">Følg trinnene som er nødvendige for å opprette eksperimentet i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="7a385-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="7a385-112">Hvis koblingen er riktig konfigurert, vil den fullstendige listen over eksperimenter du konfigurerer i tredjepartstjenesten, vises i Commerce-områdebygger i løpet av omtrent 5 minutter.</span><span class="sxs-lookup"><span data-stu-id="7a385-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will appear in Commerce site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="7a385-113">Konfigurere suksessmåledata</span><span class="sxs-lookup"><span data-stu-id="7a385-113">Set up your success metrics</span></span>
<span data-ttu-id="7a385-114">Alle eksperimenter trenger måledata for å måle virkningen av variasjonene og validere hypotesen.</span><span class="sxs-lookup"><span data-stu-id="7a385-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="7a385-115">Følg fremgangsmåten nedenfor for å aktivere beregningen av måledataene i tredjepartstjenesten ved hjelp av hendelser fra livetelemetrihendelser fra Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7a385-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7a385-116">Gjør følgende for å konfigurere suksessmåledataene.</span><span class="sxs-lookup"><span data-stu-id="7a385-116">To set up your success metrics, follow these steps.</span></span>

1. <span data-ttu-id="7a385-117">I Commerce-områdebygger velger du kategorien **Sider** i venstre navigasjonsrute, og deretter velger du siden du vil samle inn måledata for.</span><span class="sxs-lookup"><span data-stu-id="7a385-117">In Commerce site builder, select **Pages** in the left navigation pane, and then select the page that you want to collect metrics for.</span></span> 
1. <span data-ttu-id="7a385-118">Gå til delen **Hendelses-ID-er som skal spores** i egenskapsruten til høyre for siden eller modulen du vil spore.</span><span class="sxs-lookup"><span data-stu-id="7a385-118">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="7a385-119">Velg **Vis**.</span><span class="sxs-lookup"><span data-stu-id="7a385-119">Select **View**.</span></span> <span data-ttu-id="7a385-120">Det vises en liste over alle hendelses-ID-er.</span><span class="sxs-lookup"><span data-stu-id="7a385-120">A list of all event IDs is displayed.</span></span> <span data-ttu-id="7a385-121">Kopier hendelsen du vil spore, og lim inn hendelsesnøkkelen i den angitte plasseringen i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="7a385-121">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="7a385-122">Hvis du trenger mer enn én hendelse, kopierer du nøklene én om gangen.</span><span class="sxs-lookup"><span data-stu-id="7a385-122">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="7a385-123">Hvis du vil lære hvordan du viser alle tilgjengelige hendelser og attributter, inkludert sidevisninger og inntektssporing, kan du se [Hendelser for Commerce-komponent for diagnose og feilsøking](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="7a385-123">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="7a385-124">Utfør eventuelle andre trinn for å spore måledata som kreves i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="7a385-124">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="7a385-125">Forrige trinn</span><span class="sxs-lookup"><span data-stu-id="7a385-125">Previous step</span></span>
[<span data-ttu-id="7a385-126">Identifisere en hypotese og fastslå måledataene for et eksperiment</span><span class="sxs-lookup"><span data-stu-id="7a385-126">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="7a385-127">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="7a385-127">Next step</span></span>
[<span data-ttu-id="7a385-128">Koble til og redigere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="7a385-128">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)
