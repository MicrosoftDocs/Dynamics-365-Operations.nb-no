---
title: Manuelt opprettede arbeidsordrer
description: Dette emnet forklarer hvordan du oppretter arbeidsordrer manuelt i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4a4b148d9ac5d032d2caa5fcea0398a5a3726f0e
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888983"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="8df9c-103">Manuelt opprettede arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="8df9c-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="8df9c-104">Du kan opprette arbeidsordrer manuelt på to måter:</span><span class="sxs-lookup"><span data-stu-id="8df9c-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="8df9c-105">På siden **Alle arbeidsordrer** eller **Aktive arbeidsordrer**</span><span class="sxs-lookup"><span data-stu-id="8df9c-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="8df9c-106">På siden **Alle vedlikeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler** eller **Mine vedlikeholdsforespørsler for arbeidssted**</span><span class="sxs-lookup"><span data-stu-id="8df9c-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="8df9c-107">Opprett arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="8df9c-107">Create work order</span></span>

1. <span data-ttu-id="8df9c-108">Velg **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="8df9c-109">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-109">Select **New**.</span></span>

3. <span data-ttu-id="8df9c-110">I dialogboksen **Opprett arbeidsordre** velger du en arbeidsordretype i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="8df9c-111">Velg en **Beskrivelse** om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="8df9c-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="8df9c-112">Velg feltet **Aktivum** velger du aktivaet.</span><span class="sxs-lookup"><span data-stu-id="8df9c-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="8df9c-113">Når du velger et aktivum, kan tre kategorier være tilgjengelige i rullegardinlisten **Aktivum**:</span><span class="sxs-lookup"><span data-stu-id="8df9c-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="8df9c-114">Kategorien **Aktive aktiva** – Denne kategorien inneholder en liste over alle aktiva med en "Aktiv" livsløpstilstand.</span><span class="sxs-lookup"><span data-stu-id="8df9c-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="8df9c-115">**Aktivavisning** – Denne kategorien viser en trevisning av arbeidssteder og aktiva som er installert på dem.</span><span class="sxs-lookup"><span data-stu-id="8df9c-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="8df9c-116">**Mine aktiva** – Denne kategorien inneholder aktiva som er relatert til arbeidsstedene som du (arbeideren som er logget på systemet) kan tildeles.</span><span class="sxs-lookup"><span data-stu-id="8df9c-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="8df9c-117">(Hvis du vil ha informasjon om oppsettet, kan du se [Vedlikeholdsarbeidere og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md).) Hvis ingen arbeidssteder er definert for en arbeider i [Vedlikeholdsarbeidere og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md), er ikke kategorien **Mine aktiva** tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="8df9c-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="8df9c-118">I feltet **Vedlikeholdsjobbtype** velger du en vedlikeholdsjobbtype for arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="8df9c-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="8df9c-119">Velg om nødvendig **Variant av vedlikeholdsjobbtype** og **Handel**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="8df9c-120">Hvis det er nødvendig, kan du endre servicenivået for arbeidsordren i **Servicenivå**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8df9c-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="8df9c-121">Velg **Forventet startdato** og **Forventet sluttdato** i de tilknyttede feltene.</span><span class="sxs-lookup"><span data-stu-id="8df9c-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="8df9c-122">Klikk på **OK** for å opprette arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="8df9c-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="8df9c-123">På listesiden **Alle arbeidsordrer** kan du redigere arbeidsordren etter behov.</span><span class="sxs-lookup"><span data-stu-id="8df9c-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="8df9c-124">Merk følgende punkt:</span><span class="sxs-lookup"><span data-stu-id="8df9c-124">Note the following points:</span></span>

- <span data-ttu-id="8df9c-125">I detaljvisningen på listesiden **Alle arbeidsordrer** kan du legge til flere aktiva i en arbeidsordre ved å legge til linjer i hurtigfanen **Vedlikeholdsjobber for arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="8df9c-126">I et aktivum kan du bare velge vedlikeholdsjobbtypene som er definert for aktivatypen som er valgt for aktivumet.</span><span class="sxs-lookup"><span data-stu-id="8df9c-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="8df9c-127">Hvis du endrer servicenivået eller aktivakritikalitet for aktivumet etter at du har brukt det på en arbeidsordre, oppdateres ikke servicenivået eller kritikaliteten i arbeidsordren i henhold til dette.</span><span class="sxs-lookup"><span data-stu-id="8df9c-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="8df9c-128">Hvis du vil ha mer informasjon om servicenivåer og kritikaliteter, se [Tjenestenivåer for aktiva](../setup-for-objects/object-priorities.md) og [Type kritisk aktivitet for aktiva](../setup-for-objects/object-criticalities.md).</span><span class="sxs-lookup"><span data-stu-id="8df9c-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="8df9c-129">Kritikaliteten i en arbeidsordre beregnes på nytt hver gang en arbeidsordrejobb legges til eller slettes fra arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="8df9c-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="8df9c-130">I detaljvisningen **Alle arbeidsordrer** > kategorien **Hode** > **Plan**-hurtigfanen i feltet **Ansvarlig gruppe** eller **Ansvarlig** kan du velge en ansvarlig vedlikeholdspersongruppe eller en ansvarlig vedlikeholdsperson.</span><span class="sxs-lookup"><span data-stu-id="8df9c-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="8df9c-131">Disse innstillingene kan endres mens arbeidsordren er aktiv.</span><span class="sxs-lookup"><span data-stu-id="8df9c-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="8df9c-132">De kan for eksempel endres når tilstanden for arbeidsordrelivssyklusen endres.</span><span class="sxs-lookup"><span data-stu-id="8df9c-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="8df9c-133">Det automatiske valget som gjøres under opprettingen av arbeidsordrer, er basert på oppsettet på siden **Ansvarlige vedlikeholdsarbeidere**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="8df9c-134">Hvis du legger til eller fjerner arbeidsordrejobber etter at du har opprettet en arbeidsordre, og hvis feltene **Ansvarlig gruppe** og **Ansvarlig** er tomme når du oppdaterer arbeidsordren, søker Aktivastyring etter en ansvarlig vedlikeholdspersongruppe eller en ansvarlig vedlikeholdsperson.</span><span class="sxs-lookup"><span data-stu-id="8df9c-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="8df9c-135">Hvis **Ansvarlig gruppe**-feltet eller **Ansvarlig**-feltet allerede er angitt når du oppdaterer arbeidsordren, gjøres det ingen endringer.</span><span class="sxs-lookup"><span data-stu-id="8df9c-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="8df9c-136">Hvis du vil ha informasjon om ansvarlige vedlikeholdsarbeidere og arbeidergrupper, kan du se [Ansvarlige vedlikeholdsarbeidere](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="8df9c-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="8df9c-137">På siden [Vedlikeholdsstatus](../controlling-and-reporting/maintenance-status.md) kan du gjøre en beregning for å få en oversikt over arbeidsbelastningen for innkommende og fullførte arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="8df9c-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="8df9c-138">I detaljvisningen på siden **Alle arbeidsordrer** i hurtigfanen **Linjedetaljer** kan du bruke feltene **Breddegrad** og **Lengdegrad** til å legge til geografiske koordinater for aktiva som er valgt i arbeidsordrejobben.</span><span class="sxs-lookup"><span data-stu-id="8df9c-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="8df9c-139">Opprett relatert arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="8df9c-139">Create related work order</span></span>

<span data-ttu-id="8df9c-140">Du kan opprette en arbeidsordre som er knyttet til en eksisterende arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="8df9c-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="8df9c-141">Denne funksjonen er nyttig hvis du for eksempel vil arbeide med primære og sekundære arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="8df9c-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="8df9c-142">En ny arbeidsordre er basert på en arbeidsordrejobb fra en eksisterende arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="8df9c-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="8df9c-143">Velg **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="8df9c-144">Velg arbeidsordren du vil opprette en relatert arbeidsordre for.</span><span class="sxs-lookup"><span data-stu-id="8df9c-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="8df9c-145">Velg **Relatert arbeidsordre** i gruppen **Ny** i kategorien **Arbeidsordre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8df9c-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="8df9c-146">I dialogboksen **Opprett relatert arbeidsordre** velger du arbeidsordrejobben som du vil opprette en tilknyttet arbeidsordre for, i feltet **Arbeidsordrejobb**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="8df9c-147">Velg en vedlikeholdsjobbtype i feltet **Vedlikeholdsjobbtype**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="8df9c-148">Velg en relatert vedlikeholdsjobbtypevariant og -handel i feltene **Variant av vedlikeholdsjobbtype** og **Handel** etter behov.</span><span class="sxs-lookup"><span data-stu-id="8df9c-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="8df9c-149">Hvis denne arbeidsordren er den første tilknyttede arbeidsordren som er opprettet for den valgte arbeidsordren, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="8df9c-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="8df9c-150">Velg alternativet **Ny arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="8df9c-151">Velg en arbeidsordretype i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="8df9c-152">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8df9c-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="8df9c-153">Hvis det er nødvendig, endrer du servicenivået for arbeidsordren i **Servicenivå**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8df9c-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="8df9c-154">Velg start- og sluttdatoer i feltene **Forventet start** og **Forventet slutt**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="8df9c-155">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-155">Select **OK**.</span></span> <span data-ttu-id="8df9c-156">Den nye tilknyttede arbeidsordren vises på listesiden **Alle arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="8df9c-157">Hvis arbeidsrekkefølgen du oppretter denne tilknyttede arbeidsordren for, allerede har tilknyttede arbeidsordrer, følger du denne fremgangsmåten for å legge til en ny arbeidsordrejobb i en eksisterende relatert arbeidsordre:</span><span class="sxs-lookup"><span data-stu-id="8df9c-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="8df9c-158">Velg alternativet **Legg til tilknyttet arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="8df9c-159">Velg den tilknyttede arbeidsordren som du vil legge til en ny arbeidsordrejobb i, i feltet **Arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="8df9c-160">Hvis det er nødvendig, endrer du servicenivået for arbeidsordren i **Servicenivå**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8df9c-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="8df9c-161">Endre start- og sluttdatoer i feltene **Forventet start** og **Forventet slutt** etter behov.</span><span class="sxs-lookup"><span data-stu-id="8df9c-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="8df9c-162">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-162">Select **OK**.</span></span> <span data-ttu-id="8df9c-163">Arbeidsordrejobben legges til den eksisterende tilknyttede arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="8df9c-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="8df9c-164">Illustrasjonen nedenfor viser et eksempel på dialogboksen **Opprett relatert arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![Figur 1](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="8df9c-166">Hvis du har definert en relatert arbeidsordremaske i **Aktivabehandlingsparametere** > **Arbeidsordrer**-kategorien > **Relatert arbeidsordremaske**-feltet, blir det opprettet arbeidsordre-ID-er i samsvar med maskeoppsettet.</span><span class="sxs-lookup"><span data-stu-id="8df9c-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="8df9c-167">Hvis det ikke er definert en tilknyttet arbeidsordremaske, vil den neste tilgjengelige arbeidsordre-ID-en brukes for tilknyttede arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="8df9c-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="8df9c-168">Kopiere en arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="8df9c-168">Copy a work order</span></span>

<span data-ttu-id="8df9c-169">Du kan opprette en ny arbeidsordre fra en eksisterende arbeidsordre raskt.</span><span class="sxs-lookup"><span data-stu-id="8df9c-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="8df9c-170">Denne måten å arbeide med arbeidsordrer på er forskjellig fra å opprette arbeidsordrer basert på [vedlikeholdsplaner](../preventive-and-reactive-maintenance/maintenance-plans.md).</span><span class="sxs-lookup"><span data-stu-id="8df9c-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="8df9c-171">Det er nyttig hvis du for eksempel har en arbeidsordre med mange arbeidsordrejobber, og de ulike jobbene skal fullføres på ulike aktiva med jevne mellomrom.</span><span class="sxs-lookup"><span data-stu-id="8df9c-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="8df9c-172">Velg **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="8df9c-173">Velg arbeidsordren du vil kopiere innhold fra.</span><span class="sxs-lookup"><span data-stu-id="8df9c-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="8df9c-174">Velg **Kopier arbeidsordre** i gruppen **Ny** i kategorien **Arbeidsordre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8df9c-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="8df9c-175">Arbeidsordreoppsettet fra den valgte arbeidsordren vises.</span><span class="sxs-lookup"><span data-stu-id="8df9c-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="8df9c-176">Du kan redigere noen av feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="8df9c-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="8df9c-177">Velg **OK** for å opprette den nye arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="8df9c-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="8df9c-178">På listesiden **Alle arbeidsordrer** kan du redigere arbeidsordren etter behov.</span><span class="sxs-lookup"><span data-stu-id="8df9c-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="8df9c-179">Når den nye arbeidsordren opprettes, kopieres noe informasjon direkte fra den eksisterende arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="8df9c-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="8df9c-180">Informasjon om prognoser, verktøy, kontrollister for vedlikehold, funksjonsplassering, adresser og planlegging kopieres ikke.</span><span class="sxs-lookup"><span data-stu-id="8df9c-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="8df9c-181">Den initialiseres i stedet fra det gjeldende oppsettet i aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="8df9c-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="8df9c-182">Hvis denne informasjonen ble endret fra tiden da den første arbeidsordren ble opprettet, og tidspunktet da du laget en kopi av arbeidsordren, blir imidlertid endringene tatt med i den nye arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="8df9c-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="8df9c-183">Eksempler inneholder endringer for prognoser eller oppdateringer av kontrollister for vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="8df9c-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="8df9c-184">Illustrasjonen nedenfor viser et eksempel på dialogboksen **Kopier arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![Figur 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="8df9c-186">Opprette en arbeidsordre basert på en vedlikeholdsanmodning</span><span class="sxs-lookup"><span data-stu-id="8df9c-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="8df9c-187">Velg **Aktivastyring** > **Felles** > **Vedlikeholdsforespørsler** > **Alle vedlikeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="8df9c-188">Velg vedlikeholdsforespørselen du vil opprette en arbeidsordre for, og klikk på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="8df9c-189">Velg **Arbeidsordre** i gruppen **Ny** i kategorien **Vedlikeholdsanmodning** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8df9c-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="8df9c-190">I dialogboksen **Arbeidsordre** angir du feltene.</span><span class="sxs-lookup"><span data-stu-id="8df9c-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="8df9c-191">Hvis en vedlikeholdsjobbtype er valgt i vedlikeholdsforespørselen, kan du velge en annen vedlikeholdsjobbtype når du oppretter arbeidsordren, etter behov.</span><span class="sxs-lookup"><span data-stu-id="8df9c-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="8df9c-192">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-192">Select **OK**.</span></span> <span data-ttu-id="8df9c-193">En meldingen forteller deg at en arbeidsordre er blitt opprettet.</span><span class="sxs-lookup"><span data-stu-id="8df9c-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="8df9c-194">Hvis du vil se hvilke arbeidsordrer som er knyttet til en vedlikeholdsforespørsel, velger du vedlikeholdsforespørselen på listesiden **Alle vedlikeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="8df9c-195">Deretter velger du **Arbeidsordre** i gruppen **Vis** i kategorien **Vedlikeholdsanmodning** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8df9c-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="8df9c-196">Illustrasjonen nedenfor viser et eksempel på dialogboksen **Opprett arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="8df9c-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![Figur 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="8df9c-198">Hvis du vil at arbeidsordrer skal opprettes automatisk, kan du planlegge vedlikeholdsplanjobber, eller du kan konfigurere "Opprett automatisk" [vedlikeholdsplaner](../preventive-and-reactive-maintenance/maintenance-plans.md) eller [vedlikeholdsrunder](../preventive-and-reactive-maintenance/maintenance-rounds.md) på aktivumet.</span><span class="sxs-lookup"><span data-stu-id="8df9c-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="8df9c-199">Arbeidsordrer som opprettes fra vedlikeholdsforespørsler på listesiden **Alle vedlikeholdsplaner**, har vedlikeholdsjobbtypene som er valgt på vedlikeholdsforespørslene.</span><span class="sxs-lookup"><span data-stu-id="8df9c-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

