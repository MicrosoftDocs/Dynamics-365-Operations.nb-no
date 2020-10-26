---
title: Kom i gang med planleggingsoptimalisering
description: Dette emnet forklarer hvordan du begynner å bruke funksjonen for planleggingsoptimalisering.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
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
ms.openlocfilehash: 49025d0aa0f6a627b816a43dd4260449942b400c
ms.sourcegitcommit: ae04c7cb48f7ecafe71bbe77a0f97715e6290991
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973482"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="5091a-103">Komme i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="5091a-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5091a-104">Som [tidligere annonsert](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) skal Planleggingsoptimalisering erstatte den eksisterende innebygde planleggingsmotoren.</span><span class="sxs-lookup"><span data-stu-id="5091a-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="5091a-105">Hvis du bruker den innebygde hovedplanleggingsmotoren, bør du begynne å planlegge migreringen til Planleggingsoptimalisering nå.</span><span class="sxs-lookup"><span data-stu-id="5091a-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="5091a-106">Det er viktig at du starter migreringsprosessen med én gang, fordi operasjonene kan bli påvirket når avskrivingen fremtvinges.</span><span class="sxs-lookup"><span data-stu-id="5091a-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="5091a-107">Vi oppfordrer deg på det sterkeste til å fullføre migreringen før 1. desember 2020 for å unngå problemer i siste øyeblikk når avskrivingen fremtvinges.</span><span class="sxs-lookup"><span data-stu-id="5091a-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="5091a-108">Funksjonen Planleggingsoptimalisering støtter for øyeblikket ikke alle funksjonene som er tilgjengelige i planleggingsmotoren som er innebygd i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5091a-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="5091a-109">Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig i planleggingsoptimalisering, oppfyller kravene dine.</span><span class="sxs-lookup"><span data-stu-id="5091a-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="5091a-110">Funksjonen Planleggingsoptimalisering er for øyeblikket ikke aktivert som standard i Dynamics Lifecycle Services (LCS), slik at du kan gjennomføre evalueringen før funksjonen aktiveres.</span><span class="sxs-lookup"><span data-stu-id="5091a-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="5091a-111">Du må be om et unntak fra migreringen til Planleggingsoptimalisering hvis hovedplanleggingsprosessen ikke inkluderer produksjon (hovedplanlegging genererer planlagte produksjonsordrer), og du trenger den innebygde hovedplanleggingsmotoren etter versjon 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="5091a-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="5091a-112">Fra og med versjon 10.0.16 blir det vist en feil i miljøer ved kjøring av innebygd hovedplanlegging uten generering av planlagte produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="5091a-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="5091a-113">Planleggingsoptimalisering bør brukes for alle nye distribusjoner som ikke genererer planlagte produksjonsordrer under hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="5091a-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="5091a-114">Eiere av eksisterende miljøer som kjører den innebygde hovedplanleggingsmotoren uten generering av planlagte produksjonsordrer, vil motta en e-post med detaljer om unntaksprosessen.</span><span class="sxs-lookup"><span data-stu-id="5091a-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="5091a-115">Vi anbefaler at du samarbeider med en partner for å evaluere og planlegge migreringen til Planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="5091a-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="5091a-116">Før du slår på planleggingsoptimalisering, anbefaler vi på det sterkeste at du evaluerer resultatene i tilpassingsanalysen av planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="5091a-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="5091a-117">Hvis du vil ha mer informasjon, se [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5091a-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="5091a-118">Tilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="5091a-118">Availability</span></span>
<span data-ttu-id="5091a-119">Planleggingsoptimalisering er for øyeblikket tilgjengelig i følgende Azure-områder: USA, Canada, Europa, Storbritannia og Australia.</span><span class="sxs-lookup"><span data-stu-id="5091a-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="5091a-120">Hvis du prøver å installere tillegget fra et annet geografisk område, vil LCS vise en melding om at dette området ikke støttes.</span><span class="sxs-lookup"><span data-stu-id="5091a-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="5091a-121">Legg merke til at planleggingsoptimalisering ikke støtter lokale distribusjoner av Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5091a-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="5091a-122">Lisensiering</span><span class="sxs-lookup"><span data-stu-id="5091a-122">Licensing</span></span>

<span data-ttu-id="5091a-123">Hvis du kan kjøre hovedplanlegging ved hjelp av den gjeldende lisensen, trenger du ikke kjøpe en tilleggslisens for å bruke planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="5091a-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="5091a-124">Installer tillegget</span><span class="sxs-lookup"><span data-stu-id="5091a-124">Install the add-in</span></span>

<span data-ttu-id="5091a-125">Hvis du vil bruke planleggingsoptimalisering, må du installere tillegget for planleggingsoptimalisering for Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5091a-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5091a-126">Du får tilgang til tillegget fra LCS-prosjektet og kan aktivere funksjonaliteten for planleggingsoptimalisering fra brukergrensesnittet for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5091a-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="5091a-127">Kravet for planleggingsoptimalisering er et LCS-aktivert miljø med høy tilgjengelighet, lag 2 eller høyere (ikke et OneBox-miljø), med Dynamics 365 Supply Chain Management versjon 10.0.7 eller senere.</span><span class="sxs-lookup"><span data-stu-id="5091a-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="5091a-128">Hvis du prøver å installere tillegget i et OneBox-miljø, vil ikke installasjonen bli fullført, og du må avbryte installasjonen.</span><span class="sxs-lookup"><span data-stu-id="5091a-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="5091a-129">Logg på LCS, og åpne ønsket miljø.</span><span class="sxs-lookup"><span data-stu-id="5091a-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="5091a-130">Gå til **Detaljerte opplysninger** .</span><span class="sxs-lookup"><span data-stu-id="5091a-130">Go to **Full details** .</span></span>
1. <span data-ttu-id="5091a-131">Bla ned til **Miljøtillegg** -hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="5091a-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="5091a-132">Velg **Installer et nytt tillegg** .</span><span class="sxs-lookup"><span data-stu-id="5091a-132">Select **Install a new add-in** .</span></span>
1. <span data-ttu-id="5091a-133">Velg **Planleggingsoptimalisering** .</span><span class="sxs-lookup"><span data-stu-id="5091a-133">Select **Planning Optimization** .</span></span>
1. <span data-ttu-id="5091a-134">Følg installasjonsveiledningen, og godta vilkårene.</span><span class="sxs-lookup"><span data-stu-id="5091a-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="5091a-135">Velg **Installer** .</span><span class="sxs-lookup"><span data-stu-id="5091a-135">Select **Install** .</span></span>
1. <span data-ttu-id="5091a-136">I **Miljøtillegg** -hurtigfanen skal du se at planleggingsoptimalisering installeres.</span><span class="sxs-lookup"><span data-stu-id="5091a-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="5091a-137">Etter noen minutter skal **Installerer** endres til **Installert** (det er mulig at du må oppdatere siden).</span><span class="sxs-lookup"><span data-stu-id="5091a-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="5091a-138">Når installasjonen er fullført, er du klar til å aktivere planleggingsoptimalisering i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5091a-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="5091a-139">Integrering av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="5091a-139">Planning Optimization integration</span></span>

<span data-ttu-id="5091a-140">Hvis du vil konfigurere om planleggingsoptimaliserings-tillegget skal brukes til hovedplanlegging, går du til **Hovedplanlegging** \> **Oppsett** \> **Parametere for planleggingsoptimalisering** .</span><span class="sxs-lookup"><span data-stu-id="5091a-140">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters** .</span></span>

#### <a name="connection-status"></a><span data-ttu-id="5091a-141">Tilkoblingsstatus</span><span class="sxs-lookup"><span data-stu-id="5091a-141">Connection status</span></span>

<span data-ttu-id="5091a-142">Tilkoblingsstatusen angir gjeldende status for tilkoblingen mellom Supply Chain Management og planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="5091a-142">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="5091a-143">Tabellen nedenfor viser mulige verdier.</span><span class="sxs-lookup"><span data-stu-id="5091a-143">The following table shows the possible values.</span></span>

| <span data-ttu-id="5091a-144">Tilkoblingsstatus</span><span class="sxs-lookup"><span data-stu-id="5091a-144">Connection status</span></span> | <span data-ttu-id="5091a-145">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5091a-145">Description</span></span> | <span data-ttu-id="5091a-146">Kan planleggingsoptimalisering brukes?</span><span class="sxs-lookup"><span data-stu-id="5091a-146">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="5091a-147">Tilkoblet</span><span class="sxs-lookup"><span data-stu-id="5091a-147">Connected</span></span> | <span data-ttu-id="5091a-148">Det er opprettet en forbindelse mellom planleggingsoptimaliseringstjenesten og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5091a-148">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="5091a-149">Ja</span><span class="sxs-lookup"><span data-stu-id="5091a-149">Yes</span></span> |
| <span data-ttu-id="5091a-150">Aktiverer tilkobling</span><span class="sxs-lookup"><span data-stu-id="5091a-150">Enabling connection</span></span> | <span data-ttu-id="5091a-151">En forespørsel om å aktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår.</span><span class="sxs-lookup"><span data-stu-id="5091a-151">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="5091a-152">Nei</span><span class="sxs-lookup"><span data-stu-id="5091a-152">No</span></span> |
| <span data-ttu-id="5091a-153">Frakoblet</span><span class="sxs-lookup"><span data-stu-id="5091a-153">Disconnected</span></span> | <span data-ttu-id="5091a-154">Det er ingen forbindelse til planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="5091a-154">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="5091a-155">Tilkoblingen kan aktiveres fra LCS, som beskrevet tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="5091a-155">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="5091a-156">Nei</span><span class="sxs-lookup"><span data-stu-id="5091a-156">No</span></span> |
| <span data-ttu-id="5091a-157">Deaktiverer tilkobling</span><span class="sxs-lookup"><span data-stu-id="5091a-157">Disabling connection</span></span> | <span data-ttu-id="5091a-158">En forespørsel om å deaktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår.</span><span class="sxs-lookup"><span data-stu-id="5091a-158">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="5091a-159">Nei</span><span class="sxs-lookup"><span data-stu-id="5091a-159">No</span></span> |
| <span data-ttu-id="5091a-160">Henter status</span><span class="sxs-lookup"><span data-stu-id="5091a-160">Getting status</span></span> | <span data-ttu-id="5091a-161">Systemet venter på statusinformasjon fra planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="5091a-161">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="5091a-162">Nei</span><span class="sxs-lookup"><span data-stu-id="5091a-162">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="5091a-163">Alternativet Bruk planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="5091a-163">The Use Planning Optimization option</span></span>

<span data-ttu-id="5091a-164">Innstillingen for alternativet **Bruk planleggingsoptimalisering** bestemmer hvilken planleggingsmotor som skal brukes til hovedplanlegging:</span><span class="sxs-lookup"><span data-stu-id="5091a-164">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="5091a-165">**Ja** – planleggingsoptimalisering brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="5091a-165">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="5091a-166">**Nei** – den innebygde planleggingsmotoren Supply Chain Management brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="5091a-166">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="5091a-167">Hvis eksisterende satsvise planleggingsjobber for den innebygde planleggingsmotoren Supply Chain Management utløses når alternativet **Bruk planleggingsoptimalisering** er satt til **Ja** , vil disse jobbene mislykkes.</span><span class="sxs-lookup"><span data-stu-id="5091a-167">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes** , those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="5091a-168">Integrering med oppsettet</span><span class="sxs-lookup"><span data-stu-id="5091a-168">Integration with the setup</span></span>

<span data-ttu-id="5091a-169">Hvis forhåndsvisning av planleggingsoptimalisering er aktivert, utføres hovedplanlegging ved hjelp av tillegget for planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="5091a-169">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="5091a-170">I dette tilfellet berøres resultater og funksjoner for hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="5091a-170">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5091a-171">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5091a-171">Additional resources</span></span>

[<span data-ttu-id="5091a-172">Vilkår for forhåndsvisningen</span><span class="sxs-lookup"><span data-stu-id="5091a-172">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="5091a-173">Oversikt over planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="5091a-173">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="5091a-174">Tilpassingsanalyse av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="5091a-174">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="5091a-175">Vise planhistorikk og planleggingslogger</span><span class="sxs-lookup"><span data-stu-id="5091a-175">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="5091a-176">Bruke filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="5091a-176">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="5091a-177">Annullere en planleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="5091a-177">Cancel a planning job</span></span>](cancel-planning-job.md)
