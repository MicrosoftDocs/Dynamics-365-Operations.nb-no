---
title: Konfigurere et eksperiment
description: Dette emnet beskriver hvordan konfigurerer et eksperiment i en tredjepartstjeneste.
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
ms.openlocfilehash: 0f7db0ce009f6ee7603952891aacfdc16fcde016
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930260"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="bfe06-103">Konfigurere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="bfe06-103">Set up an experiment</span></span>

<span data-ttu-id="bfe06-104">Når du [definerer en hypotese og fastslår hvilke suksessmåledata du vil bruke](experimentation-identify.md), må du konfigurere eksperimentet i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="bfe06-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="bfe06-105">Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bfe06-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="bfe06-106">Flere trinn er beskrevet i separate emner.</span><span class="sxs-lookup"><span data-stu-id="bfe06-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="bfe06-107">[ ![Brukerreise for eksperimentering – konfigurere](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="bfe06-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="bfe06-108">Konfigurere eksperimentet i tredjepartstjenesten</span><span class="sxs-lookup"><span data-stu-id="bfe06-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="bfe06-109">Nå bør du ha valgt tredjepartstjenesten for å kjøre og overvåke eksperimentet og konfigurert eksperimenteringskoblingen.</span><span class="sxs-lookup"><span data-stu-id="bfe06-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="bfe06-110">Disse forutsetningene er oppført i [Eksperimentering i Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bfe06-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="bfe06-111">Følg trinnene som er nødvendige for å opprette eksperimentet i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="bfe06-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="bfe06-112">Hvis koblingen er riktig konfigurert, vil den fullstendige listen over eksperimenter du konfigurerer i tredjepartstjenesten, vises i områdebygger i løpet av omtrent 5 minutter.</span><span class="sxs-lookup"><span data-stu-id="bfe06-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will surface in site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="bfe06-113">Konfigurere suksessmåledata</span><span class="sxs-lookup"><span data-stu-id="bfe06-113">Set up your success metrics</span></span>
<span data-ttu-id="bfe06-114">Alle eksperimenter trenger måledata for å måle virkningen av variasjonene og validere hypotesen.</span><span class="sxs-lookup"><span data-stu-id="bfe06-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="bfe06-115">Følg fremgangsmåten nedenfor for å aktivere beregningen av måledataene i tredjepartstjenesten ved hjelp av hendelser fra livetelemetrihendelser fra Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bfe06-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

1. <span data-ttu-id="bfe06-116">I områdebygger velger du kategorien **Sider** i venstre navigasjonsrute, og deretter velger du siden du vil samle inn måledata for.</span><span class="sxs-lookup"><span data-stu-id="bfe06-116">In site builder, select the **Pages** tab in the left navigation pane and then select the page that you want to collect metrics on.</span></span> 
1. <span data-ttu-id="bfe06-117">Gå til delen **Hendelses-ID-er som skal spores** i egenskapsruten til høyre for siden eller modulen du vil spore.</span><span class="sxs-lookup"><span data-stu-id="bfe06-117">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="bfe06-118">Velg **Vis** .</span><span class="sxs-lookup"><span data-stu-id="bfe06-118">Select **View** .</span></span> <span data-ttu-id="bfe06-119">Det vises en liste over alle hendelses-ID-er.</span><span class="sxs-lookup"><span data-stu-id="bfe06-119">A list of all event IDs is displayed.</span></span> <span data-ttu-id="bfe06-120">Kopier hendelsen du vil spore, og lim inn hendelsesnøkkelen i den angitte plasseringen i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="bfe06-120">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="bfe06-121">Hvis du trenger mer enn én hendelse, kopierer du nøklene én om gangen.</span><span class="sxs-lookup"><span data-stu-id="bfe06-121">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="bfe06-122">Hvis du vil lære hvordan du viser alle tilgjengelige hendelser og attributter, inkludert sidevisninger og inntektssporing, kan du se [Hendelser for Commerce-komponent for diagnose og feilsøking](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="bfe06-122">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="bfe06-123">Utfør eventuelle andre trinn for å spore måledata som kreves i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="bfe06-123">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="bfe06-124">Forrige trinn</span><span class="sxs-lookup"><span data-stu-id="bfe06-124">Previous step</span></span>
[<span data-ttu-id="bfe06-125">Identifisere en hypotese og fastslå måledataene for et eksperiment</span><span class="sxs-lookup"><span data-stu-id="bfe06-125">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="bfe06-126">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="bfe06-126">Next step</span></span>
[<span data-ttu-id="bfe06-127">Koble til og redigere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="bfe06-127">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)
