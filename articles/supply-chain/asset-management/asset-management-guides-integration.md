---
title: Integrere Dynamics 365 Supply Chain Management (Aktivabehandling) med Dynamics 365 Guides
description: Dette emnet forklarer hvordan du integrerer Aktivabehandling-modulen i Microsoft Dynamics 365 Supply Chain Management med Dynamics 365 Guides for å dra nytte av veiledninger for to virkelighet i de daglige tjeneste- og vedlikeholdsarbeidsflytene.
author: kamaybac
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 50cfea6656e1f13532b018784fa64b2aac10fc7f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908573"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="c4f61-103">Integrere Dynamics 365 Supply Chain Management (Aktivabehandling) med Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="c4f61-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="c4f61-104">Du kan integrere **Aktivabehandling**-modulen i Microsoft Dynamics 365 Supply Chain Management med Dynamics 365 Guides for å dra nytte av veiledninger for to virkelighet i de daglige tjeneste- og vedlikeholdsarbeidsflytene.</span><span class="sxs-lookup"><span data-stu-id="c4f61-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="c4f61-105">Hvis en veiledning er knyttet til en arbeidsordre for aktivastyring, vil en arbeider som åpner kontrolliste for vedlikehold for arbeidsordren i mobilappen for Supply Chain Management (Dynamics 365), se at en veiledning er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="c4f61-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="c4f61-106">Arbeideren kan deretter finne og åpne veiledningen i Dynamics 365 Guides HoloLens-appen.</span><span class="sxs-lookup"><span data-stu-id="c4f61-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c4f61-107">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="c4f61-107">Prerequisites</span></span>

<span data-ttu-id="c4f61-108">Før du kan dra nytte av veiledninger for arbeidsordrer for aktivabehandling, må du fullføre disse forutsetningene:</span><span class="sxs-lookup"><span data-stu-id="c4f61-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="c4f61-109">[Konfigurer Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) versjon 10.0.9 eller senere.</span><span class="sxs-lookup"><span data-stu-id="c4f61-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="c4f61-110">[Aktivere toveis skriving for Supply Chain Management-apper](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="c4f61-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="c4f61-111">[Aktiver testversjon](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for **MRGuidesFeature**-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="c4f61-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="c4f61-112">(For produksjonsmiljøer må du først sende en støtteforespørsel for å få leieren din lagt til i kontrollgruppen.)</span><span class="sxs-lookup"><span data-stu-id="c4f61-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="c4f61-113">[Slå på følgende konfigurasjonsnøkler](/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) på **Lisenskonfigurasjon**-siden:</span><span class="sxs-lookup"><span data-stu-id="c4f61-113">[Turn on the following configuration keys](/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="c4f61-114">Aktivabehandling \> Aktivabehandling, blandet virkelighet</span><span class="sxs-lookup"><span data-stu-id="c4f61-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="c4f61-115">Blandet virkelighet \> Blandet virkelighet-veiledning</span><span class="sxs-lookup"><span data-stu-id="c4f61-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="c4f61-116">[Konfigurer Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versjon 200.0.0.96 eller senere.</span><span class="sxs-lookup"><span data-stu-id="c4f61-116">[Set up Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="c4f61-117">Bruke Dynamics 365 Guides med aktivastyring</span><span class="sxs-lookup"><span data-stu-id="c4f61-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="c4f61-118">Hvis du vil knytte til en veiledning, bruker du en kontrollistelinje for vedlikehold i Aktivabehandling.</span><span class="sxs-lookup"><span data-stu-id="c4f61-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="c4f61-119">Du kan opprette tilknytningen gjennom en mal for kontrolliste for vedlikehold, en vedlikeholdsjobbtype eller en arbeidsordre, fordi alle tre inneholder vedlikeholdssjekklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="c4f61-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="c4f61-120">Du kan spare tid ved hjelp av en mal, fordi en mal kan knyttes til alle vedlikeholdsjobbtypene som bruker den.</span><span class="sxs-lookup"><span data-stu-id="c4f61-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="c4f61-121">En veiledning som for eksempel er tilknyttet en vedlikeholdsjobbtype, knyttes automatisk til alle arbeidsordrer som angir denne jobbtypen.</span><span class="sxs-lookup"><span data-stu-id="c4f61-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="c4f61-122">På den andre siden vil en veiledning som er knyttet direkte til en arbeidsordre, bare finnes for den aktuelle arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="c4f61-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="c4f61-123">Knytte en veiledning til en mal for kontrolliste for vedlikehold</span><span class="sxs-lookup"><span data-stu-id="c4f61-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="c4f61-124">Følg disse trinnene for å knytte en veiledning til en mal for kontrolliste for vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="c4f61-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="c4f61-125">Opprett en veiledning ved å bruke Dynamics 365 Guides-PC og HoloLens-apper.</span><span class="sxs-lookup"><span data-stu-id="c4f61-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="c4f61-126">Hvis du vil ha informasjon om hvordan du oppretter en veiledning, kan du se emnene nedenfor:</span><span class="sxs-lookup"><span data-stu-id="c4f61-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="c4f61-127">Bruke PC-appen til å opprette en veiledning</span><span class="sxs-lookup"><span data-stu-id="c4f61-127">Use the PC app to create a guide</span></span>](/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="c4f61-128">Bruke HoloLens-appen til å plassere hologrammene</span><span class="sxs-lookup"><span data-stu-id="c4f61-128">Use the HoloLens app to place your holograms</span></span>](/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="c4f61-129">I Supply Chain Management [oppretter du en mal for vedlikeholdssjekkliste](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span><span class="sxs-lookup"><span data-stu-id="c4f61-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="c4f61-130">Knytt til veiledningen du opprettet ved hjelp av kontrollistelinjen for vedlikehold i den nye malen for vedlikeholdssjekkliste:</span><span class="sxs-lookup"><span data-stu-id="c4f61-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="c4f61-131">I hurtigfanen **Vedlikeholdssjekklistelinjer** velger du linjen du vil knytte veiledningen til.</span><span class="sxs-lookup"><span data-stu-id="c4f61-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="c4f61-132">På hurtigfanen **Tilknyttede veiledninger** velger du **Legg til veiledning**.</span><span class="sxs-lookup"><span data-stu-id="c4f61-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="c4f61-133">![Knytte en veiledning til en kontrollistelinje for vedlikehold](media/am-guides-integration-add-guide.png "Knytte en veiledning til en kontrollistelinje for vedlikehold")</span><span class="sxs-lookup"><span data-stu-id="c4f61-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="c4f61-134">I **Navn**-feltet velger du veiledningen og deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c4f61-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="c4f61-135">![Velg en veiledning i Navn-feltet](media/am-guides-integration-select-guide.png "Velg en veiledning i Navn-feltet")</span><span class="sxs-lookup"><span data-stu-id="c4f61-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="c4f61-136">Knytt kontrollistemalen for vedlikehold til en jobbtype:</span><span class="sxs-lookup"><span data-stu-id="c4f61-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="c4f61-137">[Opprett en vedlikeholdsjobbtype](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), eller velg en eksisterende vedlikeholdsjobbtype.</span><span class="sxs-lookup"><span data-stu-id="c4f61-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="c4f61-138">Velg **Standarder for vedlikeholdsjobbtype** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c4f61-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="c4f61-139">![Knappen Standarder for vedlikeholdsjobbtype](media/am-guides-integration-job-defaults.png "Knappen Standarder for vedlikeholdsjobbtype")</span><span class="sxs-lookup"><span data-stu-id="c4f61-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="c4f61-140">Opprett en linje, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c4f61-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="c4f61-141">![Opprett en linje](media/am-guides-integration-add-line.png "Opprett en linje")</span><span class="sxs-lookup"><span data-stu-id="c4f61-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="c4f61-142">Velg **Sjekkliste for vedlikehold** på handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c4f61-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="c4f61-143">![Knappen Sjekkliste for vedlikehold](media/am-guides-integration-maintenance-checklist.png "Knappen Sjekkliste for vedlikehold")</span><span class="sxs-lookup"><span data-stu-id="c4f61-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="c4f61-144">På hurtigfanen **Vedlikeholdssjekklistelinjer** legger du til en linje, og deretter endrer du verdien i feltet **Type** til **Mal**.</span><span class="sxs-lookup"><span data-stu-id="c4f61-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="c4f61-145">![Endre Type-verdien](media/am-guides-integration-checklist-lines.png "Endre Type-verdien")</span><span class="sxs-lookup"><span data-stu-id="c4f61-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="c4f61-146">I hurtigfanen **Linjedetaljer** i feltet **Mal** velger du malen du vil knytte veiledningen til, og deretter valger du **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c4f61-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="c4f61-147">![Velg malen](media/am-guides-integration-checklist-line-details.png "Velg malen")</span><span class="sxs-lookup"><span data-stu-id="c4f61-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="c4f61-148">[Opprett en arbeidsordre](work-orders/manually-created-workorders.md#create-work-order), og velg deretter vedlikeholdsjobbtypen som bruker sjekklistemalen for vedlikehold som du knyttet veiledningen til.</span><span class="sxs-lookup"><span data-stu-id="c4f61-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="c4f61-149">Veiledning knyttes automatisk til arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="c4f61-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="c4f61-150">![Velg en vedlikeholdsjobbtype](media/am-guides-integration-create-work-order.png "Velg en vedlikeholdsjobbtype")</span><span class="sxs-lookup"><span data-stu-id="c4f61-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="c4f61-151">Vis veiledningen som er knyttet til arbeidsordren og arbeiderne:</span><span class="sxs-lookup"><span data-stu-id="c4f61-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="c4f61-152">Åpne [Mobilt arbeidsområde for aktivabehandling](asset-management-mobile-workspace.md) for å få tilgang til arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="c4f61-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="c4f61-153">[Åpne kontrollisten for vedlikehold](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="c4f61-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="c4f61-154">Velg en sjekklistelinje for å vise den tilknyttede veiledningen.</span><span class="sxs-lookup"><span data-stu-id="c4f61-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="c4f61-155">![Veiledning tilknyttet en sjekklistelinje](media/am-guides-integration-show-guide.png "Veiledning tilknyttet en sjekklistelinje")</span><span class="sxs-lookup"><span data-stu-id="c4f61-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="c4f61-156">Åpne veiledningen på HoloLens.</span><span class="sxs-lookup"><span data-stu-id="c4f61-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="c4f61-157">![Åpne veiledningen på HoloLens](media/am-guides-integration-hololens-select.png "Åpne veiledningen på HoloLens")</span><span class="sxs-lookup"><span data-stu-id="c4f61-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="c4f61-158">Du kan også tilknytte en veiledning direkte i kontrolliste for vedlikehold for en arbeidsordre eller en jobbtype.</span><span class="sxs-lookup"><span data-stu-id="c4f61-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4f61-159">Det finnes et kjent problem: Når du knytter en sjekklistemal for vedlikehold til en standard vedlikeholdsjobbtype, vises ikke veiledningen som er koblet til malen, på hurtigfanen **Tilknyttede veiledninger** på siden **Standarder for vedlikeholdsjobbtype**.</span><span class="sxs-lookup"><span data-stu-id="c4f61-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="c4f61-160">Veiledningen vises imidlertid etter at denne jobbtypen er brukt på en arbeidsordre på hurtigfanen **Tilknyttede veiledninger**.</span><span class="sxs-lookup"><span data-stu-id="c4f61-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4f61-161">Se også</span><span class="sxs-lookup"><span data-stu-id="c4f61-161">See also</span></span>

- [<span data-ttu-id="c4f61-162">Oversikt over dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="c4f61-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="c4f61-163">Oversikt over anleggsmiddelbehandling</span><span class="sxs-lookup"><span data-stu-id="c4f61-163">Asset management overview</span></span>](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]