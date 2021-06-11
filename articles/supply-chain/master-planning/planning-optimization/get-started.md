---
title: Kom i gang med planleggingsoptimalisering
description: Dette emnet forklarer hvordan du begynner å bruke funksjonen for planleggingsoptimalisering.
author: ChristianRytt
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d12e1908e234c841fb705266b2255c6c5e2140e1
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103599"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="f0abb-103">Komme i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="f0abb-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0abb-104">Som [tidligere annonsert](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) skal Planleggingsoptimalisering erstatte den eksisterende innebygde planleggingsmotoren.</span><span class="sxs-lookup"><span data-stu-id="f0abb-104">As [previously announced](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="f0abb-105">Hvis du bruker den innebygde hovedplanleggingsmotoren, bør du begynne å planlegge migreringen til Planleggingsoptimalisering nå.</span><span class="sxs-lookup"><span data-stu-id="f0abb-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="f0abb-106">Det er viktig at du starter migreringsprosessen med én gang, fordi operasjonene kan bli påvirket når avskrivingen fremtvinges.</span><span class="sxs-lookup"><span data-stu-id="f0abb-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="f0abb-107">Vi oppfordrer deg på det sterkeste til å fullføre migreringen før 1. desember 2020 for å unngå problemer i siste øyeblikk når avskrivingen fremtvinges.</span><span class="sxs-lookup"><span data-stu-id="f0abb-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="f0abb-108">Funksjonen Planleggingsoptimalisering støtter for øyeblikket ikke alle funksjonene som er tilgjengelige i planleggingsmotoren som er innebygd i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0abb-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="f0abb-109">Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig i planleggingsoptimalisering, oppfyller kravene dine.</span><span class="sxs-lookup"><span data-stu-id="f0abb-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="f0abb-110">Funksjonen Planleggingsoptimalisering er for øyeblikket ikke aktivert som standard i Dynamics Lifecycle Services (LCS), slik at du kan gjennomføre evalueringen før funksjonen aktiveres.</span><span class="sxs-lookup"><span data-stu-id="f0abb-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="f0abb-111">Du må be om et unntak fra migreringen til Planleggingsoptimalisering hvis hovedplanleggingsprosessen ikke inkluderer produksjon (hovedplanlegging genererer planlagte produksjonsordrer), og du trenger den innebygde hovedplanleggingsmotoren etter versjon 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="f0abb-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="f0abb-112">Fra og med versjon 10.0.16 blir det vist en feil i miljøer ved kjøring av innebygd hovedplanlegging uten generering av planlagte produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="f0abb-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="f0abb-113">Planleggingsoptimalisering bør brukes for alle nye distribusjoner som ikke genererer planlagte produksjonsordrer under hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="f0abb-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="f0abb-114">Eiere av eksisterende miljøer som kjører den innebygde hovedplanleggingsmotoren uten generering av planlagte produksjonsordrer, vil motta en e-post med detaljer om unntaksprosessen.</span><span class="sxs-lookup"><span data-stu-id="f0abb-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="f0abb-115">Det anbefales at du samarbeider med en partner for å evaluere og planlegge migreringen til Planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="f0abb-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="f0abb-116">Før du slår på planleggingsoptimalisering, anbefaler vi på det sterkeste at du evaluerer resultatene i tilpassingsanalysen av planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="f0abb-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="f0abb-117">Hvis du vil ha mer informasjon, se [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f0abb-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="availability"></a><span data-ttu-id="f0abb-118">Tilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="f0abb-118">Availability</span></span>

<span data-ttu-id="f0abb-119">Planleggingsoptimalisering er for øyeblikket tilgjengelig i følgende Azure-områder: USA, Canada, Europa, Storbritannia, Australia og Asia/Stillehavskysten.</span><span class="sxs-lookup"><span data-stu-id="f0abb-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, Australia, and Asia Pacific.</span></span> <span data-ttu-id="f0abb-120">Hvis du prøver å installere tillegget fra et annet geografisk område, vil LCS vise en melding om at dette området ikke støttes.</span><span class="sxs-lookup"><span data-stu-id="f0abb-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="f0abb-121">Legg merke til at planleggingsoptimalisering ikke støtter lokale distribusjoner av Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0abb-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

## <a name="licensing"></a><span data-ttu-id="f0abb-122">Lisensiering</span><span class="sxs-lookup"><span data-stu-id="f0abb-122">Licensing</span></span>

<span data-ttu-id="f0abb-123">Hvis du kan kjøre hovedplanlegging ved hjelp av den gjeldende lisensen, trenger du ikke kjøpe en tilleggslisens for å bruke planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="f0abb-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

## <a name="install-and-enable-planning-optimization"></a><span data-ttu-id="f0abb-124">Installere og aktivere planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="f0abb-124">Install and enable Planning Optimization</span></span>

<span data-ttu-id="f0abb-125">For å kunne bruke planleggingsoptimalisering må du kontrollere at alle forutsetningene er på plass i systemet, og deretter aktivere lisensnøkkelen og installere tillegget for planleggingsoptimalisering for Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0abb-125">To use Planning Optimization, you must make sure your system has all of the prerequisites in place and then enable its license key and install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f0abb-126">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="f0abb-126">Prerequisites</span></span>

<span data-ttu-id="f0abb-127">Før du kan installere tillegget for planleggingsoptimalisering, må følgende forutsetninger være på plass:</span><span class="sxs-lookup"><span data-stu-id="f0abb-127">Before you install the Planning Optimization Add-in, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="f0abb-128">Du må kjøre Supply Chain Management i et LCS-aktivert miljø med høy tilgjengelighet, lag 2 eller høyere (ikke et OneBox-miljø), med Dynamics 365 Supply Chain Management versjon 10.0.7 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="f0abb-128">You must be running Supply Chain Management on an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="f0abb-129">Hvis du prøver å installere tillegget i et OneBox-miljø, vil ikke installasjonen bli fullført, og du må avbryte installasjonen.</span><span class="sxs-lookup"><span data-stu-id="f0abb-129">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

- <span data-ttu-id="f0abb-130">Systemet må være konfigurert for Power Platform-integrering.</span><span class="sxs-lookup"><span data-stu-id="f0abb-130">Your system must be set up for Power Platform integration.</span></span> <span data-ttu-id="f0abb-131">Hvis du vil ha mer informasjon, se [Microsoft Power Platform-integrering med Finance and Operations-apper](../../../fin-ops-core/dev-itpro/power-platform/overview.md).</span><span class="sxs-lookup"><span data-stu-id="f0abb-131">For more information, see [Microsoft Power Platform integration with Finance and Operations apps](../../../fin-ops-core/dev-itpro/power-platform/overview.md).</span></span>

### <a name="enable-the-planning-optimization-license"></a><span data-ttu-id="f0abb-132">Aktivere lisensen for planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="f0abb-132">Enable the Planning Optimization license</span></span>

<span data-ttu-id="f0abb-133">Hvis du vil bruke planleggingsoptimalisering, må du aktivere konfigurasjonsnøkkelen.</span><span class="sxs-lookup"><span data-stu-id="f0abb-133">To use Planning Optimization, you must enable its configuration key.</span></span> <span data-ttu-id="f0abb-134">Slik gjør du dette:</span><span class="sxs-lookup"><span data-stu-id="f0abb-134">To do so:</span></span>

1. <span data-ttu-id="f0abb-135">Sett systemet i vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="f0abb-135">Put your system into maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="f0abb-136">Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="f0abb-136">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="f0abb-137">Merk av for **Planleggingsoptimalisering** i fanen **Konfigurasjonsnøkler**.</span><span class="sxs-lookup"><span data-stu-id="f0abb-137">On the **Configuration keys** tab, select the check box for **Planning Optimization**.</span></span>
1. <span data-ttu-id="f0abb-138">Deaktiver vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="f0abb-138">Turn off maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

### <a name="install-the-planning-optimization-add-in"></a><span data-ttu-id="f0abb-139">Installere tillegget for planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="f0abb-139">Install the Planning Optimization Add-in</span></span>

<span data-ttu-id="f0abb-140">Du må installere tillegget fra LCS-prosjektet og deretter aktivere funksjonaliteten for planleggingsoptimalisering fra brukergrensesnittet for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0abb-140">You must install the add-in from your LCS project and then turn on the Planning Optimization functionality from the Supply Chain Management user interface.</span></span>

<span data-ttu-id="f0abb-141">Slik installerer du tillegget for planleggingsoptimalisering:</span><span class="sxs-lookup"><span data-stu-id="f0abb-141">To install the Planning Optimization Add-in:</span></span>

1. <span data-ttu-id="f0abb-142">Logg på LCS, og åpne ønsket miljø.</span><span class="sxs-lookup"><span data-stu-id="f0abb-142">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="f0abb-143">Gå til **Detaljerte opplysninger**.</span><span class="sxs-lookup"><span data-stu-id="f0abb-143">Go to **Full details**.</span></span>
1. <span data-ttu-id="f0abb-144">Bla ned til **Miljøtillegg**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="f0abb-144">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="f0abb-145">Velg **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="f0abb-145">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="f0abb-146">Velg **Planleggingsoptimalisering**.</span><span class="sxs-lookup"><span data-stu-id="f0abb-146">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="f0abb-147">Følg installasjonsveiledningen, og godta vilkårene.</span><span class="sxs-lookup"><span data-stu-id="f0abb-147">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="f0abb-148">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="f0abb-148">Select **Install**.</span></span>
1. <span data-ttu-id="f0abb-149">I hurtigfanen **Miljøtillegg** skal du se at planleggingsoptimalisering installeres.</span><span class="sxs-lookup"><span data-stu-id="f0abb-149">On the **Environment add-ins** FastTab, you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="f0abb-150">Etter noen minutter skal **Installerer** endres til **Installert** (det er mulig at du må oppdatere siden).</span><span class="sxs-lookup"><span data-stu-id="f0abb-150">After a few minutes, **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="f0abb-151">Når installasjonen er fullført, er du klar til å aktivere planleggingsoptimalisering i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0abb-151">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="f0abb-152">Hovedformålet med å installere tillegget for planleggingsoptimalisering er å koble til tjenesten og miljøet.</span><span class="sxs-lookup"><span data-stu-id="f0abb-152">The main purpose of installing the Planning Optimization Add-in is to connect the service and the environment.</span></span> <span data-ttu-id="f0abb-153">Derfor må du installere tillegget separat i hvert miljø der du bruker Planleggingsoptimalisering, uavhengig av hvilken kode som er flyttet mellom miljøene.</span><span class="sxs-lookup"><span data-stu-id="f0abb-153">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

## <a name="integrate-planning-optimization-with-your-system"></a><span data-ttu-id="f0abb-154">Integrere planleggingsoptimalisering med systemet</span><span class="sxs-lookup"><span data-stu-id="f0abb-154">Integrate Planning Optimization with your system</span></span>

<span data-ttu-id="f0abb-155">Hvis du vil konfigurere om planleggingsoptimaliserings-tillegget skal brukes til hovedplanlegging, går du til **Hovedplanlegging** \> **Oppsett** \> **Parametere for planleggingsoptimalisering**.</span><span class="sxs-lookup"><span data-stu-id="f0abb-155">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

### <a name="connection-status"></a><span data-ttu-id="f0abb-156">Tilkoblingsstatus</span><span class="sxs-lookup"><span data-stu-id="f0abb-156">Connection status</span></span>

<span data-ttu-id="f0abb-157">Tilkoblingsstatusen angir gjeldende status for tilkoblingen mellom Supply Chain Management og planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="f0abb-157">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="f0abb-158">Tabellen nedenfor viser mulige verdier.</span><span class="sxs-lookup"><span data-stu-id="f0abb-158">The following table shows the possible values.</span></span>

| <span data-ttu-id="f0abb-159">Tilkoblingsstatus</span><span class="sxs-lookup"><span data-stu-id="f0abb-159">Connection status</span></span> | <span data-ttu-id="f0abb-160">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f0abb-160">Description</span></span> | <span data-ttu-id="f0abb-161">Kan planleggingsoptimalisering brukes?</span><span class="sxs-lookup"><span data-stu-id="f0abb-161">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="f0abb-162">Tilkoblet</span><span class="sxs-lookup"><span data-stu-id="f0abb-162">Connected</span></span> | <span data-ttu-id="f0abb-163">Det er opprettet en forbindelse mellom planleggingsoptimaliseringstjenesten og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0abb-163">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="f0abb-164">Ja</span><span class="sxs-lookup"><span data-stu-id="f0abb-164">Yes</span></span> |
| <span data-ttu-id="f0abb-165">Aktiverer tilkobling</span><span class="sxs-lookup"><span data-stu-id="f0abb-165">Enabling connection</span></span> | <span data-ttu-id="f0abb-166">En forespørsel om å aktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår.</span><span class="sxs-lookup"><span data-stu-id="f0abb-166">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="f0abb-167">Nei</span><span class="sxs-lookup"><span data-stu-id="f0abb-167">No</span></span> |
| <span data-ttu-id="f0abb-168">Frakoblet</span><span class="sxs-lookup"><span data-stu-id="f0abb-168">Disconnected</span></span> | <span data-ttu-id="f0abb-169">Det er ingen forbindelse til planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="f0abb-169">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="f0abb-170">Tilkoblingen kan aktiveres fra LCS, som beskrevet tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="f0abb-170">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="f0abb-171">Nei</span><span class="sxs-lookup"><span data-stu-id="f0abb-171">No</span></span> |
| <span data-ttu-id="f0abb-172">Deaktiverer tilkobling</span><span class="sxs-lookup"><span data-stu-id="f0abb-172">Disabling connection</span></span> | <span data-ttu-id="f0abb-173">En forespørsel om å deaktivere tilkoblingen til planleggingsoptimaliseringstjenesten pågår.</span><span class="sxs-lookup"><span data-stu-id="f0abb-173">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="f0abb-174">Nei</span><span class="sxs-lookup"><span data-stu-id="f0abb-174">No</span></span> |
| <span data-ttu-id="f0abb-175">Henter status</span><span class="sxs-lookup"><span data-stu-id="f0abb-175">Getting status</span></span> | <span data-ttu-id="f0abb-176">Systemet venter på statusinformasjon fra planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="f0abb-176">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="f0abb-177">Nei</span><span class="sxs-lookup"><span data-stu-id="f0abb-177">No</span></span> |

### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="f0abb-178">Alternativet Bruk planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="f0abb-178">The Use Planning Optimization option</span></span>

<span data-ttu-id="f0abb-179">Innstillingen for alternativet **Bruk planleggingsoptimalisering** bestemmer hvilken planleggingsmotor som skal brukes til hovedplanlegging:</span><span class="sxs-lookup"><span data-stu-id="f0abb-179">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="f0abb-180">**Ja** – planleggingsoptimalisering brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="f0abb-180">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="f0abb-181">**Nei** – den innebygde planleggingsmotoren Supply Chain Management brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="f0abb-181">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="f0abb-182">Hvis eksisterende satsvise planleggingsjobber for den innebygde planleggingsmotoren Supply Chain Management utløses når alternativet **Bruk planleggingsoptimalisering** er satt til **Ja**, vil disse jobbene mislykkes.</span><span class="sxs-lookup"><span data-stu-id="f0abb-182">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="f0abb-183">Integrering med oppsettet</span><span class="sxs-lookup"><span data-stu-id="f0abb-183">Integration with the setup</span></span>

<span data-ttu-id="f0abb-184">Hvis Planleggingsoptimalisering er aktivert, utføres hovedplanlegging ved hjelp av tillegget for planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="f0abb-184">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="f0abb-185">I dette tilfellet berøres resultater og funksjoner for hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="f0abb-185">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0abb-186">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f0abb-186">Additional resources</span></span>

[<span data-ttu-id="f0abb-187">Vilkår for forhåndsvisningen</span><span class="sxs-lookup"><span data-stu-id="f0abb-187">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="f0abb-188">Oversikt over planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="f0abb-188">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="f0abb-189">Tilpassingsanalyse av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="f0abb-189">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="f0abb-190">Vise planhistorikk og planleggingslogger</span><span class="sxs-lookup"><span data-stu-id="f0abb-190">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="f0abb-191">Bruke filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="f0abb-191">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="f0abb-192">Annullere en planleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="f0abb-192">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
