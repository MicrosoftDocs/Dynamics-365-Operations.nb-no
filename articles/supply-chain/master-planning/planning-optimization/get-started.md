---
title: Kom i gang med planleggingsoptimalisering
description: Dette emnet forklarer hvordan du begynner å bruke funksjonen for planleggingsoptimalisering.
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
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
ms.openlocfilehash: 04b39469ccf4f088bb33bdfc73ce40eece6f5f2e
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887270"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="f3abc-103">Kom i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="f3abc-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3abc-104">Planleggingsoptimaliseringsfunksjonaliteten støtter for øyeblikket ikke alle funksjonene som er tilgjengelige i planleggingsmotoren som er innebygd i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3abc-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f3abc-105">Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig i planleggingsoptimalisering, oppfyller kravene dine.</span><span class="sxs-lookup"><span data-stu-id="f3abc-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="f3abc-106">Som standard er ikke planleggingsoptimaliseringsfunksjonaliteten aktivert i Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f3abc-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="f3abc-107">Du har derfor mulighet til å gjennomføre evalueringen før den er slått på.</span><span class="sxs-lookup"><span data-stu-id="f3abc-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="f3abc-108">Til slutt erstatter planleggingsoptimalisering den eksisterende innebygde planleggingsmotoren Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3abc-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="f3abc-109">Før du slår på planleggingsoptimalisering, anbefaler vi på det sterkeste at du evaluerer resultatene i tilpassingsanalysen av planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="f3abc-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="f3abc-110">Hvis du vil ha mer informasjon, se [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f3abc-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="f3abc-111">Tilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="f3abc-111">Availability</span></span>
<span data-ttu-id="f3abc-112">Planleggingsoptimalisering er for øyeblikket tilgjengelig i følgende Azure-områder: USA, Canada, Europa, Storbritannia og Australia.</span><span class="sxs-lookup"><span data-stu-id="f3abc-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="f3abc-113">Hvis du prøver å installere tillegget fra et annet geografisk område, vil LCS vise en melding om at dette området ikke støttes.</span><span class="sxs-lookup"><span data-stu-id="f3abc-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="f3abc-114">Legg merke til at planleggingsoptimalisering ikke støtter lokale distribusjoner av Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3abc-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="f3abc-115">Lisensiering</span><span class="sxs-lookup"><span data-stu-id="f3abc-115">Licensing</span></span>

<span data-ttu-id="f3abc-116">Hvis du kan kjøre hovedplanlegging ved hjelp av den gjeldende lisensen, trenger du ikke kjøpe en tilleggslisens for å bruke planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="f3abc-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="f3abc-117">Installer tillegget</span><span class="sxs-lookup"><span data-stu-id="f3abc-117">Install the add-in</span></span>

<span data-ttu-id="f3abc-118">Hvis du vil bruke planleggingsoptimalisering, må du installere tillegget for planleggingsoptimalisering for Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3abc-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f3abc-119">Du får tilgang til tillegget fra LCS-prosjektet og kan aktivere funksjonaliteten for planleggingsoptimalisering fra brukergrensesnittet for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3abc-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="f3abc-120">Kravet for planleggingsoptimalisering er et LCS-aktivert miljø med høy tilgjengelighet, lag 2 eller høyere (ikke et OneBox-miljø), med Dynamics 365 Supply Chain Management versjon 10.0.7 eller senere.</span><span class="sxs-lookup"><span data-stu-id="f3abc-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="f3abc-121">Hvis du prøver å installere tillegget i et OneBox-miljø, vil ikke installasjonen bli fullført, og du må avbryte installasjonen.</span><span class="sxs-lookup"><span data-stu-id="f3abc-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="f3abc-122">Logg på LCS, og åpne ønsket miljø.</span><span class="sxs-lookup"><span data-stu-id="f3abc-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="f3abc-123">Gå til **Detaljerte opplysninger**.</span><span class="sxs-lookup"><span data-stu-id="f3abc-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="f3abc-124">Bla ned til **Miljøtillegg**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="f3abc-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="f3abc-125">Velg **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="f3abc-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="f3abc-126">Velg **Planleggingsoptimalisering**.</span><span class="sxs-lookup"><span data-stu-id="f3abc-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="f3abc-127">Følg installasjonsveiledningen, og godta vilkårene.</span><span class="sxs-lookup"><span data-stu-id="f3abc-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="f3abc-128">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="f3abc-128">Select **Install**.</span></span>
1. <span data-ttu-id="f3abc-129">I **Miljøtillegg**-hurtigfanen skal du se at planleggingsoptimalisering installeres.</span><span class="sxs-lookup"><span data-stu-id="f3abc-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="f3abc-130">Etter noen minutter skal **Installerer** endres til **Installert** (det er mulig at du må oppdatere siden).</span><span class="sxs-lookup"><span data-stu-id="f3abc-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="f3abc-131">Når installasjonen er fullført, er du klar til å aktivere planleggingsoptimalisering i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3abc-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="f3abc-132">Integrering av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="f3abc-132">Planning Optimization integration</span></span>

<span data-ttu-id="f3abc-133">Hvis du vil konfigurere om planleggingsoptimaliserings-tillegget skal brukes til hovedplanlegging, går du til **Hovedplanlegging** \> **Oppsett** \> **Parametere for planleggingsoptimalisering**.</span><span class="sxs-lookup"><span data-stu-id="f3abc-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="f3abc-134">Tilkoblingsstatus</span><span class="sxs-lookup"><span data-stu-id="f3abc-134">Connection status</span></span>

<span data-ttu-id="f3abc-135">Tilkoblingsstatusen angir gjeldende status for tilkoblingen mellom Supply Chain Management og planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="f3abc-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="f3abc-136">Tabellen nedenfor viser mulige verdier.</span><span class="sxs-lookup"><span data-stu-id="f3abc-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="f3abc-137">Tilkoblingsstatus</span><span class="sxs-lookup"><span data-stu-id="f3abc-137">Connection status</span></span> | <span data-ttu-id="f3abc-138">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f3abc-138">Description</span></span> | <span data-ttu-id="f3abc-139">Kan planleggingsoptimalisering brukes?</span><span class="sxs-lookup"><span data-stu-id="f3abc-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="f3abc-140">Tilkoblet</span><span class="sxs-lookup"><span data-stu-id="f3abc-140">Connected</span></span> | <span data-ttu-id="f3abc-141">Det er opprettet en forbindelse mellom planleggingsoptimaliseringstjenesten og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3abc-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="f3abc-142">Ja</span><span class="sxs-lookup"><span data-stu-id="f3abc-142">Yes</span></span> |
| <span data-ttu-id="f3abc-143">Aktiverer tilkobling</span><span class="sxs-lookup"><span data-stu-id="f3abc-143">Enabling connection</span></span> | <span data-ttu-id="f3abc-144">En forespørsel om å aktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår.</span><span class="sxs-lookup"><span data-stu-id="f3abc-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="f3abc-145">Nei</span><span class="sxs-lookup"><span data-stu-id="f3abc-145">No</span></span> |
| <span data-ttu-id="f3abc-146">Frakoblet</span><span class="sxs-lookup"><span data-stu-id="f3abc-146">Disconnected</span></span> | <span data-ttu-id="f3abc-147">Det er ingen forbindelse til planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="f3abc-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="f3abc-148">Tilkoblingen kan aktiveres fra LCS, som beskrevet tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="f3abc-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="f3abc-149">Nei</span><span class="sxs-lookup"><span data-stu-id="f3abc-149">No</span></span> |
| <span data-ttu-id="f3abc-150">Deaktiverer tilkobling</span><span class="sxs-lookup"><span data-stu-id="f3abc-150">Disabling connection</span></span> | <span data-ttu-id="f3abc-151">En forespørsel om å deaktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår.</span><span class="sxs-lookup"><span data-stu-id="f3abc-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="f3abc-152">Nei</span><span class="sxs-lookup"><span data-stu-id="f3abc-152">No</span></span> |
| <span data-ttu-id="f3abc-153">Henter status</span><span class="sxs-lookup"><span data-stu-id="f3abc-153">Getting status</span></span> | <span data-ttu-id="f3abc-154">Systemet venter på statusinformasjon fra planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="f3abc-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="f3abc-155">Nei</span><span class="sxs-lookup"><span data-stu-id="f3abc-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="f3abc-156">Alternativet Bruk planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="f3abc-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="f3abc-157">Innstillingen for alternativet **Bruk planleggingsoptimalisering** bestemmer hvilken planleggingsmotor som skal brukes til hovedplanlegging:</span><span class="sxs-lookup"><span data-stu-id="f3abc-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="f3abc-158">**Ja** – planleggingsoptimalisering brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="f3abc-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="f3abc-159">**Nei** – den innebygde planleggingsmotoren Supply Chain Management brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="f3abc-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="f3abc-160">Hvis eksisterende satsvise planleggingsjobber for den innebygde planleggingsmotoren Supply Chain Management utløses når alternativet **Bruk planleggingsoptimalisering** er satt til **Ja**, vil disse jobbene mislykkes.</span><span class="sxs-lookup"><span data-stu-id="f3abc-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="f3abc-161">Integrering med oppsettet</span><span class="sxs-lookup"><span data-stu-id="f3abc-161">Integration with the setup</span></span>

<span data-ttu-id="f3abc-162">Hvis forhåndsvisning av planleggingsoptimalisering er aktivert, utføres hovedplanlegging ved hjelp av tillegget for planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="f3abc-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="f3abc-163">I dette tilfellet berøres resultater og funksjoner for hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="f3abc-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3abc-164">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f3abc-164">Additional resources</span></span>

[<span data-ttu-id="f3abc-165">Vilkår for forhåndsvisningen</span><span class="sxs-lookup"><span data-stu-id="f3abc-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="f3abc-166">Oversikt over planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="f3abc-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="f3abc-167">Tilpassingsanalyse av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="f3abc-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="f3abc-168">Vise planhistorikk og planleggingslogger</span><span class="sxs-lookup"><span data-stu-id="f3abc-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="f3abc-169">Bruke filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="f3abc-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="f3abc-170">Annullere en planleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="f3abc-170">Cancel a planning job</span></span>](cancel-planning-job.md)
