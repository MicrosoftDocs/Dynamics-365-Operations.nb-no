---
title: Konfigurer jobbkort for enheter
description: Dette emnet beskriver de ulike alternativene for konfigurasjon av jobbkortenheten.
author: johanhoffmann
manager: tfehr
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: fc698ac7e0cfc8d6b196abf35658688ad1bc8bc7
ms.sourcegitcommit: 6319a07ee6c36ebb28acaf205bc79d2fd8f7dd5d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/30/2020
ms.locfileid: "3413176"
---
# <a name="configure-job-card-for-devices"></a><span data-ttu-id="6327b-103">Konfigurer jobbkort for enheter</span><span class="sxs-lookup"><span data-stu-id="6327b-103">Configure job card for devices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6327b-104">Jobbkortenheten brukes av butikkansatte til å registrere det daglige arbeidet deres – for eksempel når de begynner på jobber – rapportere tilbakemeldinger om jobber, registrere indirekte aktiviteter og rapportere fravær.</span><span class="sxs-lookup"><span data-stu-id="6327b-104">The job card device is used by the shop floor workers to register their daily work, such as when jobs are started, reporting feedback on jobs, registering indirect activities, and reporting absence.</span></span> <span data-ttu-id="6327b-105">Disse registreringene er grunnlaget for sporing av fremdriften og kostnaden av produksjonsordrer, samt for beregning av grunnlaget for arbeidernes lønn.</span><span class="sxs-lookup"><span data-stu-id="6327b-105">These registrations are the basis for tracking progress and cost on production orders and for calculating the basis for the workers' pay.</span></span> <span data-ttu-id="6327b-106">Dette emnet beskriver de ulike alternativene for konfigurasjon av jobbkortenheter.</span><span class="sxs-lookup"><span data-stu-id="6327b-106">This topic describes the various options for configuring job card devices.</span></span>

## <a name="enable-new-features-in-feature-management"></a><span data-ttu-id="6327b-107">Aktivere nye funksjoner i funksjonsbehandling</span><span class="sxs-lookup"><span data-stu-id="6327b-107">Enable new features in feature management</span></span>

<span data-ttu-id="6327b-108">Noen få av innstillingene som er beskrevet i dette emnet, må være aktivert i systemet før de blir tilgjengelige for deg.</span><span class="sxs-lookup"><span data-stu-id="6327b-108">A few of the settings described in this topic must be enabled on your system before they will be available to you.</span></span> <span data-ttu-id="6327b-109">Bruk [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-siden for å aktivere noen av eller alle de følgende funksjonene ved behov.</span><span class="sxs-lookup"><span data-stu-id="6327b-109">Use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to enable any or all of the following features as required.</span></span>

### <a name="generate-license-plate"></a><span data-ttu-id="6327b-110">Generer nummerskilt</span><span class="sxs-lookup"><span data-stu-id="6327b-110">Generate license plate</span></span>

<span data-ttu-id="6327b-111">For å gjøre denne funksjonen tilgjengelig aktiverer du følgende funksjoner i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rekkefølgen):</span><span class="sxs-lookup"><span data-stu-id="6327b-111">To make this feature available, enable the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in order):</span></span>

1. <span data-ttu-id="6327b-112">Nummerskilt for ferdigmelding lagt til i jobbkortenheten</span><span class="sxs-lookup"><span data-stu-id="6327b-112">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="6327b-113">Aktiver automatisk generering av nummerskiltnummer ved ferdigrapportering i jobbkortenheten</span><span class="sxs-lookup"><span data-stu-id="6327b-113">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>

### <a name="print-label"></a><span data-ttu-id="6327b-114">Skriv ut etikett</span><span class="sxs-lookup"><span data-stu-id="6327b-114">Print label</span></span>

<span data-ttu-id="6327b-115">For å gjøre denne funksjonen tilgjengelig aktiverer du følgende funksjoner i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rekkefølgen):</span><span class="sxs-lookup"><span data-stu-id="6327b-115">To make this feature available, enable the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in order):</span></span>

1. <span data-ttu-id="6327b-116">Nummerskilt for ferdigmelding lagt til i jobbkortenheten</span><span class="sxs-lookup"><span data-stu-id="6327b-116">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="6327b-117">Skriv ut etikett fra jobbkortenhet</span><span class="sxs-lookup"><span data-stu-id="6327b-117">Print label from Job Card Device</span></span>

### <a name="allow-locking-of-touch-screen"></a><span data-ttu-id="6327b-118">Tillate låsing av berøringsskjerm</span><span class="sxs-lookup"><span data-stu-id="6327b-118">Allow locking of touch screen</span></span>

<span data-ttu-id="6327b-119">For å gjøre denne funksjonen tilgjengelig aktiverer du følgende funksjon i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span><span class="sxs-lookup"><span data-stu-id="6327b-119">To make this feature available, enable the following feature in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span></span>

- <span data-ttu-id="6327b-120">(Forhåndsversjon) Funksjon for låsing av jobbkortenheten og jobbkortterminal slik at de kan rengjøres.</span><span class="sxs-lookup"><span data-stu-id="6327b-120">(Preview) Feature for locking job card device and job card terminal so that they can be sanitized</span></span>

## <a name="manage-your-device-configurations"></a><span data-ttu-id="6327b-121">Administrere enhetskonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="6327b-121">Manage your device configurations</span></span>

<span data-ttu-id="6327b-122">For å konfigurere enhetskonfigurasjoner går du til **Produksjonskontroll > Oppsett > Produksjonsutførelse > Konfigurer jobbkort for enheter**.</span><span class="sxs-lookup"><span data-stu-id="6327b-122">To set up your device configurations, go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span> <span data-ttu-id="6327b-123">Siden **Konfigurer jobbkort for enheter** åpnes, og viser en liste over eksisterende konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="6327b-123">The **Configure job card for devices** page opens, which shows a list of existing configurations.</span></span> <span data-ttu-id="6327b-124">Herfra kan du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="6327b-124">From here, you can do the following:</span></span> 

- <span data-ttu-id="6327b-125">Velg en hvilken som helst enhetskonfigurasjon som er oppført i venstre kolonne, for å vise og redigere den.</span><span class="sxs-lookup"><span data-stu-id="6327b-125">Select any device configuration listed in the left column to view and edit it.</span></span>
- <span data-ttu-id="6327b-126">Velg **Ny** i handlingsruten for å legge til en ny enhetskonfigurasjon i listen.</span><span class="sxs-lookup"><span data-stu-id="6327b-126">Select **New** on the Action Pane to add a new device configuration to the list.</span></span> <span data-ttu-id="6327b-127">Deretter angir du et navn i **Konfigurasjon**-feltet slik at du kan identifisere den nye konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="6327b-127">Then enter a name in the **Configuration** field to identify the new configuration.</span></span> <span data-ttu-id="6327b-128">Verdien du angir her, må være unik blant alle enhetskonfigurasjoner, og du vil ikke kunne redigere den senere.</span><span class="sxs-lookup"><span data-stu-id="6327b-128">The value you enter here must be unique among all device configurations, and you won't be able to edit it later.</span></span>

<span data-ttu-id="6327b-129">Se delene nedenfor for mer informasjon om hver av innstillingene for konfigurering av jobbkortenheter.</span><span class="sxs-lookup"><span data-stu-id="6327b-129">Refer to following sections for details about each of the settings for configuring job card devices.</span></span>

## <a name="general-settings"></a><span data-ttu-id="6327b-130">Generelle innstillinger</span><span class="sxs-lookup"><span data-stu-id="6327b-130">General settings</span></span>

<span data-ttu-id="6327b-131">I **Generelt**-hurtigkategorien kan du konfigurere hvert av de ulike alternativene som er tilgjengelige for den valgte enhetskonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="6327b-131">The **General** FastTab lets you configure each of the various options available for the selected device configuration.</span></span> <span data-ttu-id="6327b-132">Følgende innstillinger er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="6327b-132">The following settings are available:</span></span>

- <span data-ttu-id="6327b-133">**Rapporter antall ved utstempling** – sett dette til **Ja** for å be arbeiderne om å rapportere tilbakemelding om jobber som pågår ved utstempling. Når **Nei** er valgt, blir ikke arbeiderne spurt om dette.</span><span class="sxs-lookup"><span data-stu-id="6327b-133">**Report quantity at clock-out** - Set this to **Yes** to prompt workers to report feedback on jobs in progress when clocking out. When set to **No**, workers won't not be prompted.</span></span>
- <span data-ttu-id="6327b-134">**Lås ansatt** – Når dette alternativet er satt til **Nei**, logges hver arbeider av umiddelbart etter at de har gjort en registrering (for eksempel en ny jobb), og deretter går enheten tilbake til påloggingssiden.</span><span class="sxs-lookup"><span data-stu-id="6327b-134">**Lock employee** -  When this option is set to **No**, each worker will be logged out immediately after they make a registration (such as a new job), and then the device will return to the log-in page.</span></span> <span data-ttu-id="6327b-135">Når dette alternativet er satt til **Ja**, vil hver arbeider forbli logget på jobbkortenheten.</span><span class="sxs-lookup"><span data-stu-id="6327b-135">When this option is set to **Yes**, each worker will stay logged in to the job card device.</span></span> <span data-ttu-id="6327b-136">Arbeideren vil likevel kunne logge seg av manuelt for å tillate at en annen arbeider logger seg på mens jobbkortenheten fortsatt kjører med samme systembrukerkonto.</span><span class="sxs-lookup"><span data-stu-id="6327b-136">However, the worker will still be able to log out manually to allow another worker to log in while the job card device remains running under the same system user account.</span></span> <span data-ttu-id="6327b-137">Hvis du vil ha mer informasjon om disse kontotypene, kan du se [Tilordnede brukere](#assigned-users).</span><span class="sxs-lookup"><span data-stu-id="6327b-137">For more information about these types of accounts, see [Assigned users](#assigned-users).</span></span>
- <span data-ttu-id="6327b-138">**Strekkodeskanner** – sett dette til **Ja** for å angi et alternativ på jobbkortenheten som lar arbeiderne registrere at en ny jobb har startet, ved å skanne en strekkode.</span><span class="sxs-lookup"><span data-stu-id="6327b-138">**Barcode scanner** - Set this to **Yes** to provide an option on the job card device that allows workers register the start of a new job by scanning a bar code.</span></span>
- <span data-ttu-id="6327b-139">**Bruk det faktiske registreringstidspunktet** – Velg **Ja** for å angi at tidspunktet for hver nye registrering skal være likt det nøyaktige tidspunktet da registreringen ble sendt av en arbeider.</span><span class="sxs-lookup"><span data-stu-id="6327b-139">**Use the actual time of registration** - Set this to **Yes** to set the time for each new registration to be equal to the exact time that registration was submitted by a worker.</span></span> <span data-ttu-id="6327b-140">Angi **Nei** for å bruke påloggingstiden i stedet.</span><span class="sxs-lookup"><span data-stu-id="6327b-140">Set to **No** to use the log-in time instead.</span></span> <span data-ttu-id="6327b-141">Du bør normalt velge **Ja** hvis du har aktivert **Lås ansatt**- og/eller **Én arbeider**-alternativene, ettersom arbeiderne ofte er logget på i lengre perioder.</span><span class="sxs-lookup"><span data-stu-id="6327b-141">You'll usually want to set this to **Yes** if you have enabled the **Lock employee** and/or **Single worker** options, where workers often remain logged in for longer periods.</span></span>
- <span data-ttu-id="6327b-142">**Én arbeider** – Velg **Ja** hvis bare én arbeider bruker hver jobbkortenhet der denne konfigurasjonen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="6327b-142">**Single worker** - Set this option to **Yes** if only one worker uses each job card device where this configuration is active.</span></span> <span data-ttu-id="6327b-143">Når alternativet er valgt, er **Lås ansatt**-alternativet automatisk satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6327b-143">When this option is selected, the **Lock employee** option is automatically set to **Yes**.</span></span> <span data-ttu-id="6327b-144">I tillegg fjerner dette alternativet behovet (og muligheten) for at arbeideren kan logge på med en kort-ID (eller lignende).</span><span class="sxs-lookup"><span data-stu-id="6327b-144">In addition, this option removes the requirement (and ability) for the worker to log in using a badge ID (or similar).</span></span> <span data-ttu-id="6327b-145">I stedet logger arbeideren seg på Supply Chain Management ved hjelp av en systembrukerkonto som er koblet til et *tidsregistrert arbeider* (fra *arbeidere*-tabellen), og blir samtidig logget på jobbkortenheten som den aktuelle arbeideren</span><span class="sxs-lookup"><span data-stu-id="6327b-145">Instead the worker signs in to Supply Chain Management using a system user account linked to a *time registered worker* (from the *workers* table) and gets logged in to the job card device as that worker at the same time.</span></span>  <span data-ttu-id="6327b-146">Hvis du vil ha mer informasjon om disse kontotypene, kan du se [Tilordnede brukere](#assigned-users).</span><span class="sxs-lookup"><span data-stu-id="6327b-146">For more information about these types of accounts, see [Assigned users](#assigned-users).</span></span>
- <span data-ttu-id="6327b-147">**Tillat at arbeidere kan angi personlige filtre** – Velg **Ja** for å tillate at arbeidere kan filtrere jobbene de ser på enheten.</span><span class="sxs-lookup"><span data-stu-id="6327b-147">**Allow workers to set personal filters** - Set this option to **Yes** to allow workers to filter the jobs shown to them on the device.</span></span> <span data-ttu-id="6327b-148">Arbeideren kan endre verdier for ett av de tre filterkriteriene: **Produksjonsenhet**, **Ressursgruppe** og **Ressurs**.</span><span class="sxs-lookup"><span data-stu-id="6327b-148">The worker can modify values for any of the three filter criteria: **Production unit**, **Resource group** and **Resource**.</span></span> <span data-ttu-id="6327b-149">Bare jobber som er planlagt på ressurser som samsvarer med de valgte filterkriteriene, vises på enheten.</span><span class="sxs-lookup"><span data-stu-id="6327b-149">Only jobs that are scheduled on resources matching the selected filter criteria will be shown on the device.</span></span> <span data-ttu-id="6327b-150">Du kan også tilordne standardverdier for enkelte av eller alle disse kriteriene, og de vil gjelde selv når dette alternativet ikke er valgt.</span><span class="sxs-lookup"><span data-stu-id="6327b-150">You can also assign default values for any or all of these criteria, and those will apply even with this option is not selected.</span></span>
- <span data-ttu-id="6327b-151">**Tillat låsing av berøringsskjermen** – Velg **Ja** for å tillate at arbeiderne kan låse berøringsskjermen for jobbkortenheten slik at de kan rengjøre den.</span><span class="sxs-lookup"><span data-stu-id="6327b-151">**Allow locking the touchscreen** - Set this option to **Yes** to allow workers to lock the job card device touchscreen so they can sanitize it.</span></span> <span data-ttu-id="6327b-152">Når den er aktivert, legges det til en **Lås skjerm for rengjøring** -knapp på påloggingssiden for enheten.</span><span class="sxs-lookup"><span data-stu-id="6327b-152">When enabled, a **Lock screen for sanitizing** button is added to the device log-in page.</span></span> <span data-ttu-id="6327b-153">Når en arbeider velger denne knappen, låses berøringsskjermen midlertidig for å hindre uønskede inndata, og en nedtellingstidtaker vises.</span><span class="sxs-lookup"><span data-stu-id="6327b-153">When a worker selects this button, the touchscreen temporarily locks to prevent unintended input and a countdown timer is shown.</span></span> <span data-ttu-id="6327b-154">Arbeideren kan nå trygt rengjøre enheten og skjermen.</span><span class="sxs-lookup"><span data-stu-id="6327b-154">The worker can now safely clean the device and the screen.</span></span> <span data-ttu-id="6327b-155">Når nedtellingen er fullført, låses berøringsskjermen automatisk opp igjen.</span><span class="sxs-lookup"><span data-stu-id="6327b-155">When the countdown completes, the touchscreen automatically unlocks again.</span></span>
- <span data-ttu-id="6327b-156">**Varighet for skjermlås** – når alternativet **Tillat låsing av berøringsskjerm** er aktivert, bruker du dette alternativet til å angi antall sekunder berøringsskjermen skal være låst for rengjøring.</span><span class="sxs-lookup"><span data-stu-id="6327b-156">**Screen lock duration** - When the **Allow locking touchscreen** option is enabled, use this option so specify number of seconds the touchscreen should be locked for sanitizing.</span></span> <span data-ttu-id="6327b-157">Varigheten må være mellom 5 og 120 sekunder.</span><span class="sxs-lookup"><span data-stu-id="6327b-157">The duration must be between 5 and 120 seconds.</span></span>
- <span data-ttu-id="6327b-158">**Produksjonsenhet** – Velg en produksjonsenhet som skal brukes som standard filterkriterium for listen over jobber som vises for hver arbeider.</span><span class="sxs-lookup"><span data-stu-id="6327b-158">**Production unit** - Select a production unit to be applied as a default filter criterion for the list of jobs shown to each worker.</span></span> <span data-ttu-id="6327b-159">Bare jobber som er planlagt på ressursgrupper under den valgte produksjonsenheten, vises i utgangspunktet av enheten.</span><span class="sxs-lookup"><span data-stu-id="6327b-159">Only jobs that are scheduled on resources grouped under the selected production unit will initially be displayed by the device.</span></span> <span data-ttu-id="6327b-160">Hvis **Tillat at arbeidere kan angi personlige filtre** er aktivert, kan arbeidere redigere denne verdien. Hvis ikke vil dette filteret alltid gjelde når enhetskonfigurasjonen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="6327b-160">If **Allow workers to set personal filters** is enabled, workers will be able to edit this value, otherwise this filter will always apply when this device configuration is active.</span></span>
- <span data-ttu-id="6327b-161">**Ressursgruppe** – Velg en ressursgruppe som skal brukes som standard filterkriterium for listen over jobber som vises for hver arbeider.</span><span class="sxs-lookup"><span data-stu-id="6327b-161">**Resource group** - Select a resource group to be applied as a default filter criterion for the list of jobs shown to each worker.</span></span> <span data-ttu-id="6327b-162">Bare jobber som er planlagt på ressursgrupper under den valgte ressursgruppen, vises i utgangspunktet av enheten.</span><span class="sxs-lookup"><span data-stu-id="6327b-162">Only jobs that are scheduled on resources grouped under the selected resource group will initially be displayed by the device.</span></span> <span data-ttu-id="6327b-163">Hvis **Tillat at arbeidere kan angi personlige filtre** er aktivert, kan arbeidere redigere denne verdien. Hvis ikke vil dette filteret alltid gjelde når enhetskonfigurasjonen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="6327b-163">If **Allow workers to set personal filters** is enabled, workers will be able to edit this value, otherwise this filter will always apply when this device configuration is active.</span></span>
- <span data-ttu-id="6327b-164">**Ressurs** – Velg en ressurs som skal brukes som standard filterkriterium for listen over jobber som vises for hver arbeider.</span><span class="sxs-lookup"><span data-stu-id="6327b-164">**Resource** - Select a resource to be applied as a default filter criterion for the list of jobs shown to each worker.</span></span> <span data-ttu-id="6327b-165">Bare jobber som er planlagt på den valgte ressursen, vises i utgangspunktet av enheten.</span><span class="sxs-lookup"><span data-stu-id="6327b-165">Only jobs that are scheduled on the selected resource will initially be displayed by the device.</span></span> <span data-ttu-id="6327b-166">Hvis **Tillat at arbeidere kan angi personlige filtre** er aktivert, kan arbeidere redigere denne verdien. Hvis ikke vil dette filteret alltid gjelde når enhetskonfigurasjonen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="6327b-166">If **Allow workers to set personal filters** is enabled, workers will be able to edit this value, otherwise this filter will always apply when this device configuration is active.</span></span>
- <span data-ttu-id="6327b-167">**Generer nummerskilt** – sett dette alternativet til **Ja** for å generere et nytt nummerskilt hver gang en arbeider bruker en jobbkortenhet for å ferdigmelde.</span><span class="sxs-lookup"><span data-stu-id="6327b-167">**Generate license plate** - Set this option to **Yes** to generate a new license plate each time a worker uses the job card device to report as finished.</span></span> <span data-ttu-id="6327b-168">Skiltnummeret genereres fra en nummerserie som er definert på **Parametere for lagerstyring**-siden.</span><span class="sxs-lookup"><span data-stu-id="6327b-168">The license plate number is generated from a number sequence set up on the **Warehouse management parameters** page.</span></span> <span data-ttu-id="6327b-169">Når den er satt til **Nei**, må arbeiderne angi et eksisterende nummerskilt når de ferdigmelder seg.</span><span class="sxs-lookup"><span data-stu-id="6327b-169">When set to **No**, workers must specify an existing license plate when reporting as finished.</span></span>
- <span data-ttu-id="6327b-170">**Skriv ut etikett** – sett dette alternativet til **Ja** for å skrive ut en nummerskiltetikett når en arbeider bruker jobbkortenheten til å ferdigmelde.</span><span class="sxs-lookup"><span data-stu-id="6327b-170">**Print label** - Set this option to **Yes** to print a license plate label when a worker uses the job card device to report as finished.</span></span> <span data-ttu-id="6327b-171">Konfigurasjonen av etiketten defineres i dokumentruting, som beskrevet i [Dokumentrutingsoppsett for nummerskiltetiketter](../warehousing/document-routing-layout-for-license-plates.md).</span><span class="sxs-lookup"><span data-stu-id="6327b-171">The configuration of the label is set up in document routing, as described in [Document routing layout for license plate labels](../warehousing/document-routing-layout-for-license-plates.md).</span></span>

<a name="assigned-users"></a>

## <a name="assigned-users"></a><span data-ttu-id="6327b-172">Tilordnede brukere</span><span class="sxs-lookup"><span data-stu-id="6327b-172">Assigned users</span></span>

<span data-ttu-id="6327b-173">Bruk **Tilordnede brukere**-hurtigkategorien for å knytte én eller flere systembrukere til den gjeldende enhetskonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="6327b-173">Use the **Assigned users** FastTab to associate one or more system users with the current device configuration.</span></span> <span data-ttu-id="6327b-174">Hver systembruker kan bare tilordnes én jobbenhetskonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="6327b-174">Each system user can only be assigned one job device configuration.</span></span>

<span data-ttu-id="6327b-175">Når du konfigurerer en enhet, logger en IT-arbeider vanligvis på Supply Chain Management ved hjelp av en systembrukerkonto.</span><span class="sxs-lookup"><span data-stu-id="6327b-175">When setting up a device, an IT worker typically signs in to Supply Chain Management using a system user account.</span></span> <span data-ttu-id="6327b-176">Deretter gjelder jobbenhetskonfigurasjonen som er tilknyttet systembrukeren, så lenge den systembrukeren fortsatt er logget på.</span><span class="sxs-lookup"><span data-stu-id="6327b-176">Thereafter, the job device configuration associated with that system user applies for as long as that system user remains signed in.</span></span> <span data-ttu-id="6327b-177">Disse systembrukerkontoene er vanligvis begrenset til bare å tillate tilgang til enhetssiden for jobbkort og ingen annen del av Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6327b-177">These system user accounts are typically limited to allow access only to the job card device page and no other part of Supply Chain Management.</span></span>

<span data-ttu-id="6327b-178">Når systembrukeren er logget på, og jobbenhetskonfigurasjonen er lastet inn, kan vedkommende deretter logge på jobbkortenheten ved å bruke den *tidsregistrerte arbeider*-kontoen (for eksempel ved å skanne en strekkode på kortet), slik at de kan starte nye jobber og utføre andre typer registreringer.</span><span class="sxs-lookup"><span data-stu-id="6327b-178">After the system user is signed in and the job device configuration is loaded, workers can then log in to the job card device using their *time registered worker* account (for example, by scanning a bar code on their badge) so they can start new jobs and make other kinds of registrations.</span></span> <span data-ttu-id="6327b-179">Ulike arbeidere kan logge på og av i løpet av dagen, men den samme enhetskonfigurasjonen forblir aktivert på den aktuelle maskinen fordi systembrukeren fortsatt er logget på Supply Chain Management for dagen.</span><span class="sxs-lookup"><span data-stu-id="6327b-179">Various workers can log in and out during the day, while the same device configuration remains in effect on that machine because the system user remains signed in to Supply Chain Management for the day.</span></span>

<span data-ttu-id="6327b-180">Men som nevnt tidligere, når du for eksempel bruker en enhetskonfigurasjon med alternativet **Én arbeider**, logger arbeiderne seg vanligvis på Supply Chain Management ved hjelp av en systembruker som er koblet til deres egen *tidsregistrert arbeider*-konto, slik at de laster inn enhetskonfigurasjonen og logger på som en arbeider på jobbkortenheten samtidig.</span><span class="sxs-lookup"><span data-stu-id="6327b-180">However, as mentioned previously, when you use a device configuration with the **Single worker** option, workers themselves typically sign in to Supply Chain Management using a system user linked to their own *time registered worker* account, so they load the device configuration and log in as a worker on the job card device at the same time.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6327b-181">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6327b-181">Additional resources</span></span>

[<span data-ttu-id="6327b-182">Ferdigmeld fra den jobbkortenheten.</span><span class="sxs-lookup"><span data-stu-id="6327b-182">Report as finished from the job card device</span></span>](report-finished-job-device.md)