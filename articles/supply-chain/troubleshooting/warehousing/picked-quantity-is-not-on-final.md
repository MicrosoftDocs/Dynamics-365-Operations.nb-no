---
title: Du kan ikke bekrefte en forsendelse fordi varer ikke har blitt plukket
description: Du kan ikke bekrefte en forsendelse fordi varer ikke har blitt plukket
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301311"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="ac97e-103">Du kan ikke bekrefte en forsendelse fordi varer ikke har blitt plukket</span><span class="sxs-lookup"><span data-stu-id="ac97e-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="ac97e-104">Feilkode: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="ac97e-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="ac97e-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="ac97e-105">Symptoms</span></span>

<span data-ttu-id="ac97e-106">Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="ac97e-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="ac97e-107">Noen av varene som trengs for lasten %1, har ennå ikke blitt plukket og flyttet til den endelige forsendelseslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="ac97e-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="ac97e-108">Derfor kan du ikke bekrefte forsendelsen for belastningen.</span><span class="sxs-lookup"><span data-stu-id="ac97e-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="ac97e-109">Årsak</span><span class="sxs-lookup"><span data-stu-id="ac97e-109">Cause</span></span>

<span data-ttu-id="ac97e-110">Belastningen eller forsendelsen kan ikke bekreftes i gjeldende tilstand, fordi det kan hende at én av følgende betingelser finnes:</span><span class="sxs-lookup"><span data-stu-id="ac97e-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="ac97e-111">Det relaterte arbeidet er ennå ikke plukket og flyttet til den endelige forsendelseslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="ac97e-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="ac97e-112">Det plukkede arbeidsantallet samsvarer ikke med det opprettede arbeidsantallet på belastningslinjen.</span><span class="sxs-lookup"><span data-stu-id="ac97e-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="ac97e-113">Lokasjonsdirektivet er konfigurert med emballasjelokasjon som den endelige forsendelseslokasjonen ved bruk av bølgemalcontainerbruk.</span><span class="sxs-lookup"><span data-stu-id="ac97e-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="ac97e-114">Løsning</span><span class="sxs-lookup"><span data-stu-id="ac97e-114">Resolution</span></span>

<span data-ttu-id="ac97e-115">Lasten eller forsendelsen er for øyeblikket i en tilstand der forsendelsesbekreftelsen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="ac97e-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="ac97e-116">Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="ac97e-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="ac97e-117">Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.</span><span class="sxs-lookup"><span data-stu-id="ac97e-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="ac97e-118">Avbryt arbeids-IDene som er opprettet med emballasjelokasjonen som endelig forsendelseslokasjon, konfigurer lokasjonsdirektivet på nytt, og slett lasten på nytt.</span><span class="sxs-lookup"><span data-stu-id="ac97e-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="ac97e-119">Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer</span><span class="sxs-lookup"><span data-stu-id="ac97e-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="ac97e-120">Bruk følgende fremgangsmåte til å g gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.</span><span class="sxs-lookup"><span data-stu-id="ac97e-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="ac97e-121">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="ac97e-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="ac97e-122">Velg belastningen som forsendelsen ikke kan bekreftes for.</span><span class="sxs-lookup"><span data-stu-id="ac97e-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="ac97e-123">I hurtigfanen **Lastlinjer** velger du lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="ac97e-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="ac97e-124">Legg merke til verdien i feltet **Antall for arbeid opprettet**.</span><span class="sxs-lookup"><span data-stu-id="ac97e-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="ac97e-125">I handlingsruten, i fanen **Laster** i gruppen **Relatert informasjon**, velger du **Arbeid**.</span><span class="sxs-lookup"><span data-stu-id="ac97e-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="ac97e-126">Kontroller at arbeidet er fullført på det endelige forsendelsesstedet, og at det plukkede arbeidsantallet samsvarer med det opprettede arbeidsantallet på belastningslinjen.</span><span class="sxs-lookup"><span data-stu-id="ac97e-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="ac97e-127">Gjenta denne fremgangsmåten for alle belastningslinjer for å være sikker på at alle kriteriene er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="ac97e-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="ac97e-128">Avbryt arbeids-IDene som er opprettet med emballasjelokasjonen som endelig forsendelseslokasjon, konfigurer lokasjonsdirektivet på nytt, og slett lasten på nytt</span><span class="sxs-lookup"><span data-stu-id="ac97e-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="ac97e-129">Bruk fremgangsmåten nedenfor til å avbryte arbeids-IDene som har emballasjelokasjonen som endelig plasseringslokasjon med automatisert containerbruk på plass.</span><span class="sxs-lookup"><span data-stu-id="ac97e-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="ac97e-130">Gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Avbryt arbeid**.</span><span class="sxs-lookup"><span data-stu-id="ac97e-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="ac97e-131">Dialogboksen **Avbryt arbeid** åpnes.</span><span class="sxs-lookup"><span data-stu-id="ac97e-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="ac97e-132">Angi IDen for arbeidet du vil avbryte, i **Arbeids-ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ac97e-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="ac97e-133">Den valgte arbeids-IDen må ha **Arbeidsstatus**-verdien *Åpen*, *Pågår*, *Avbrutt*, *Kombinert* eller *Lukket*.</span><span class="sxs-lookup"><span data-stu-id="ac97e-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="ac97e-134">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac97e-134">Select **OK**.</span></span>
1. <span data-ttu-id="ac97e-135">Velg **Ja** for å bekrefte at du vil avbryte arbeidet.</span><span class="sxs-lookup"><span data-stu-id="ac97e-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="ac97e-136">Gjenta denne fremgangsmåten for de andre arbeids-IDene etter behov.</span><span class="sxs-lookup"><span data-stu-id="ac97e-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="ac97e-137">For mer informasjon, se [Avbryte lagerarbeid for unntaksbehandling](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="ac97e-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="ac97e-138">Bruk fremgangsmåten nedenfor til å konfigurere lokasjonsdirektivet på nytt, slik at det ikke bruker emballasjelokasjonen som endelig forsendelseslokasjon når automatisert containerbruk er definert for bølgemalen.</span><span class="sxs-lookup"><span data-stu-id="ac97e-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="ac97e-139">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="ac97e-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="ac97e-140">Velg *Salgsordrer* i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="ac97e-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="ac97e-141">Velg lokasjonsdirektivet du bruker for automatisert containerbruk.</span><span class="sxs-lookup"><span data-stu-id="ac97e-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="ac97e-142">I **Lokasjonsdirektivhandlinger**-hurtigfaneverktøylinjen velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="ac97e-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="ac97e-143">I dialogboksen for Power Query-redigering, i fanen **Område**, finner du raden der **Felt** er satt til *Lokasjonsprofil*, og kontroller at **Kriterier**-feltet for denne raden ikke er satt til en lokasjonsprofil som har **Lokasjonstype** *Emballasje*.</span><span class="sxs-lookup"><span data-stu-id="ac97e-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="ac97e-144">Juster **Kriterier**-feltet for å rette den endelige plasserte lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="ac97e-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="ac97e-145">Bruk fremgangsmåten nedenfor til å slette belastningen på nytt og opprette arbeids-IDer med riktig endelig forsendelseslokasjon.</span><span class="sxs-lookup"><span data-stu-id="ac97e-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="ac97e-146">Gå til **Lagerstyring \> Laster \> Arbeidsområde for lastplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="ac97e-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="ac97e-147">I **Last**-delen finner du lasten som må frigis.</span><span class="sxs-lookup"><span data-stu-id="ac97e-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="ac97e-148">I delen **Laster** velger du **Frigi \> Frigi til lager** for å frigi den valgte lasten til lageret.</span><span class="sxs-lookup"><span data-stu-id="ac97e-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="ac97e-149">Gjenta denne fremgangsmåten for de andre lastene etter behov.</span><span class="sxs-lookup"><span data-stu-id="ac97e-149">Repeat this procedure for the other loads as needed.</span></span>
