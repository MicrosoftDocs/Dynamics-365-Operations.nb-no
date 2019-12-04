---
title: Kom i gang med planleggingsoptimalisering
description: Dette emnet forklarer hvordan du begynner å bruke funksjonen for planleggingsoptimalisering.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
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
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774019"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="e5aad-103">Kom i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="e5aad-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="e5aad-104">Planleggingsoptimaliseringsfunksjonaliteten støtter for øyeblikket ikke alle funksjonene som er tilgjengelige i planleggingsmotoren som er innebygd i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e5aad-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e5aad-105">Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig i planleggingsoptimalisering, oppfyller kravene dine.</span><span class="sxs-lookup"><span data-stu-id="e5aad-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="e5aad-106">Som standard er ikke planleggingsoptimaliseringsfunksjonaliteten aktivert i Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e5aad-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="e5aad-107">Du har derfor mulighet til å gjennomføre evalueringen før den er slått på.</span><span class="sxs-lookup"><span data-stu-id="e5aad-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="e5aad-108">Til slutt erstatter planleggingsoptimalisering den eksisterende innebygde planleggingsmotoren Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e5aad-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="e5aad-109">Før du slår på planleggingsoptimalisering, anbefaler vi på det sterkeste at du evaluerer resultatene i tilpassingsanalysen av planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="e5aad-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="e5aad-110">Hvis du vil ha mer informasjon, se [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e5aad-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="e5aad-111">Lisensiering</span><span class="sxs-lookup"><span data-stu-id="e5aad-111">Licensing</span></span>

<span data-ttu-id="e5aad-112">Hvis du kan kjøre hovedplanlegging ved hjelp av den gjeldende lisensen, trenger du ikke kjøpe en tilleggslisens for å bruke planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="e5aad-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="e5aad-113">Installer tillegget</span><span class="sxs-lookup"><span data-stu-id="e5aad-113">Install the add-in</span></span>

<span data-ttu-id="e5aad-114">Hvis du vil bruke planleggingsoptimalisering, må du installere tillegget for planleggingsoptimalisering for Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e5aad-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e5aad-115">Du får tilgang til tillegget fra LCS-prosjektet og kan aktivere funksjonaliteten for planleggingsoptimalisering fra brukergrensesnittet for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e5aad-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="e5aad-116">Logg på LCS, og åpne ønsket miljø.</span><span class="sxs-lookup"><span data-stu-id="e5aad-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="e5aad-117">Gå til **Detaljerte opplysninger**.</span><span class="sxs-lookup"><span data-stu-id="e5aad-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="e5aad-118">Velg **Vedlikehold**, eller rull ned til hurtigfanen **Miljøtillegg**.</span><span class="sxs-lookup"><span data-stu-id="e5aad-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="e5aad-119">Velg **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="e5aad-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="e5aad-120">Velg **Planleggingsoptimalisering**.</span><span class="sxs-lookup"><span data-stu-id="e5aad-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="e5aad-121">Følg installasjonsveiledningen, og godta vilkårene.</span><span class="sxs-lookup"><span data-stu-id="e5aad-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="e5aad-122">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="e5aad-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="e5aad-123">Integrering av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="e5aad-123">Planning Optimization integration</span></span>

<span data-ttu-id="e5aad-124">Hvis du vil konfigurere om planleggingsoptimaliserings-tillegget skal brukes til hovedplanlegging, går du til **Hovedplanlegging** \> **Oppsett** \> **Integrering av planleggingsoptimalisering** \> **Integreringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="e5aad-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="e5aad-125">Tilkoblingsstatus</span><span class="sxs-lookup"><span data-stu-id="e5aad-125">Connection status</span></span>

<span data-ttu-id="e5aad-126">Tilkoblingsstatusen angir gjeldende status for tilkoblingen mellom Supply Chain Management og planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="e5aad-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="e5aad-127">Tabellen nedenfor viser mulige verdier.</span><span class="sxs-lookup"><span data-stu-id="e5aad-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="e5aad-128">Tilkoblingsstatus</span><span class="sxs-lookup"><span data-stu-id="e5aad-128">Connection status</span></span> | <span data-ttu-id="e5aad-129">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e5aad-129">Description</span></span> | <span data-ttu-id="e5aad-130">Kan planleggingsoptimalisering brukes?</span><span class="sxs-lookup"><span data-stu-id="e5aad-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="e5aad-131">Tilkoblet</span><span class="sxs-lookup"><span data-stu-id="e5aad-131">Connected</span></span> | <span data-ttu-id="e5aad-132">Det er opprettet en forbindelse mellom planleggingsoptimaliseringstjenesten og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e5aad-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="e5aad-133">Ja</span><span class="sxs-lookup"><span data-stu-id="e5aad-133">Yes</span></span> |
| <span data-ttu-id="e5aad-134">Aktiverer tilkobling</span><span class="sxs-lookup"><span data-stu-id="e5aad-134">Enabling connection</span></span> | <span data-ttu-id="e5aad-135">En forespørsel om å aktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår.</span><span class="sxs-lookup"><span data-stu-id="e5aad-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="e5aad-136">Nei</span><span class="sxs-lookup"><span data-stu-id="e5aad-136">No</span></span> |
| <span data-ttu-id="e5aad-137">Frakoblet</span><span class="sxs-lookup"><span data-stu-id="e5aad-137">Disconnected</span></span> | <span data-ttu-id="e5aad-138">Det er ingen forbindelse til planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="e5aad-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="e5aad-139">Tilkoblingen kan aktiveres fra LCS, som beskrevet tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="e5aad-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="e5aad-140">Nei</span><span class="sxs-lookup"><span data-stu-id="e5aad-140">No</span></span> |
| <span data-ttu-id="e5aad-141">Deaktiverer tilkobling</span><span class="sxs-lookup"><span data-stu-id="e5aad-141">Disabling connection</span></span> | <span data-ttu-id="e5aad-142">En forespørsel om å deaktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår.</span><span class="sxs-lookup"><span data-stu-id="e5aad-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="e5aad-143">Nei</span><span class="sxs-lookup"><span data-stu-id="e5aad-143">No</span></span> |
| <span data-ttu-id="e5aad-144">Henter status</span><span class="sxs-lookup"><span data-stu-id="e5aad-144">Getting status</span></span> | <span data-ttu-id="e5aad-145">Systemet venter på statusinformasjon fra planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="e5aad-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="e5aad-146">Nei</span><span class="sxs-lookup"><span data-stu-id="e5aad-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="e5aad-147">Alternativet Bruk planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="e5aad-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="e5aad-148">Innstillingen for alternativet **Bruk planleggingsoptimalisering** bestemmer hvilken planleggingsmotor som skal brukes til hovedplanlegging:</span><span class="sxs-lookup"><span data-stu-id="e5aad-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="e5aad-149">**Ja** – planleggingsoptimalisering brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="e5aad-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="e5aad-150">**Nei** – den innebygde planleggingsmotoren Supply Chain Management brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="e5aad-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="e5aad-151">Hvis eksisterende satsvise planleggingsjobber for den innebygde planleggingsmotoren Supply Chain Management utløses når alternativet **Bruk planleggingsoptimalisering** er satt til **Ja**, vil disse jobbene mislykkes.</span><span class="sxs-lookup"><span data-stu-id="e5aad-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="e5aad-152">Integrering med oppsettet</span><span class="sxs-lookup"><span data-stu-id="e5aad-152">Integration with the setup</span></span>

<span data-ttu-id="e5aad-153">Hvis forhåndsvisning av planleggingsoptimalisering er aktivert, utføres hovedplanlegging ved hjelp av tillegget for planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="e5aad-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="e5aad-154">I dette tilfellet berøres resultater og funksjoner for hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="e5aad-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="e5aad-155">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="e5aad-155">Related resources</span></span>

[<span data-ttu-id="e5aad-156">Vilkår for forhåndsvisningen</span><span class="sxs-lookup"><span data-stu-id="e5aad-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="e5aad-157">Oversikt over planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="e5aad-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="e5aad-158">Tilpassingsanalyse av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="e5aad-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="e5aad-159">Vise planhistorikk og planleggingslogger</span><span class="sxs-lookup"><span data-stu-id="e5aad-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="e5aad-160">Bruke filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="e5aad-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="e5aad-161">Annullere en planleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="e5aad-161">Cancel a planning job</span></span>](cancel-planning-job.md)
