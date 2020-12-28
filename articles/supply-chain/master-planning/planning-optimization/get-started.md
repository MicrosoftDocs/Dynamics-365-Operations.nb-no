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
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434854"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="b2ec2-103">Komme i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="b2ec2-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2ec2-104">Som [tidligere annonsert](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) skal Planleggingsoptimalisering erstatte den eksisterende innebygde planleggingsmotoren.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="b2ec2-105">Hvis du bruker den innebygde hovedplanleggingsmotoren, bør du begynne å planlegge migreringen til Planleggingsoptimalisering nå.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="b2ec2-106">Det er viktig at du starter migreringsprosessen med én gang, fordi operasjonene kan bli påvirket når avskrivingen fremtvinges.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="b2ec2-107">Vi oppfordrer deg på det sterkeste til å fullføre migreringen før 1. desember 2020 for å unngå problemer i siste øyeblikk når avskrivingen fremtvinges.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="b2ec2-108">Funksjonen Planleggingsoptimalisering støtter for øyeblikket ikke alle funksjonene som er tilgjengelige i planleggingsmotoren som er innebygd i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="b2ec2-109">Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig i planleggingsoptimalisering, oppfyller kravene dine.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="b2ec2-110">Funksjonen Planleggingsoptimalisering er for øyeblikket ikke aktivert som standard i Dynamics Lifecycle Services (LCS), slik at du kan gjennomføre evalueringen før funksjonen aktiveres.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="b2ec2-111">Du må be om et unntak fra migreringen til Planleggingsoptimalisering hvis hovedplanleggingsprosessen ikke inkluderer produksjon (hovedplanlegging genererer planlagte produksjonsordrer), og du trenger den innebygde hovedplanleggingsmotoren etter versjon 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="b2ec2-112">Fra og med versjon 10.0.16 blir det vist en feil i miljøer ved kjøring av innebygd hovedplanlegging uten generering av planlagte produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="b2ec2-113">Planleggingsoptimalisering bør brukes for alle nye distribusjoner som ikke genererer planlagte produksjonsordrer under hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="b2ec2-114">Eiere av eksisterende miljøer som kjører den innebygde hovedplanleggingsmotoren uten generering av planlagte produksjonsordrer, vil motta en e-post med detaljer om unntaksprosessen.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="b2ec2-115">Vi anbefaler at du samarbeider med en partner for å evaluere og planlegge migreringen til Planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="b2ec2-116">Før du slår på planleggingsoptimalisering, anbefaler vi på det sterkeste at du evaluerer resultatene i tilpassingsanalysen av planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="b2ec2-117">Hvis du vil ha mer informasjon, se [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b2ec2-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="b2ec2-118">Tilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="b2ec2-118">Availability</span></span>
<span data-ttu-id="b2ec2-119">Planleggingsoptimalisering er for øyeblikket tilgjengelig i følgende Azure-områder: USA, Canada, Europa, Storbritannia og Australia.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="b2ec2-120">Hvis du prøver å installere tillegget fra et annet geografisk område, vil LCS vise en melding om at dette området ikke støttes.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="b2ec2-121">Legg merke til at planleggingsoptimalisering ikke støtter lokale distribusjoner av Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="b2ec2-122">Lisensiering</span><span class="sxs-lookup"><span data-stu-id="b2ec2-122">Licensing</span></span>

<span data-ttu-id="b2ec2-123">Hvis du kan kjøre hovedplanlegging ved hjelp av den gjeldende lisensen, trenger du ikke kjøpe en tilleggslisens for å bruke planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="b2ec2-124">Installer tillegget</span><span class="sxs-lookup"><span data-stu-id="b2ec2-124">Install the add-in</span></span>

<span data-ttu-id="b2ec2-125">Hvis du vil bruke planleggingsoptimalisering, må du installere tillegget for planleggingsoptimalisering for Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b2ec2-126">Du får tilgang til tillegget fra LCS-prosjektet og kan aktivere funksjonaliteten for planleggingsoptimalisering fra brukergrensesnittet for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="b2ec2-127">Kravet for planleggingsoptimalisering er et LCS-aktivert miljø med høy tilgjengelighet, lag 2 eller høyere (ikke et OneBox-miljø), med Dynamics 365 Supply Chain Management versjon 10.0.7 eller senere.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="b2ec2-128">Hvis du prøver å installere tillegget i et OneBox-miljø, vil ikke installasjonen bli fullført, og du må avbryte installasjonen.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="b2ec2-129">Logg på LCS, og åpne ønsket miljø.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="b2ec2-130">Gå til **Detaljerte opplysninger**.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="b2ec2-131">Bla ned til **Miljøtillegg**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="b2ec2-132">Velg **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-132">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="b2ec2-133">Velg **Planleggingsoptimalisering**.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-133">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="b2ec2-134">Følg installasjonsveiledningen, og godta vilkårene.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="b2ec2-135">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-135">Select **Install**.</span></span>
1. <span data-ttu-id="b2ec2-136">I **Miljøtillegg**-hurtigfanen skal du se at planleggingsoptimalisering installeres.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="b2ec2-137">Etter noen minutter skal **Installerer** endres til **Installert** (det er mulig at du må oppdatere siden).</span><span class="sxs-lookup"><span data-stu-id="b2ec2-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="b2ec2-138">Når installasjonen er fullført, er du klar til å aktivere planleggingsoptimalisering i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="b2ec2-139">Hovedformålet med å installere tilleggsfunksjonen for Planleggingsoptimalisering er å koble til tjenesten og miljøet.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-139">The main purpose of installing the Planning Optimization add-in is to connect the service and the environment.</span></span> <span data-ttu-id="b2ec2-140">Derfor må du installere tillegget separat i hvert miljø der du bruker Planleggingsoptimalisering, uavhengig av hvilken kode som er flyttet mellom miljøene.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-140">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="b2ec2-141">Integrering av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="b2ec2-141">Planning Optimization integration</span></span>

<span data-ttu-id="b2ec2-142">Hvis du vil konfigurere om planleggingsoptimaliserings-tillegget skal brukes til hovedplanlegging, går du til **Hovedplanlegging** \> **Oppsett** \> **Parametere for planleggingsoptimalisering**.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-142">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="b2ec2-143">Tilkoblingsstatus</span><span class="sxs-lookup"><span data-stu-id="b2ec2-143">Connection status</span></span>

<span data-ttu-id="b2ec2-144">Tilkoblingsstatusen angir gjeldende status for tilkoblingen mellom Supply Chain Management og planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-144">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="b2ec2-145">Tabellen nedenfor viser mulige verdier.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-145">The following table shows the possible values.</span></span>

| <span data-ttu-id="b2ec2-146">Tilkoblingsstatus</span><span class="sxs-lookup"><span data-stu-id="b2ec2-146">Connection status</span></span> | <span data-ttu-id="b2ec2-147">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b2ec2-147">Description</span></span> | <span data-ttu-id="b2ec2-148">Kan planleggingsoptimalisering brukes?</span><span class="sxs-lookup"><span data-stu-id="b2ec2-148">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="b2ec2-149">Tilkoblet</span><span class="sxs-lookup"><span data-stu-id="b2ec2-149">Connected</span></span> | <span data-ttu-id="b2ec2-150">Det er opprettet en forbindelse mellom planleggingsoptimaliseringstjenesten og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-150">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="b2ec2-151">Ja</span><span class="sxs-lookup"><span data-stu-id="b2ec2-151">Yes</span></span> |
| <span data-ttu-id="b2ec2-152">Aktiverer tilkobling</span><span class="sxs-lookup"><span data-stu-id="b2ec2-152">Enabling connection</span></span> | <span data-ttu-id="b2ec2-153">En forespørsel om å aktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-153">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="b2ec2-154">Nei</span><span class="sxs-lookup"><span data-stu-id="b2ec2-154">No</span></span> |
| <span data-ttu-id="b2ec2-155">Frakoblet</span><span class="sxs-lookup"><span data-stu-id="b2ec2-155">Disconnected</span></span> | <span data-ttu-id="b2ec2-156">Det er ingen forbindelse til planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-156">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="b2ec2-157">Tilkoblingen kan aktiveres fra LCS, som beskrevet tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-157">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="b2ec2-158">Nei</span><span class="sxs-lookup"><span data-stu-id="b2ec2-158">No</span></span> |
| <span data-ttu-id="b2ec2-159">Deaktiverer tilkobling</span><span class="sxs-lookup"><span data-stu-id="b2ec2-159">Disabling connection</span></span> | <span data-ttu-id="b2ec2-160">En forespørsel om å deaktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-160">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="b2ec2-161">Nei</span><span class="sxs-lookup"><span data-stu-id="b2ec2-161">No</span></span> |
| <span data-ttu-id="b2ec2-162">Henter status</span><span class="sxs-lookup"><span data-stu-id="b2ec2-162">Getting status</span></span> | <span data-ttu-id="b2ec2-163">Systemet venter på statusinformasjon fra planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-163">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="b2ec2-164">Nei</span><span class="sxs-lookup"><span data-stu-id="b2ec2-164">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="b2ec2-165">Alternativet Bruk planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="b2ec2-165">The Use Planning Optimization option</span></span>

<span data-ttu-id="b2ec2-166">Innstillingen for alternativet **Bruk planleggingsoptimalisering** bestemmer hvilken planleggingsmotor som skal brukes til hovedplanlegging:</span><span class="sxs-lookup"><span data-stu-id="b2ec2-166">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="b2ec2-167">**Ja** – planleggingsoptimalisering brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-167">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="b2ec2-168">**Nei** – den innebygde planleggingsmotoren Supply Chain Management brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-168">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="b2ec2-169">Hvis eksisterende satsvise planleggingsjobber for den innebygde planleggingsmotoren Supply Chain Management utløses når alternativet **Bruk planleggingsoptimalisering** er satt til **Ja**, vil disse jobbene mislykkes.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-169">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="b2ec2-170">Integrering med oppsettet</span><span class="sxs-lookup"><span data-stu-id="b2ec2-170">Integration with the setup</span></span>

<span data-ttu-id="b2ec2-171">Hvis Planleggingsoptimalisering er aktivert, utføres hovedplanlegging ved hjelp av tillegget for planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-171">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="b2ec2-172">I dette tilfellet berøres resultater og funksjoner for hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="b2ec2-172">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2ec2-173">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b2ec2-173">Additional resources</span></span>

[<span data-ttu-id="b2ec2-174">Vilkår for forhåndsvisningen</span><span class="sxs-lookup"><span data-stu-id="b2ec2-174">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="b2ec2-175">Oversikt over planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="b2ec2-175">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="b2ec2-176">Tilpassingsanalyse av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="b2ec2-176">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="b2ec2-177">Vise planhistorikk og planleggingslogger</span><span class="sxs-lookup"><span data-stu-id="b2ec2-177">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="b2ec2-178">Bruke filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="b2ec2-178">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="b2ec2-179">Annullere en planleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="b2ec2-179">Cancel a planning job</span></span>](cancel-planning-job.md)
