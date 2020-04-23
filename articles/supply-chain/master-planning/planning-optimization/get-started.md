---
title: Kom i gang med planleggingsoptimalisering
description: Dette emnet forklarer hvordan du begynner å bruke funksjonen for planleggingsoptimalisering.
author: ChristianRytt
manager: tfehr
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4f9124e824a0b6d5035b2567cb19c2c494390d55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213521"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="d3d79-103">Kom i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="d3d79-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3d79-104">Planleggingsoptimaliseringsfunksjonaliteten støtter for øyeblikket ikke alle funksjonene som er tilgjengelige i planleggingsmotoren som er innebygd i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d3d79-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d3d79-105">Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig i planleggingsoptimalisering, oppfyller kravene dine.</span><span class="sxs-lookup"><span data-stu-id="d3d79-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="d3d79-106">Som standard er ikke planleggingsoptimaliseringsfunksjonaliteten aktivert i Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="d3d79-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="d3d79-107">Du har derfor mulighet til å gjennomføre evalueringen før den er slått på.</span><span class="sxs-lookup"><span data-stu-id="d3d79-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="d3d79-108">Til slutt erstatter planleggingsoptimalisering den eksisterende innebygde planleggingsmotoren Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d3d79-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="d3d79-109">Før du slår på planleggingsoptimalisering, anbefaler vi på det sterkeste at du evaluerer resultatene i tilpassingsanalysen av planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="d3d79-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="d3d79-110">Hvis du vil ha mer informasjon, se [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d3d79-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="d3d79-111">Lisensiering</span><span class="sxs-lookup"><span data-stu-id="d3d79-111">Licensing</span></span>

<span data-ttu-id="d3d79-112">Hvis du kan kjøre hovedplanlegging ved hjelp av den gjeldende lisensen, trenger du ikke kjøpe en tilleggslisens for å bruke planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="d3d79-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="d3d79-113">Installer tillegget</span><span class="sxs-lookup"><span data-stu-id="d3d79-113">Install the add-in</span></span>

<span data-ttu-id="d3d79-114">Hvis du vil bruke planleggingsoptimalisering, må du installere tillegget for planleggingsoptimalisering for Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d3d79-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d3d79-115">Du får tilgang til tillegget fra LCS-prosjektet og kan aktivere funksjonaliteten for planleggingsoptimalisering fra brukergrensesnittet for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d3d79-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="d3d79-116">Kravet for planleggingsoptimalisering er et LCS-aktivert miljø med høy tilgjengelighet (ikke et OneBox-miljø), med Dynamics 365 Supply Chain Management versjon 10.0.7 eller senere.</span><span class="sxs-lookup"><span data-stu-id="d3d79-116">The requirement for Planning Optimization is an LCS enabled high-availability environment (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span>

1. <span data-ttu-id="d3d79-117">Logg på LCS, og åpne ønsket miljø.</span><span class="sxs-lookup"><span data-stu-id="d3d79-117">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="d3d79-118">Gå til **Detaljerte opplysninger**.</span><span class="sxs-lookup"><span data-stu-id="d3d79-118">Go to **Full details**.</span></span>
1. <span data-ttu-id="d3d79-119">Bla ned til **Miljøtillegg**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="d3d79-119">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="d3d79-120">Velg **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="d3d79-120">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="d3d79-121">Velg **Planleggingsoptimalisering**.</span><span class="sxs-lookup"><span data-stu-id="d3d79-121">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="d3d79-122">Følg installasjonsveiledningen, og godta vilkårene.</span><span class="sxs-lookup"><span data-stu-id="d3d79-122">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="d3d79-123">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="d3d79-123">Select **Install**.</span></span>
1. <span data-ttu-id="d3d79-124">I **Miljøtillegg**-hurtigfanen skal du se at planleggingsoptimalisering installeres.</span><span class="sxs-lookup"><span data-stu-id="d3d79-124">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="d3d79-125">Etter noen minutter skal **Installerer** endres til **Installert** (det er mulig at du må oppdatere siden).</span><span class="sxs-lookup"><span data-stu-id="d3d79-125">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="d3d79-126">Når installasjonen er fullført, er du klar til å aktivere planleggingsoptimalisering i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d3d79-126">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="d3d79-127">Integrering av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="d3d79-127">Planning Optimization integration</span></span>

<span data-ttu-id="d3d79-128">Hvis du vil konfigurere om planleggingsoptimaliserings-tillegget skal brukes til hovedplanlegging, går du til **Hovedplanlegging** \> **Oppsett** \> **Parametere for planleggingsoptimalisering**.</span><span class="sxs-lookup"><span data-stu-id="d3d79-128">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="d3d79-129">Tilkoblingsstatus</span><span class="sxs-lookup"><span data-stu-id="d3d79-129">Connection status</span></span>

<span data-ttu-id="d3d79-130">Tilkoblingsstatusen angir gjeldende status for tilkoblingen mellom Supply Chain Management og planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="d3d79-130">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="d3d79-131">Tabellen nedenfor viser mulige verdier.</span><span class="sxs-lookup"><span data-stu-id="d3d79-131">The following table shows the possible values.</span></span>

| <span data-ttu-id="d3d79-132">Tilkoblingsstatus</span><span class="sxs-lookup"><span data-stu-id="d3d79-132">Connection status</span></span> | <span data-ttu-id="d3d79-133">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d3d79-133">Description</span></span> | <span data-ttu-id="d3d79-134">Kan planleggingsoptimalisering brukes?</span><span class="sxs-lookup"><span data-stu-id="d3d79-134">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="d3d79-135">Tilkoblet</span><span class="sxs-lookup"><span data-stu-id="d3d79-135">Connected</span></span> | <span data-ttu-id="d3d79-136">Det er opprettet en forbindelse mellom planleggingsoptimaliseringstjenesten og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d3d79-136">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="d3d79-137">Ja</span><span class="sxs-lookup"><span data-stu-id="d3d79-137">Yes</span></span> |
| <span data-ttu-id="d3d79-138">Aktiverer tilkobling</span><span class="sxs-lookup"><span data-stu-id="d3d79-138">Enabling connection</span></span> | <span data-ttu-id="d3d79-139">En forespørsel om å aktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår.</span><span class="sxs-lookup"><span data-stu-id="d3d79-139">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="d3d79-140">Nei</span><span class="sxs-lookup"><span data-stu-id="d3d79-140">No</span></span> |
| <span data-ttu-id="d3d79-141">Frakoblet</span><span class="sxs-lookup"><span data-stu-id="d3d79-141">Disconnected</span></span> | <span data-ttu-id="d3d79-142">Det er ingen forbindelse til planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="d3d79-142">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="d3d79-143">Tilkoblingen kan aktiveres fra LCS, som beskrevet tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="d3d79-143">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="d3d79-144">Nei</span><span class="sxs-lookup"><span data-stu-id="d3d79-144">No</span></span> |
| <span data-ttu-id="d3d79-145">Deaktiverer tilkobling</span><span class="sxs-lookup"><span data-stu-id="d3d79-145">Disabling connection</span></span> | <span data-ttu-id="d3d79-146">En forespørsel om å deaktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår.</span><span class="sxs-lookup"><span data-stu-id="d3d79-146">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="d3d79-147">Nei</span><span class="sxs-lookup"><span data-stu-id="d3d79-147">No</span></span> |
| <span data-ttu-id="d3d79-148">Henter status</span><span class="sxs-lookup"><span data-stu-id="d3d79-148">Getting status</span></span> | <span data-ttu-id="d3d79-149">Systemet venter på statusinformasjon fra planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="d3d79-149">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="d3d79-150">Nei</span><span class="sxs-lookup"><span data-stu-id="d3d79-150">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="d3d79-151">Alternativet Bruk planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="d3d79-151">The Use Planning Optimization option</span></span>

<span data-ttu-id="d3d79-152">Innstillingen for alternativet **Bruk planleggingsoptimalisering** bestemmer hvilken planleggingsmotor som skal brukes til hovedplanlegging:</span><span class="sxs-lookup"><span data-stu-id="d3d79-152">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="d3d79-153">**Ja** – planleggingsoptimalisering brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="d3d79-153">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="d3d79-154">**Nei** – den innebygde planleggingsmotoren Supply Chain Management brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="d3d79-154">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="d3d79-155">Hvis eksisterende satsvise planleggingsjobber for den innebygde planleggingsmotoren Supply Chain Management utløses når alternativet **Bruk planleggingsoptimalisering** er satt til **Ja**, vil disse jobbene mislykkes.</span><span class="sxs-lookup"><span data-stu-id="d3d79-155">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="d3d79-156">Integrering med oppsettet</span><span class="sxs-lookup"><span data-stu-id="d3d79-156">Integration with the setup</span></span>

<span data-ttu-id="d3d79-157">Hvis forhåndsvisning av planleggingsoptimalisering er aktivert, utføres hovedplanlegging ved hjelp av tillegget for planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="d3d79-157">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="d3d79-158">I dette tilfellet berøres resultater og funksjoner for hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="d3d79-158">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="d3d79-159">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="d3d79-159">Related resources</span></span>

[<span data-ttu-id="d3d79-160">Vilkår for forhåndsvisningen</span><span class="sxs-lookup"><span data-stu-id="d3d79-160">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="d3d79-161">Oversikt over planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="d3d79-161">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="d3d79-162">Tilpassingsanalyse av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="d3d79-162">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="d3d79-163">Vise planhistorikk og planleggingslogger</span><span class="sxs-lookup"><span data-stu-id="d3d79-163">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="d3d79-164">Bruke filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="d3d79-164">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="d3d79-165">Annullere en planleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="d3d79-165">Cancel a planning job</span></span>](cancel-planning-job.md)
