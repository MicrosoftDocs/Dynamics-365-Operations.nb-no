---
title: Manuelt opprettede arbeidsordrer
description: Dette emnet forklarer hvordan du oppretter arbeidsordrer manuelt i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875818"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="b0377-103">Manuelt opprettede arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="b0377-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="b0377-104">Du kan opprette arbeidsordrer manuelt på to måter:</span><span class="sxs-lookup"><span data-stu-id="b0377-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="b0377-105">i **Alle arbeidsordrer** eller **Aktive arbeidsordrer**</span><span class="sxs-lookup"><span data-stu-id="b0377-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="b0377-106">i **Alle vedlikeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler** eller **Mine vedlikeholdsforespørsler for arbeidssted**</span><span class="sxs-lookup"><span data-stu-id="b0377-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="b0377-107">Opprett arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="b0377-107">Create work order</span></span>

1. <span data-ttu-id="b0377-108">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b0377-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="b0377-109">Klikk på **Ny**-knappen.</span><span class="sxs-lookup"><span data-stu-id="b0377-109">Click the **New** button.</span></span>

3. <span data-ttu-id="b0377-110">I rullegardinlisten **Opprett arbeidsordre** velger du en arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="b0377-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="b0377-111">Velg en beskrivelse om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="b0377-111">If required, select a description.</span></span>

5. <span data-ttu-id="b0377-112">Velg anleggsmiddelet for arbeidsordren og en vedlikeholdsjobbtype.</span><span class="sxs-lookup"><span data-stu-id="b0377-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="b0377-113">Når du velger et aktiva, kan tre kategorier være tilgjengelige: Kategorien **Mine aktiva** inneholder aktiva som er knyttet til arbeidsstedene der du (personen som er logget på systemet), kan være tilordnet (oppsett i [Vedlikeholdsarbeidere og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="b0377-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="b0377-114">Hvis ingen arbeidssteder er definert for en person i [Vedlikeholdsarbeidere og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md), er ikke kategorien **Mine aktiva** synlig.</span><span class="sxs-lookup"><span data-stu-id="b0377-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="b0377-115">Kategorien **Aktive aktiva** inneholder en liste over alle aktiva med statusen "Aktiv" for livsløpstilstanden.</span><span class="sxs-lookup"><span data-stu-id="b0377-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="b0377-116">Kategorien **Aktivavisning** viser en trevisning av arbeidssteder og aktiva som er installert på disse stedene.</span><span class="sxs-lookup"><span data-stu-id="b0377-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="b0377-117">Velg om nødvendig **Variant av vedlikeholdsjobbtype** og **Handel**.</span><span class="sxs-lookup"><span data-stu-id="b0377-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="b0377-118">Hvis det er nødvendig, kan du endre servicenivået for arbeidsordren i **Servicenivå**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0377-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="b0377-119">Velg forventet start- og sluttdato i de tilknyttede feltene.</span><span class="sxs-lookup"><span data-stu-id="b0377-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="b0377-120">Klikk på **OK** for å opprette en ny arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="b0377-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="b0377-121">Rediger arbeidsordren i **Alle arbeidsordrer** om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="b0377-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="b0377-122">I **Alle arbeidsordrer** kan du legge til flere aktiva i en arbeidsordre i detaljvisningen ved å legge til linjer i hurtigfanen **Vedlikeholdsjobber for arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="b0377-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="b0377-123">I et aktiva kan du bare velge vedlikeholdsjobbtypene som er definert for aktivatypen som er valgt for aktivaet.</span><span class="sxs-lookup"><span data-stu-id="b0377-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="b0377-124">Hvis du har endret et servicenivå for et anleggsmiddel eller en kritisk aktivitet for et anleggsmiddel etter at du har brukt dem i en arbeidsordre (se [Tjenestenivåer for aktiva](../setup-for-objects/object-priorities.md) og [Kritiske forhold omkring aktiva](../setup-for-objects/object-criticalities.md)), oppdateres ikke servicenivået eller kritikaliteten i arbeidsordren tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="b0377-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="b0377-125">Kritikaliteten i en arbeidsordre beregnes på nytt hver gang en arbeidsordrelinje legges til eller slettes i arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="b0377-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="b0377-126">I **Alle arbeidsordrer**-detaljvisningen > **Hode**-visningen > **Plan**-hurtigfanen kan du velge en ansvarlig vedlikeholdspersongruppe eller en ansvarlig vedlikeholdsperson i feltene **Ansvarlig gruppe** eller **Ansvarlig**.</span><span class="sxs-lookup"><span data-stu-id="b0377-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="b0377-127">Disse innstillingene kan endres så lenge arbeidsordren er aktiv, for eksempel når livssyklustilstanden for arbeidsordren endres.</span><span class="sxs-lookup"><span data-stu-id="b0377-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="b0377-128">Det automatiske valget som gjøres under opprettingen av arbeidsordrer, er basert på oppsettet i **Ansvarlige vedlikeholdsarbeidere**.</span><span class="sxs-lookup"><span data-stu-id="b0377-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="b0377-129">Hvis du legger til eller fjerner arbeidsordrejobber etter at du har opprettet en arbeidsordre, og **Ansvarlig gruppe**-feltet og **Ansvarlig**-feltet er tomme når du oppdaterer arbeidsordren, søker Aktivastyring etter et mulig treff i oppsettsskjemaet for en ansvarlig vedlikeholdspersongruppe eller ansvarlig vedlikeholdsperson.</span><span class="sxs-lookup"><span data-stu-id="b0377-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="b0377-130">Hvis **Ansvarlig gruppe**-feltet eller **Ansvarlig**-feltet allerede er fylt ut når du oppdaterer arbeidsordren, gjøres det ingen endringer.</span><span class="sxs-lookup"><span data-stu-id="b0377-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="b0377-131">I **Vedlikeholdsstatus** kan du gjøre en beregning for å få en oversikt over arbeidsbelastningen for innkommende og fullførte arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="b0377-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="b0377-132">I hurtigfanen **Linjedetaljer** bruker du feltene **Breddegrad** og **Lengdegrad** til å legge til geografiske koordinater for aktivaet som er valgt i arbeidsordrejobben.</span><span class="sxs-lookup"><span data-stu-id="b0377-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="b0377-133">Opprett relatert arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="b0377-133">Create related work order</span></span>

<span data-ttu-id="b0377-134">Du kan opprette en relatert arbeidsordre til en eksisterende arbeidsordre hvis du for eksempel vil arbeide med primære og sekundære arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="b0377-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="b0377-135">En ny arbeidsordre er basert på en arbeidsordrejobb fra en eksisterende arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="b0377-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="b0377-136">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b0377-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="b0377-137">Velg arbeidsordren som du vil opprette en tilknyttet arbeidsordre for.</span><span class="sxs-lookup"><span data-stu-id="b0377-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="b0377-138">Klikk på **Relatert arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="b0377-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="b0377-139">I rullegardinlisten **Opprett relatert arbeidsordre** velger du arbeidsordrejobben som du vil opprette en tilknyttet arbeidsordre for, i feltet **Arbeidsordrejobb**.</span><span class="sxs-lookup"><span data-stu-id="b0377-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="b0377-140">Velg en vedlikeholdsjobbtype i feltet **Vedlikeholdsjobbtype**, og, om nødvendig, en tilknyttet variant av vedlikeholdsjobbtype og handel i feltene **Variant av vedlikeholdsjobbtype** og **Handel**.</span><span class="sxs-lookup"><span data-stu-id="b0377-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="b0377-141">Hvis dette er den første tilknyttede arbeidsordren du oppretter, klikker du på alternativknappen **Ny arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="b0377-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="b0377-142">Velg en **arbeidsordretype** og en **beskrivelse** i de tilknyttede feltene.</span><span class="sxs-lookup"><span data-stu-id="b0377-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="b0377-143">Hvis det er nødvendig, endrer du servicenivået for arbeidsordren i **Servicenivå**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0377-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="b0377-144">Sett inn forventet start- og sluttdato i de tilknyttede feltene.</span><span class="sxs-lookup"><span data-stu-id="b0377-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="b0377-145">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0377-145">Click **OK**.</span></span> <span data-ttu-id="b0377-146">Den nye tilknyttede arbeidsordren vises i listen **Alle arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b0377-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="b0377-147">Hvis du oppretter en relatert arbeidsordre i en arbeidsordre som allerede har tilknyttede arbeidsordrer, kan du legge til arbeidsordrejobben i en allerede tilknyttet arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="b0377-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="b0377-148">Dette gjøres ved å klikke på alternativknappen **Legg til tilknyttet arbeidsordre** i trinn 6.</span><span class="sxs-lookup"><span data-stu-id="b0377-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="b0377-149">Deretter velger du den tilknyttede arbeidsordren som du vil legge til en ny arbeidsordrejobb i.</span><span class="sxs-lookup"><span data-stu-id="b0377-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="b0377-150">Rediger **Servicenivå**, **Forventet start**- og **Forventet slutt**-feltene etter behov, og klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0377-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="b0377-151">Arbeidsordrejobben legges til den eksisterende tilknyttede arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="b0377-151">The work order job is added to the existing related work order.</span></span>


![Figur 1](media/03-work-orders.png)

<span data-ttu-id="b0377-153">**Obs!** Hvis du har definert en relatert arbeidsordremaske i **Aktivabehandlingsparametere** > **Arbeidsordrer**-koblingen > **Relatert arbeidsordremaske**-feltet, blir det opprettet arbeidsordre-ID-er i samsvar med maskeoppsettet.</span><span class="sxs-lookup"><span data-stu-id="b0377-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="b0377-154">Hvis det ikke er definert en tilknyttet arbeidsordremaske, vil den neste tilgjengelige arbeidsordre-ID-en brukes for tilknyttede arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="b0377-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="b0377-155">Kopier arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="b0377-155">Copy work order</span></span>

<span data-ttu-id="b0377-156">Det er mulig å opprette en ny arbeidsordre fra en eksisterende arbeidsordre raskt.</span><span class="sxs-lookup"><span data-stu-id="b0377-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="b0377-157">Denne måten å arbeide med arbeidsordrer på er forskjellig fra å opprette arbeidsordrer basert på vedlikeholdsplaner.</span><span class="sxs-lookup"><span data-stu-id="b0377-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="b0377-158">Det er nyttig hvis du for eksempel har en arbeidsordre med mange arbeidsordrejobber med ulike jobber for ulike anleggsmidler som skal fullføres med jevne mellomrom.</span><span class="sxs-lookup"><span data-stu-id="b0377-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="b0377-159">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b0377-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="b0377-160">Velg arbeidsordren du vil kopiere innhold fra.</span><span class="sxs-lookup"><span data-stu-id="b0377-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="b0377-161">Klikk på **Kopier arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="b0377-161">Click **Copy work order**.</span></span> <span data-ttu-id="b0377-162">Arbeidsordreoppsettet fra den valgte arbeidsordren vises.</span><span class="sxs-lookup"><span data-stu-id="b0377-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="b0377-163">Hvis det er nødvendig, kan du redigere noen av feltene.</span><span class="sxs-lookup"><span data-stu-id="b0377-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="b0377-164">Klikk på **OK** for å opprette den nye arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="b0377-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="b0377-165">Rediger arbeidsordren i **Alle arbeidsordrer** om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="b0377-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="b0377-166">Når den nye arbeidsordren opprettes, kopieres noe informasjon direkte fra den eksisterende arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="b0377-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="b0377-167">Informasjon om prognoser, verktøy, sjekklister for vedlikehold, arbeidssted, adresser og planlegging blir ikke kopiert, men initialisert fra gjeldende oppsett i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="b0377-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="b0377-168">Dette betyr at hvis det ble gjort endringer i disse dataene fra tidspunktet da den første arbeidsordren ble opprettet, til tidspunktet du opprettet en kopi av arbeidsordren, blir disse endringene tatt med i den nye arbeidsordren du har opprettet.</span><span class="sxs-lookup"><span data-stu-id="b0377-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="b0377-169">Eksempler er endringer i prognoser eller oppdaterte kontrollister for vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="b0377-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![Figur 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="b0377-171">Opprette arbeidsordre basert på en vedlikeholdsanmodning</span><span class="sxs-lookup"><span data-stu-id="b0377-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="b0377-172">Klikk på **Aktivastyring** > **Felles** > **Vedlikeholdsforespørsler** > **Alle vedlikeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="b0377-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="b0377-173">Velg vedlikeholdsforespørselen du vil opprette en arbeidsordre for, og klikk på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="b0377-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="b0377-174">Klikk på **Arbeidsordre** i **Alle forespørsler**.</span><span class="sxs-lookup"><span data-stu-id="b0377-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="b0377-175">Fyll ut rullegardinlisten **Arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="b0377-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="b0377-176">Hvis en vedlikeholdsjobbtype er valgt i vedlikeholdsforespørselen, kan du velge en annen vedlikeholdsjobbtype, hvis det er nødvendig, når du oppretter arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="b0377-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="b0377-177">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0377-177">Click **OK**.</span></span> <span data-ttu-id="b0377-178">Du vil se en melding som gir deg beskjed om at arbeidsordren er opprettet.</span><span class="sxs-lookup"><span data-stu-id="b0377-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="b0377-179">Hvis du vil se hvilke arbeidsordrer som er knyttet til en vedlikeholdsforespørsel, velger du vedlikeholdsforespørselen i listene **Alle vedlikeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler** og klikker på **Arbeidsordrer**-knappen.</span><span class="sxs-lookup"><span data-stu-id="b0377-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![Figur 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="b0377-181">Arbeidsordrer kan også opprettes automatisk ved å planlegge vedlikeholdsplanjobber, eller ved å definere vedlikeholdsplaner for automatisk oppretting eller vedlikeholdsrunder for et anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="b0377-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="b0377-182">Arbeidsordrer opprettet fra vedlikeholdsforespørsler i **Vedlikeholdsplan** opprettes med vedlikeholdsjobbtypene som er valgt i vedlikeholdsforespørslene.</span><span class="sxs-lookup"><span data-stu-id="b0377-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

