---
title: Kom i gang med planleggingsoptimalisering
description: Dette emnet forklarer hvordan du begynner å bruke funksjonen for planleggingsoptimalisering.
author: ChristianRytt
manager: AnnBe
ms.date: 01/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 3e0371c6addc0412dc2fc105891b012941e92a06
ms.sourcegitcommit: e5a3c85a322a9216b8f176536d664fef40ae0bec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/17/2020
ms.locfileid: "2971470"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="bda9f-103">Kom i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="bda9f-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="bda9f-104">Planleggingsoptimaliseringsfunksjonaliteten støtter for øyeblikket ikke alle funksjonene som er tilgjengelige i planleggingsmotoren som er innebygd i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bda9f-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="bda9f-105">Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig i planleggingsoptimalisering, oppfyller kravene dine.</span><span class="sxs-lookup"><span data-stu-id="bda9f-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="bda9f-106">Som standard er ikke planleggingsoptimaliseringsfunksjonaliteten aktivert i Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="bda9f-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="bda9f-107">Du har derfor mulighet til å gjennomføre evalueringen før den er slått på.</span><span class="sxs-lookup"><span data-stu-id="bda9f-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="bda9f-108">Til slutt erstatter planleggingsoptimalisering den eksisterende innebygde planleggingsmotoren Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bda9f-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="bda9f-109">Før du slår på planleggingsoptimalisering, anbefaler vi på det sterkeste at du evaluerer resultatene i tilpassingsanalysen av planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="bda9f-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="bda9f-110">Hvis du vil ha mer informasjon, se [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="bda9f-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="bda9f-111">Lisensiering</span><span class="sxs-lookup"><span data-stu-id="bda9f-111">Licensing</span></span>

<span data-ttu-id="bda9f-112">Hvis du kan kjøre hovedplanlegging ved hjelp av den gjeldende lisensen, trenger du ikke kjøpe en tilleggslisens for å bruke planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="bda9f-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="bda9f-113">Installer tillegget</span><span class="sxs-lookup"><span data-stu-id="bda9f-113">Install the add-in</span></span>

<span data-ttu-id="bda9f-114">Hvis du vil bruke planleggingsoptimalisering, må du installere tillegget for planleggingsoptimalisering for Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bda9f-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="bda9f-115">Du får tilgang til tillegget fra LCS-prosjektet og kan aktivere funksjonaliteten for planleggingsoptimalisering fra brukergrensesnittet for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bda9f-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="bda9f-116">Logg på LCS, og åpne ønsket miljø.</span><span class="sxs-lookup"><span data-stu-id="bda9f-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="bda9f-117">Gå til **Detaljerte opplysninger**.</span><span class="sxs-lookup"><span data-stu-id="bda9f-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="bda9f-118">Bla ned til **Miljøtillegg**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="bda9f-118">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="bda9f-119">Velg **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="bda9f-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="bda9f-120">Velg **Planleggingsoptimalisering**.</span><span class="sxs-lookup"><span data-stu-id="bda9f-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="bda9f-121">Følg installasjonsveiledningen, og godta vilkårene.</span><span class="sxs-lookup"><span data-stu-id="bda9f-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="bda9f-122">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="bda9f-122">Select **Install**.</span></span>
1. <span data-ttu-id="bda9f-123">I **Miljøtillegg**-hurtigfanen skal du se at planleggingsoptimalisering installeres.</span><span class="sxs-lookup"><span data-stu-id="bda9f-123">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="bda9f-124">Etter noen minutter skal **Installerer** endres til **Installert** (det er mulig at du må oppdatere siden).</span><span class="sxs-lookup"><span data-stu-id="bda9f-124">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="bda9f-125">Når installasjonen er fullført, er du klar til å aktivere planleggingsoptimalisering i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bda9f-125">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="bda9f-126">Integrering av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="bda9f-126">Planning Optimization integration</span></span>

<span data-ttu-id="bda9f-127">Hvis du vil konfigurere om planleggingsoptimaliserings-tillegget skal brukes til hovedplanlegging, går du til **Hovedplanlegging** \> **Oppsett** \> **Parametere for planleggingsoptimalisering**.</span><span class="sxs-lookup"><span data-stu-id="bda9f-127">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="bda9f-128">Tilkoblingsstatus</span><span class="sxs-lookup"><span data-stu-id="bda9f-128">Connection status</span></span>

<span data-ttu-id="bda9f-129">Tilkoblingsstatusen angir gjeldende status for tilkoblingen mellom Supply Chain Management og planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="bda9f-129">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="bda9f-130">Tabellen nedenfor viser mulige verdier.</span><span class="sxs-lookup"><span data-stu-id="bda9f-130">The following table shows the possible values.</span></span>

| <span data-ttu-id="bda9f-131">Tilkoblingsstatus</span><span class="sxs-lookup"><span data-stu-id="bda9f-131">Connection status</span></span> | <span data-ttu-id="bda9f-132">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="bda9f-132">Description</span></span> | <span data-ttu-id="bda9f-133">Kan planleggingsoptimalisering brukes?</span><span class="sxs-lookup"><span data-stu-id="bda9f-133">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="bda9f-134">Tilkoblet</span><span class="sxs-lookup"><span data-stu-id="bda9f-134">Connected</span></span> | <span data-ttu-id="bda9f-135">Det er opprettet en forbindelse mellom planleggingsoptimaliseringstjenesten og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bda9f-135">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="bda9f-136">Ja</span><span class="sxs-lookup"><span data-stu-id="bda9f-136">Yes</span></span> |
| <span data-ttu-id="bda9f-137">Aktiverer tilkobling</span><span class="sxs-lookup"><span data-stu-id="bda9f-137">Enabling connection</span></span> | <span data-ttu-id="bda9f-138">En forespørsel om å aktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår.</span><span class="sxs-lookup"><span data-stu-id="bda9f-138">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="bda9f-139">Nei</span><span class="sxs-lookup"><span data-stu-id="bda9f-139">No</span></span> |
| <span data-ttu-id="bda9f-140">Frakoblet</span><span class="sxs-lookup"><span data-stu-id="bda9f-140">Disconnected</span></span> | <span data-ttu-id="bda9f-141">Det er ingen forbindelse til planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="bda9f-141">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="bda9f-142">Tilkoblingen kan aktiveres fra LCS, som beskrevet tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="bda9f-142">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="bda9f-143">Nei</span><span class="sxs-lookup"><span data-stu-id="bda9f-143">No</span></span> |
| <span data-ttu-id="bda9f-144">Deaktiverer tilkobling</span><span class="sxs-lookup"><span data-stu-id="bda9f-144">Disabling connection</span></span> | <span data-ttu-id="bda9f-145">En forespørsel om å deaktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår.</span><span class="sxs-lookup"><span data-stu-id="bda9f-145">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="bda9f-146">Nei</span><span class="sxs-lookup"><span data-stu-id="bda9f-146">No</span></span> |
| <span data-ttu-id="bda9f-147">Henter status</span><span class="sxs-lookup"><span data-stu-id="bda9f-147">Getting status</span></span> | <span data-ttu-id="bda9f-148">Systemet venter på statusinformasjon fra planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="bda9f-148">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="bda9f-149">Nei</span><span class="sxs-lookup"><span data-stu-id="bda9f-149">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="bda9f-150">Alternativet Bruk planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="bda9f-150">The Use Planning Optimization option</span></span>

<span data-ttu-id="bda9f-151">Innstillingen for alternativet **Bruk planleggingsoptimalisering** bestemmer hvilken planleggingsmotor som skal brukes til hovedplanlegging:</span><span class="sxs-lookup"><span data-stu-id="bda9f-151">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="bda9f-152">**Ja** – planleggingsoptimalisering brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="bda9f-152">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="bda9f-153">**Nei** – den innebygde planleggingsmotoren Supply Chain Management brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="bda9f-153">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="bda9f-154">Hvis eksisterende satsvise planleggingsjobber for den innebygde planleggingsmotoren Supply Chain Management utløses når alternativet **Bruk planleggingsoptimalisering** er satt til **Ja**, vil disse jobbene mislykkes.</span><span class="sxs-lookup"><span data-stu-id="bda9f-154">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="bda9f-155">Integrering med oppsettet</span><span class="sxs-lookup"><span data-stu-id="bda9f-155">Integration with the setup</span></span>

<span data-ttu-id="bda9f-156">Hvis forhåndsvisning av planleggingsoptimalisering er aktivert, utføres hovedplanlegging ved hjelp av tillegget for planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="bda9f-156">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="bda9f-157">I dette tilfellet berøres resultater og funksjoner for hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="bda9f-157">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="bda9f-158">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="bda9f-158">Related resources</span></span>

[<span data-ttu-id="bda9f-159">Vilkår for forhåndsvisningen</span><span class="sxs-lookup"><span data-stu-id="bda9f-159">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="bda9f-160">Oversikt over planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="bda9f-160">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="bda9f-161">Tilpassingsanalyse av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="bda9f-161">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="bda9f-162">Vise planhistorikk og planleggingslogger</span><span class="sxs-lookup"><span data-stu-id="bda9f-162">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="bda9f-163">Bruke filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="bda9f-163">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="bda9f-164">Annullere en planleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="bda9f-164">Cancel a planning job</span></span>](cancel-planning-job.md)
